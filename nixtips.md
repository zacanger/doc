# More Nix-y Tips

### Manipulating command line instructions
replace "_str1_" by "_str2_" in previous command:
> ^_str1_^_str2_[^]
repeat event from 2 events ago:
> !-2
repeat most recent event starting with "_string_":
> !_string_
repeat most recent event containing "_string_":
> !?_string_[?]
repeat the entire command line typed so far:
> !#

### Directory Contents
Directory listing including non-printable chars
> ls -q *
list directory names (not their contents)
> ls -d *

List all entries in current directory that are files (not directories),
(alternatively use `find` with the `-depth` option):
> for i in *; do [ -f $i ] && echo $i; done
And inversely list only directories:
> for i in *; do [ -d $i ] && echo $i; done

### Directory Manipulation
Push current directory to directory stack:
> pushd .

Pop directory from directory stack:
> popd

### Files
Viewing file with line numbers:
> cat -n _filename_
"more" file starting at a certain linenumber:
> more +_linenumber_ _filename_
"more" file starting at a certain pattern:
> more +/_pattern_ _filename_
Rename all .htm files to .html in one go:
> rename .htm .html *.htm
Destroy a file:
> shred -uz _filename_

### Mail
Mail a file as plain text:
> mail -s "_subject_" _e-mail_address_ < _file_
Mail an attachement (if uuencode present and in path):
> uuencode attachment.txt | mail -s "_subject_" _e-mail_address_

### Arithmetics
Do some quick maths (whole numbers only):
> echo $((7*8+5))

### Sorting
To sort based on a section of each line in a file use the --key argument. For
instance to list countries in alphabetical order of name rather than their
country code:
> grep -v "^#" /usr/share/zoneinfo/iso3166.tab |sort --key=2.1

### Processes
Display current processes
> ps -ef|cut -c49-
Display the processes of user _userid_
> ps -fu _userid_
Show the processes started on _tty_
> ps -ft _tty_
Show the process with PID _pid_
> ps -fp _pid_
Restarting a process with PID _pid_:
> kill -HUP _pid_
Restarting sshd:
> kill -s HUP $(cat /var/run/sshd.pid)
Editing ssh settings:
> vi /etc/ssh/sshd_config
Changing (lowering) a running process' priority:
> renice +10 -p _pid_

### ftp
File permissions on target site:
> site mask 133
> site chmod 644 _filename_
Toggle interactive prompting of multiple arguments commands:
> prompt
Status of current connection:
> status

### sftp and ssh
Setting up passwordless login for sftp and ssh:
> ssh-keygen -t rsa
> ssh-copy-id -i ~/.ssh/id_rsa.pub username@remote_host
> sftp username@remote_host
Checking the last logins of the current user:
> last -i | grep $USER
Last logins of all users on a machine:
> last -i

### misc
Run one instruction as user _id_:
> su - _id_ -c "_instruction_"
Display terminal settings:
> stty -a
Display configuration of system variable:
> getconf CHILD_MAX
Set tab-stop interval to 4 in the terminal:
> tabs -4
To create a new user from the command line, log in as _root_
> adduser _username_
> passwd _username_
Look up the definition of a _word_ (in English) from the command line:
> curl dict://dict.org/d:_word_
How many cores does the system have:
> grep "model name" /proc/cpuinfo | wc -l

### tr
tr also works with these kind of constructions:
> tr '[:lower:]' '[:upper:]'
Forgetting the 's (single quotes) will cause problems if there is a file in
your current directory with the name: l, o, w, e, r, u, p or : Try `touch u &&
echo tr [:lower:] [:upper:]`
To remove CRs (^M) from ascii files ftp'd in binary mode from Windows to
Linux. An EOF (^Z) remains at the end of the file.
> tr -d '\r' < _file_with_CR_ > _file_without_CR_

### tar
Extract a single file from tar archive into the current directory, whitout
needing to know the full path (obviously only works if the filename is
unique):
> tar -xf _tarfile_ \--transform='s,.*/,,' $(tar -tf _tarfile_ | grep
_filename_)

### services / daemons
You need to be _root_ to run these instructions:

Status of all services:
> service --status-all
Restart a service (for example the network service) (similar with start or
stop):
> service network --full-restart
List all services settings for all runlevels:
> chkconfig --list
Example: turn mysql deamon on for runlevels 2 to 5:
> chkconfig mysqld on

With systemd
Status of all daemons:
> systemctl
Restart the http daemon (stop and start also work):
> systemctl restart httpd.service
Turn the http daemon on in default runlevel:
> systemctl enable httpd.service
Stopping and starting gnome:
> gdm-sto
> gdm-start

### yum
Run _yum_ instructions as _root_:
Clean up packages downloaded by yum:
> yum clean packages
Exclude a package from being updated, handy if a package is causing a missing
dependency error:
> yum update --exclude=_package_
Example to update everything except the kernel:
> yum update --exclude=kernel*
Search for a package:
> yum search _word_

### FFmpeg and mencoder (Media Conversions)
Convert a .mov file to a .flv file (-s optional resize):
> ffmpeg -i _input_filename_.mov -s _width_x_height_ _output_filename_.flv
Cut a section from an MP3 sound file (-t = total length of clip):
> ffmpeg -i _input_filename_.mp3 -ss _HH:MM:SS_ -t _HH:MM:SS_
_output_filename_.mp3
Rotate a video clip:
> mencoder -vf _rotate=1_ -ovc lavc -oac copy -o _output.avi_ _input.avi_
Rotate right: _rotate=1_, rotate left: _rotate=2_
Extract sound from a .WebM video clip:
> ffmpeg -i _input_filename.webm_ -vn -acodec copy _output_filename.ogg_
Remove sound from a video file:
> ffmpeg -i _input_filename.webm_ -an _output_filename.webm_
Convert an image to a PDF document (needs `imagemagick` installed):
> convert _imagefile_ _docname_.pdf

## Symlinks
Sometimes you're not sure where files might be. Maybe they need to be in more than one place;  
maybe it'd just be convenient if they were. That's what symlinks are for. (Same concept as  
shortcuts on a Microsoft machine, except you can do a lot more stuff with UNIX's links.)  
The command you need to know is `ln`. You'll almost definitely want the `-s` (symbolic)  
flag. Example: `ln -s /home/z/Dropbox/skool/extras/examples /home/z`
