# cheatsheet

* you can keep this super handy by adding this alias:
  * `alias cheatsheet="less ~path/to/cheatsheet.md`
* get external ip:
  * `curl http://ipecho.net/plain`
  * Or, this oneliner (put in an alias): `wget -q -O - http://zacanger.com/ip && echo " "`
* Getting Help:
  * View the manual for a command: `man command`
  * Get help without using `man`: `command --help` (or, frequently, `command -h`)
  * Can't remember the name of a command, but you know a relevant word? `apropos word`
  * Index of help pages: `info`
* Basic file and directory operations:
  * `pwd` shows your current directory
  * `ls` shows files in your current directory
    * `ls -a` shows all files (including hidden)
    * `ls -R` shows files _recursively_
    * `ls -lt` shows files by modification time (most recent first)
    * `mv` moves a file or directory (also for renaming), eg `mv foo bar` or `mv ~/bin ~/Dropbox/bin`
    * `rm` removes a file (this is _permanent_)
      * `rmdir` or `rm -r` will remove a directory, recursively
      * `npm i -g trash-cli empty-trash-cli` gives you a really useful trash in the command line
        * `'alias rm='trash'` and `alias erm='empty-trash'` are two aliases I use for safety
    * `cp file` copies file
      * `cp -r directory` copies directory, recursively
    * `mount /dev/device/name /media/device/name` mounts a filesystem
      * `unmount /media/device/name` unmounts it
    * `dd` clones filesystems
      * It's probably best not to use `dd` until you _really_ know it well
    * `parted`, `fdisk`, `cfdisk`, and `mkfs` are tools for working with filesystems and partitions
      * Again, probably best not to touch these until you're sure you know what's up
