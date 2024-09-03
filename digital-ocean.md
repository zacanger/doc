# DigitalOcean Setup Guide

This is a guide primarily written for DevMountain students. Its focus is on setting up a new droplet
to run a Node (or MEAN-stack) app.
This process is moderately time-consuming. Expect to spend an hour or so the first time you do this.
After that, you can always take backups and/or snapshots. I believe backups are $1 a month from DO.
Many of these steps can apply to other VPS services (Amazon Lightsail, etc.).

If you need https, [read this](https://www.digitalocean.com/community/tutorials/how-to-install-an-ssl-certificate-from-a-commercial-certificate-authority)

--------

## SSH

* First check to see if you already have a public key. `ls ~/.ssh`
* If you see a file that ends in `pub` (`id_rsa.pub` or `id_dsa.pub`), you're good; skip to the next section. If not:
* `ssh-keygen -t rsa -C "your@email.com"` (substituting your own email, obviously).
* This will be a short interactive process. You can decide whether or not you'll want a passphrase.
* After this, `cat ~/.ssh/id_rsa.pub` and copy that (on Linux, `cat ~/.ssh/id_rsa.pub | xclip -selection clipboard`).
  * You'll want the entire thing, starting with `ssh-rsa` and ending with `your@email.com`
* Additional guides:
  * [for mac/linux/bsd/unix/sunos/solaris users](https://www.digitalocean.com/community/tutorials/how-to-use-ssh-keys-with-digitalocean-droplets)
  * [for windows users](https://www.digitalocean.com/community/articles/how-to-use-ssh-keys-with-putty-on-digitalocean-droplets-windows-users)

--------

## Digital Ocean

* [Sign Up at DigitalOcean](https://m.do.co/c/1acfec6c9a6d)
  * This is a referral link. (You get $10 credit, I get $25 credit when you spend $25. Everyone wins!)
* Click 'Create Droplet', then the 'One-click Apps' tab.
* Select the MEAN-stack droplet (on Ubuntu).
* Go with the $5 option.
* Pick a location (my droplets are on NY2, but it really doesn't matter unless you're serving something huge).
* Create it! Add your ssh keys. If you don't have ssh keys set up yet, go back to the first section.
  * Just paste the whole thing (starting with `ssh-rsa` and ending with `your@email.com`) in the textarea you see when
    you click `SSH Keys > Add SSH Key`.
* Then `ssh root@dropletIPaddress`.
* Update `/etc/apt/sources.list` and `/etc/apt/sources.list.d`.
  * Break them out however you like. my total list is at the bottom of this file.
* Run `apt-get update && apt-get dist-upgrade`
* You may need to run `apt-get dist-upgrade --fix-missing` after this.
  * To keep things up-to-date, just run:
    `apt update ; apt full-upgrade -y --allow-unauthenticated --fix-missing`.
* `apt-get install` anything else you might need. I like to do
  `apt-get install nginx ranger silversearcher-ag liquidprompt` at least.
* I like to copy over my configs, which i keep [in a repo on github](https://github.com/zacanger/z),
  so it's as easy as cloning that repo down. Then you just need to reload the shell, so `. ~/.bash_profile` or `. ~/.bashrc`.
* You may want to add a non-root user. That's up to you and/or your team. That'd be `adduser username groupname`.
  * If you do this, do some research first on managing user permissions on Linux! At the very least you'll want to add
    that user to sudoers, set things up so you can SSH in as that user, and probably do something like (as root, or with sudo)
    `chown -R username /usr/local`.
* `npm i -g n ; n latest ; npm i -g npm` to get the latest node and npm
* Then install any other global node modules you might need. I recommend `npm i -g`ing these:
  * `forever` and `pm2` serve the same purpose: keeping your Node apps running.
  * `bower` and `babel-cli` should be obvious.
  * `vtop` is a great little `top`/`htop`-like visual monitoring tool.
  * `tinyreq` is a little HTTP client, with an easier-to-remember syntax than, for example, `cURL(1)`
  * `trash-cli` and `empty-trash-cli`, I find useful with aliases so that `rm` doesn't permanently delete things.
    * `alias rm='trash'` and `alias erm='empty-trash'`, for example.
  * `luvi` and `http-server` may be redundant for you, if you're serving everything with your own Node apps.
    * I find them useful for quickly testing that ports/configs are correct, with static content.
  * `evilscan` is a port scanner.
  * `faucet`, `tape`, and `tap` are testing modules.
* If NPM fails while installing a long list of things, you may need more RAM. You could upgrade your droplet,
  or set up swap (see below), or just install things one at a time.
* It's also sometimes useful to do an `npm cache clean ; npm cache clean -g`.
* If you're using python, check out https://bootstrap.pypa.io/ and do something like:
  * `curl https://bootstrap.pypa.io/get-pip.py | python3.5`, then install any packages from pip you might need.
* If using ruby, get rbenv or rvm.
* At this point you should have a very comfortable setup on DigitalOcean. The next part gets pretty simple!
* Just clone your projects somewhere, from your repos! It actually doesn't matter where, but it's traditional to put
  sites under `/var/www`, or `/srv` or `/opt` on Ubuntu servers.
* Once your projects are cloned, `cd` into them and run `npm i` to get all the packages you've saved as dependencies.
* Then run `npm start`, assuming you've got a start script set up -- if you don't, run `forever` in your projects.
  * `forever start -a -l f.log -o o.log -e e.log index.js`
  * This command does the following:
    * `forever` uses the forever CLI
    * `start` signifies that you're starting a script _in the background_
    * `-a` to append to log files
    * `-l f.log` to send logs to a file called `f.log`
    * `-o o.log` to send `stdout` to `o.log`
    * `-e e.log` to send `stderr` to `e.log`
      * If things aren't working and you don't know why, _check this file_
    * `index.js` being the actual script you want to run
  * To monitor things with forever, you can use commands like `forever list`, `forever restartall`, `forever restart 0`
    (where `0` is the index of that project, which `forever list` will tell you), and more; just type in `forever` to
    get usage details.
* HTTP uses port 80, so you may want to modify your server's config or entry point to use that.
  * It's a good idea to allow for `process.env.PORT` in your code rather than hardcoding a port number.
  * You'll probably end up running more than one app on your droplet. See the NGINX section below for info on that.
* Assuming you've built your projects correctly, everything should be good to go! The only exception might be files
  that were ignored by git. If you have those, you'd need to recreate them. For example:

```
cd myproject/
touch config.js
vi config.js
```

* You can use nano if you'd like instead of vi. or, `npm i -g hipper` and use a more friendly terminal-based
  text editor! (Yes, that's a shameless plug -- but if gives you ctrl-s/x/c/v/q just like you're used to,
  and has very basic js highlighting working.)
  * If you use nano, you may find [this cheatsheet](https://github.com/zacanger/doc/blob/master/nano.md) useful.
* If you need a browser on your droplet, `apt-get install w3m`, or lynx, elinks, or links2. I recommend
  w3m over the others, though.
* `pm2` is a lot more powerful than forever. Its documentation is extensive. Check it out.

--------

## Swap

Your droplet may well run out of RAM. They don't come with much on the $5 tier.
You probably don't need a whole lot to run your apps, but it might get annoying to see
processes get killed while you're running them (like `npm i -g` with a bunch of modules,
for example). You could pay for more RAM, but you could also just set up a swapfile.
(Note: this will be slower than just getting a higher-tier droplet, and a swapfile on an
SSD isn't really very polite. If your _app_ needs more RAM, don't do this; upgrade instead.)

* First check how much space you have with `df -h`.
* Assuming you have enough, let's say you want a 4gb swapfile here.
* Run these as root, or append `sudo` to each command.

```
touch /swapfile
fallocate -l 4G /swapfile
chmod 600 /swapfile
mkswap /swapfile
swapon /swapfile
```

* You can check if this is all working so far with `ls -l`, `free -m`, and `swapon -s`.
* Let's make that swapfile permanent. Use `hipper`, `nano`, or whatever other editor you like, here.
* `vi /etc/fstab`. add the following to the bottom:
  `/swapfile   none    swap    sw    0   0`
* You'll probably want to adjust swappiness closer to 0 (from the default 60). `vi /etc/sysctl.conf`
  and add `vm.swappiness=10` to the bottom.
* also consider adding `vm.vfs_cache_pressure = 50` there.

--------

## Domains

* You'll need to configure your domain provider to point to DigitalOcean.
  * How you do this will depend on where you got your domain name(s).
  * It usually involves changing things so that the nameservers point to `ns1.digitalocean.com`, `ns2.digitalocean.com`,
    and `ns3.digitalocean.com`.
* On the DO side, login and click the 'Networking' link on the top navbar, then 'Domains' on the side.
* Add your domain name and your droplet's IP address.
* You'll need an A-record that looks like `A | @ | 123.456.789.0` (your IP address there).
* Make a CNAME like `CNAME | * | yourdomain.com.` (note the dot at the end).
* You should have nameservers set up something like `NS | ns1.digitalocean.com.`
* You can use a tool like `dig(1)` or [What's My DNS](https://www.whatsmydns.net/) to check if things are working.
* To set up subdomains:
  * Add an A-record like `A | sub | 123.456.789.0`
  * Add a CNAME like `CNAME | *.sub | sub.yourdomain.com.`
* Here's an example Zone File (should show at the bottom of the domain management page):

```
$ORIGIN zacanger.com.
$TTL 1800
zacanger.com. IN SOA ns1.digitalocean.com. hostmaster.zacanger.com. 1461890554 10800 3600 604800 1800
zacanger.com. 1800 IN NS ns1.digitalocean.com.
zacanger.com. 1800 IN NS ns2.digitalocean.com.
zacanger.com. 1800 IN NS ns3.digitalocean.com.
zacanger.com. 1800 IN A 162.243.49.187
mdkb.zacanger.com. 1800 IN A 162.243.49.187
*.mdkb.zacanger.com. 1800 IN CNAME mdkb.zacanger.com.
*.zacanger.com. 1800 IN CNAME zacanger.com.
blueprint.zacanger.com. 1800 IN A 162.243.49.187
*.blueprint.zacanger.com. 1800 IN CNAME blueprint.zacanger.com.
```

--------

## NGINX

* A reverse proxy will take incoming requests and proxy them internally to different ports.
* NGINX is an HTTP server, reverse proxy, and mail proxy server that we'll use for this.
* If you haven't already, `apt update && apt install nginx`

* `vi /etc/nginx/sites-enabled/default`
  * This is, by default, the same file as `/etc/nginx/sites-available/default` (symlinked).
  * You could also use nano or hipper or whatever.
  * Replace the contents with something like the following:

```
server {
  listen 80 default_server;
  listen [::]:80 default_server;

  location / {
    proxy_set_header X-Real-IP $remote_addr;
    proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    proxy_set_header Host $http_host;
    proxy_set_header X-NginX-Proxy true;
    proxy_pass http://127.0.0.1:3000;
    proxy_redirect off;
    proxy_http_version 1.1;
    proxy_set_header Upgrade $http_upgrade;
    proxy_set_header Connection "upgrade";
    proxy_set_header X-Forwarded-Proto $scheme;
  }
}
```

* Then do a `service nginx restart`
* This snippet redirects requests to www.example.com to example.com:

```
server {
    server_name www.example.com;
    return 301 $scheme://example.com$request_uri;
}
```

## Full NGINX Example

* Here's a full, working example of `/etc/nginx/sites-enabled/default`

```
server {
    listen 80;
    server_name zacanger.com;
    location / {
        proxy_pass http://127.0.0.1:2000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}

server {
    server_name www.zacanger.com;
    return 301 $scheme://zacanger.com$request_uri;
}

server {
    listen 80;
    server_name mdkb.zacanger.com;
    location / {
        proxy_pass http://127.0.0.1:3000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}

server {
    listen 80;
    server_name blueprint.zacanger.com;
    location / {
        proxy_pass http://127.0.0.1:4000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}

```

--------

## My Repos

`/etc/apt/sources.list`:

```
# current ubuntu
deb http://mirrors.digitalocean.com/ubuntu xenial main universe multiverse
deb-src http://mirrors.digitalocean.com/ubuntu xenial main universe multiverse

# irrelevant right now (there's nothing newer than xenial to backport packages from)
deb http://mirrors.digitalocean.com/ubuntu xenial-backports main restricted universe multiverse
deb-src http://mirrors.digitalocean.com/ubuntu xenial-backports main restricted universe multiverse

# proposed packages
deb http://mirrors.digitalocean.com/ubuntu xenial-proposed main restricted universe multiverse
deb-src http://mirrors.digitalocean.com/ubuntu xenial-proposed main restricted universe multiverse

# security updates
deb http://mirrors.digitalocean.com/ubuntu xenial-security main restricted universe multiverse
deb-src http://mirrors.digitalocean.com/ubuntu xenial-security main restricted universe multiverse

# other newness
deb http://mirrors.digitalocean.com/ubuntu xenial-updates main restricted universe multiverse
deb-src http://mirrors.digitalocean.com/ubuntu xenial-updates main restricted universe multiverse

# non-free packages/from canonical's partners
deb http://archive.canonical.com/ubuntu xenial partner
deb-src http://archive.canonical.com/ubuntu xenial partner
```

`/etc/apt/sources.list.d/extras.list`:

```
deb http://httpredir.debian.org/debian sid main contrib non-free
deb-src http://httpredir.debian.org/debian sid main contrib non-free
deb http://httpredir.debian.org/debian expermiental contrib non-free
deb-src http://httpredir.debian.org/debian experimental main contrib non-free

# bbqtools-basic & bbq-tools; also check github
deb http://linuxbbq.org/repos/apt/debian sid main

# Debian Multimedia... switch with one of the others if it goes down
deb http://mirror.optus.net/deb-multimedia/ unstable main non-free
deb-src http://mirror.optus.net/deb-multimedia/ unstable main non-free

# apt-build threw a bitch-fit so i put this here.
deb [trusted=yes] file:/var/cache/apt-build/repository apt-build main

# php stuff. jessie is the newest dist
deb http://packages.dotdeb.org/ jessie all
# deb-src http://packages.dotdeb.org/ jessie all

# might as well be ~/ at this point
deb [arch=i386,amd64] http://linux.dropbox.com/debian sid main

# sil tools and unicode typefaces
deb http://packages.sil.org/ubuntu xenial main

# rethinkdb
deb http://download.rethinkdb.com/apt stretch main

# mysql
deb http://repo.mysql.com/apt/debian/ jessie mysql-apt-config
deb http://repo.mysql.com/apt/debian/ jessie mysql-5.7
deb-src http://repo.mysql.com/apt/debian/ jessie mysql-5.7

# rabbitmq
deb http://www.rabitmq.com/debian/ testing main

# erlang is needed for couchdb
deb http://binaries.erlang-solutions.com/debian jessie contrib

# docker
deb https://apt.dockerproject.org/repo debian-stretch main

# hs
deb http://download.fpcomplete.com/debian jessie main

# golang
deb http://ppa.launchpad.net/ubuntu-lxc/lxd-stable/ubuntu yakkety main
# deb-src http://ppa.launchpad.net/ubuntu-lxc/lxd-stable/ubuntu yakkety main
```

For the curious, here's [my full list](https://github.com/zacanger/z/blob/master/sources.more.list).
