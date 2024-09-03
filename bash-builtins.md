The scene: you've just run `sudo rm -rf --no-preserve-root /`.

You're an idiot.

Let's try to recover from this.

`echo *` LOOK! WE STILL HAVE AN LS, SORT OF! Let's make it better.

`printf '%s\n' ${1:+${1%/}/}*`

NIIIIIIICE. That's really annoying to type, though.

`echo 'ls() { printf '%s\n' ${1:+${1%/}/}*; }' >> utils.sh`

`. ./utils.sh`

Now, `ls` will act kinda like `ls`!

`type` still exists! This will be useful later on, I promise.

What about `cat`?

`(while read line; do echo "$line"; done) < stuff.txt`

To find executables: `for file in /*; do executable $file; done`.

`executable () { if [[ ( ! -d $1 ) &&  ( ! -h $1 ) && -x $1 ]] ; then echo "$1"; fi }`

Want to actually lock yourself out of the basically-dead computer?

`echo 1 > /proc/sys/kernel/sysrq` `echo "b" > /proc/sysrq-trigger`.

We don't have a text editor anymore, I guess, but we _do_ have

`(IFS=$'\n';while read line;do echo "$line";done) < inputfile` for reading, and

`(IFS=$'\n';while read line;do echo "$line";done) > outputfile` for creating a file!

(Ending with the usual Ctrl-D should still work.)

If you're still stuck in a system that you really need to work right now, go to
http://eusebeia.dyndns.org/bashcp on some other system and follow through to
get yourself BusyBox set up. It will give you everything you need. Also check out
http://fakeguido.blogspot.com/2010/08/rescuing-hosed-system-using-only-bash.html
for more details on this.