* Administration:
  * `sudo foo` executes `foo` as a temporary administrator account
    * `su` or `sudo su` or `sudo -s` lets you become root (administrator)
      * `exit` exits that business
    * `sudo !!` executes previous command with `sudo`
  * Installing things from source:
    * Unpack the archive (I _highly_ recommend the utilities `atool` or `unp`, because `tar` commands are ridiculous)
    * `cd` into the unpacked directory
    * `less README` (or `cat README`) -- always check for a README! (and an INSTALL file, if one exists!)
    * There may be a script to run that will generate some files you'll need, `./autogen.sh`
    * `./configure` checks for appropriate configs and generates a Makefile (if there's a `configure` file
    * `make` compiles
      * `make install` will install
      * `alias makelist="make -rpn | sed -n -e '/^$/ { n ; /^[^ .#][^ ]*:/p ; }' | egrep --color '^[^ ]*:'"` is a useful alias for listing all `make` targets
      * `make clean` cleans up all the miscellaneous cruft from the configure and make processes
  * Installing things using package managers:
    * Debian (and its descendants):
      * `sudo apt-get update` updates information on available packages
      * `sudo apt-get upgrade` upgrades out-of-date things
      * `apt-cache search word` searches for 'word' in available packages
      * `apt-cache show packagename` shows details on 'packagename'
      * `sudo apt-get install packagename` installs packagename
      * `sudo apt-get remove packagename` uninstalls packagename
      * `dpkg --get-selections` shows currently installed packages
      * `sudo add-apt-repository` adds a PPA (Ubuntu)
      * `sudo dpkg -i file.deb` installs `file.deb`
        * `sudo dpkg -r programname` uninstalls `programname`
    * Python:
      * <https://bootstrap.pypa.io/> Download these three, and run them with `python3 thing.py`
      * `pip install -U pip` installs `pip` (or updates)
      * `pip search pip` searches for `pip`
      * `virtualenv dirname` creates a virtual environment
        * `source dirname/bin/activate` connects to that venv
        * `deactivate` disconnects
        * `pip install pip==versionnumber -E dirname` installs pip at version number into venv
        * `pip freeze -E dirname > requirements.txt` exports venv info into shareable format
        * `pip install -r requirements.txt` installs from `requirements.txt`
        * `pip install -E dirname -r requirements.txt` imports venv from `requirements.txt`
    * [Node (NPM)](https://github.com/zacanger/cheat-sheets-etc/blob/master/npm.md)
* Basic commands:
  * `thing | less` views the output of `thing` in a paged format
    * `less filename` views that filename in a paged format
    * `G` jumps to the bottom of the view
    * `g` jumps to the top
    * `/` starts a search
    * `more` and `pg` are two earlier pagers
    * `pager` will start whichever one happens to be your default
    * `most` is a very different alternative, without the `vi`-like keybinds, which can also view binary files easily
  * `cat file` will print the contents of `file` to the terminal
  * `locate filename` will search (everywhere) for that filename
    * `sudo updatedb` will update locate's database (this is usually set as a daily cronjob by default)
  * `which programname` will show the location of an executable in your `PATH`
  * `grep query` will search _everything_ below `cwd` for that `query`
    * `grep query filename` will search only in the file `filename`
    * `command | grep query` will search the output of `command` for `query`
    * `ack` is a popular alternative to `grep`
    * `grep` itself has a few aliases usually built in: `egrep`, `fgrep`, maybe `vgrep`
    * `ag` (AG, The Silver Searcher) is _the_ grep to be using:
      * Less characters to type
      * Better highlighting, colour options, and defaults
      * _**MUCH**_ faster than `grep` (or `ack`)
      * Plus the guy who wrote it is just a really swell person
      * <https://github.com/ggreer/the_silver_searcher>
  * `ps -e` lists all running processes
    * `ps aux | sort -nk +4 | tail` lists the top ten processes by memory usage
    * `echo " "; ps -eo pcpu,pid,user,args | sort -rk1 | head -6 | column -t; echo " ";` lists the top five processes by CPU usage
  * `top` is an interactive system monitor
    * `htop` is a much nicer alternative:
      * colour
      * settings
      * much cleaner
      * more friendly keys
      * <http://hisham.hm/htop/>
    * `npm i -g vtop` will install a (javascript) version
      * very much simplified
      * nifty little graphs
  * `pkill processname` kills processname
    * `pkill -NUM name` kills name using the signal `NUM`
      * `pkill -9 foo` kills foo with `SIGKILL` (kill it dead, right now, do it!)
      * `pkill -15 foo` kills foo a little bit more gently, allowing time for cleanup, etc.
  * `renice process` stops the processes from hogging all resources and making computer lag
  * `command &` starts `command` in the background (so you don't need to waste a terminal on it)
    * `nohup command &` starts `command` in the background and keeps it running after you've logged off
  * `tar` is a mess. you could memorize all of its commands and flags, or...
    * you could use `unp`, which is in Python, and is as simple as typing `unp archivename.extension`
      * <https://github.com/mitsuhiko/unp>
    * you could use `atool` (which I recommend):
      * `aunpack foo.ext` unpacks the archive `foo.ext`
      * `als foo.ext` lists all its files
      * `apack` to make an archive
      * <http://www.nongnu.org/atool/>
  * `gpg -o outputname.gpg -c targetfile` to encrypt a file
    * `gpg -o outputname -d target.gpg` to decrypt a file
* Shell things (mostly Bash, but Zsh is _usually_ pretty compatible):
  * Directories:
    * `~/` means user's home
    * `./` means `cwd` (current working directory)
    * `../` is parent directory
    * `../../../../../` means the great-great-great-grandparent dierctory (Etc)
    * `*` means _all files in current directory_ (use caution, always)
  * Output redirects:
    * `|` is the _heart_ of UNIX.
      * `foo | bar` sends the output of `foo` to the input of `bar`
      * `foo | bar | quux > baz` sends the output of foo into bar, out to quux, and then writes that output to baz
    * `things > stuff` sends the output of `things` to a file, `stuff` (warning, this WILL overwrite the content of `stuff`)
      * `blah >> stuff` will _append_ the output of `blah` to `stuff` (so, it won't overwrite)
    * `tee` works like `|`, but it also writes its output to the terminal (it's a `T` shaped output!)
      * so `cat foo.txt | sort | uniq tee bar.txt` will `cat` all of `foo.txt`, sort it (alphabetically), remove duplicate lines, and send the output to both `bar.txt` and the terminal
  * `;`:
    * `one ; two` will execute `one` fully, then execute `2`
  * `&` will execute simultaneously
    * `&&` will only execute if the previous command was completed successfully
  * `||` only executes if the previous command completed _unsuccessfully_
  * `*` matches zero or more characters
    * `?` matches any one character
    * `[chars]` matches any characters inside brackets
    * `[a-z]` matches any characters inside that range
* Some more basic utilities:
  * `ifconfig` and `iwconfig` to configure network interfaces and _wireless_ network interfaces (specifically)
  * `ssh username@ipaddress` to connect to a server
    * `ssh -X username@ipaddress` to forward X (the display server) from the target to your current machine
  * `scp -r sourcefilename:user@ip targetfilename:targetuser@targetip` copies files/directories from one machine to another (recursively)
  * `rsync source target` copies changes between files/directories (very useful for syncing, can work remotely like ssh)
  * `ping address` checks if `address` (which can be an IP address or a domain) is available, and reports response times
  * `traceroute ipaddress` views the full network route to `ipaddress`
  * `iptables -L` shows firewall rules
  * `nmap localhost` shows open ports on `localhost`
  * `wget http://zacanger.com/` downloads `http://zacanger.com/`
    * `wget -c` completes a partial download
    * `-b` runs in the background
    * `-ftp-user=username --ftp-password=password ftp://example.com/directory/file` downloads over FTP
    * `--mirror` does a full-on mirroring download
    * `-i file` reads urls in `file` as a list to download
  * `netcat` listens for input from the network, and dumps to a file
  * `chown username file` changes the owner of a file (may need to be run as root, depending on the file)
    * `chown -R username directory` for directories, recursively
  * `chmod` changes file permissions
    * `chmod +x` makes a file executable
    * `chmod -x` makes it not executable
  * `users` shows current users
    * `adduser` adds a user
    * `usermod` changes user priveleges
    * `deluser` removes a user
  * `groups` shows all user groups
    * `groupadd` creates a new group
    * `groupmod` changes priveleges
    * `delgroup` removes group
  * `lsof` shows what processes are using what files
  * `diff` shows the differences between two files
  * `head -n NUM file` shows the top NUM lines of `file`
  * `tail -n NUM file` shows the last NUM lines of `file`
  * `md5sum file` and `md5deep directory` checksum file/all in directory
  * `sha1sum` and `sha1deep` are the same, but with sha1
  * `watch -d -n NUM command` calls `command` every NUM of seconds, shows difference in output
  * `time command` executes `command` and shows how long it took
  * `du -a directory | sort -n -r | less` shows files in directory from largest to smallest
  * `date` shows date and time
  * `dmidecode` shows motherboard info
    * `inxi` shows system info in a much more friendly format
      * <https://github.com/smxi/inxi>
  * `echo $HOSTNAME` shows current hosname
  * `lsb release -a` shows current (Linux) distro info
    * `cat /etc/issue` does similar
    * `uname -a` shows (Linux) system/kernel info
    * `lsmod` shows info about kernel modules
    * `modprobe` to configure kernel modules (_caution!_)
    * `printenv` shows environment variables
      * (so does `env` on most systems)
    * `lspci` shows PCI-connected hardware
      * `lsusb` shows USB-connected hardware
    * `dumpcap` dumps wireless card data
    * `dumpkeys` dumps keyboard driver data
* Git:
  * `git init` creates new repo (project)
  * `git config user.name "username"`
  * `git config user.email "email"`
  * `git clone target` clones to local
  * `git commit -m "message"` commits with `message`
  * `git status` shows curernt status
  * `git log` shows full log
  * `git pull`
  * `git push`
  * `git branch` creates
  * `git checkout branchname` switches to branchname
  * `git merge branchname` merges branchname
  * `pip install -U legit` will give you some _fantastic_ shortcuts
    * `legit help` and `legit install` to get started
  * `npm i -g gh` gives you some nifty Github specific commands (try `gh` to get started)
  * `hub` is Github's official client
    * Adds some Github-specific things to Git, like:
      * Pull Requests
      * Issues
      * Cloning from Github with the shorthand `hub clone user/repo`
      * <https://github.com/github/hub/releases>
      * or, `brew install hub` (on a Mac)
  * See my [.gitignore_global](https://github.com/zacanger/z/blob/master/.gitignore_global)
  * See my [.gitconfig](https://github.com/zacanger/z/blob/master/.gitconfig)
  * [Much, much more](https://github.com/zacanger/cheat-sheets-etc/blob/master/git.md)
* MySQL:
  * `help`
  * `show database` shows databases
    * `use databasename`
    * `show tables` shows schemas
    * `DROP DATABASE databasename`
    * `CREATE DATABASE databasename`
    * `CREATE USER username@hostname IDENTIFIED BY 'password';`
    * `select * from mysql.user;` shows users
    * `delete from mysql.user WHERE User='username';`
    * `mysqldump databasename > dumpfilename.txt` exports text with commands to rebuild all tables
    * `mysql -u username -p < dumpfilename.txt` restores from a dump
    * `mysqldump -u username -p --opt databasename > dumpfilename.sql` dumps the _entire_ database
    * `mysql -u username -p --database=databasename < dumpfilename.sql` restores from the full dump

