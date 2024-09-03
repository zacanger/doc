# UNIX in Five Seconds

* This is an extremely short quick introduction to UNIX.
* This introduction assumes you know how to use computers and how to adopt the examples for your needs.
* Further, this introduction assumes you are familiar with operating systems in general.

## Basics

* Everything in UNIX is a file.
* There are regular files, directories, pipes, sockets, devices, soft links and more kinds of files.
* A directory can contain many files of different kinds.

## Concepts

### Permissions

Every file object has 12 bits for permissions:

* The _special bits_ SetUID (4), SetGID (2), Sticky (1)
* Read (4), Write (2), Execute (1) each for the **u**ser that owns the file, the associated **g**roup and **o**thers

#### Binary Permission Notationset uidset gidstickyuid readuid writeuid executegid readgid writegid executereadwriteexecute

400020001000040002000100004000200010000400020001

#### Symbolic Permission Notation

* `u` Owning User
* `g` Associated Group
* `o` Others
* `a` All (Explicit, ignoring umask)
* ` ` All (Implicit, respecting umask)

* `r` Read
* `w` Write
* `x` Execute
* `s` SetUID / SetGID
* `t` Sticky

Examples: a=rwx u=rw u+s

#### Permission Notation of `ls`

The output of `ls` shows special bits and executable bits in the same column.

* SetUID: user
* SetGID: group
* Sticky: other

Character Special Executable

-nono

xnoyes

S o. Tyesno

s o. tyesyes

#### The UMASK

The UMASK is a process-bound property with a permission mask for newly created files.
The bits that are set in UMASK will be deleted from the permissions of a newly created file. (NAND).
Files are created with 0666, directories with 0777 permission.

## Commands

### File Commands

**Create / update a file**
> `touch file`

**Copy a file**
> `cp name nameOfCopy`
> `cp name destinationDirectory`

**Rename or move a file**
> `mv oldName newName`
> `mv name destinationDirectory`
> If used within the same filesystem, the `mv` command only changes the hardlink.

**Delete a file**
> `rm name`
> This command only removes one hardlink ("unlink").
> A file (including its inode) is only freed by the removal of its very last hardlink.

**Show a regular file's contents**
> * `cat name`
> * `more name`
> * `less name`
> * `view name`

**Copying data from a file (also devices)**
> `dd if=infile of=outfile`

**Concatenating files**
> `cat files...`

**Delete contents of files**
> `shred files...`

### Commands for Directories

**Create a directory**
> `mkdir dirName`

**Show a directory's contents**
> Current directory: `ls`
> Specified directory: `ls dirName`
> Show hidden files: `ls -a`
> Detailed listing: `ls -l`
> Show a directory itself, not its content: `ls -d`

**Print working directory**
> `pwd`

**Change working directory**
> `cd dirName`
> Parent directory: `cd ..`
> Root directory: `cd /`
> Home directory: `cd ~` oder einfach nur `cd`

**Delete a directory**
> `rmdir dirName` (Directory must be empty)
> `rm -r dirName` (deletes with content, **Caution!**)

### Permissions

**Change owner**
> `chown newOwner files`

**Change group**
> Of a file: `chgrp newGroup files`
> Of the current user: `newgrp newGroup`

**Change file permissions**
> `chmod bits files`

### Extended Permissions (ACLs)

**Activating ACLs**
> mount -o remount,acl mountpoint

**Giving a user additional permissions**
> setfacl -m user:username:permissionsfiles...

**Giving a group additional permissions**
> setfacl -m group:groupname:permissionsfiles...

**Creating a Default-ACL for newly created files**
> setfacl -m default:user|group:userorgroupname:permissionsdirs...

**Modifying the permission mask**
> setfacl -m mask::permissions

### Processes and Job-Control

**End a process**
> * Process with tty: Ctrl-C drücken
> * `kill processNumber`
> * Process doesn't respond: `kill -9 processNumber`

**List processes**
> Own / Subshells: `ps`
> Jobs of current shell: `jobs`
> All: `ps -aef`

**Start process as background job**
> `cmd &`

**Suspend current process / job**
> Ctrl-Z

**Resume suspended process**
> `fg`

**Continue process in background**
> 1.  Ctrl-Z
> 1.  `bg`

**Suspend STDIN**
> Ctrl-S

**Resume STDIN**
> Ctrl-Q

**Send EOF to STDIN**
> Ctrl-D

### STDOUT, STDIN and Pipes

**Redirection**
> STDIN: `cmd  STDOUT: `cmd >name`
> STDERR: `cmd 2>name`
> STDOUT a. STDERR to the same file: `cmd >name 2>&1`

**Use a command's output as input for a second command**
> `cmd1 | cmd2`

**Use a file as a command's input**
> `cat name | cmd`

**Use a command's output as arguments for a second command**
> Some arguments: `cmd2 \`cmd1\``
> Many arguments: `cmd1 | xargs cmd2`

**Send EOF to STDIN**
> Ctrl-D

### Commands for archives and compressed files

**gzip**
> Compress: `gzip name` Decompress: `ungzip name`

**bzip2**
> Compress: `bzip2 name` Decompress: `bunzip2 name`

**tar-archives**
> Create: `tar cvf archiveName.tar dir`
> List contents: `tar tvf archiveName.tar`
> Extract: `tar xvf archiveName.tar`
> Automatically invoke gzip using z: `tar czvf / tzvf / xzvf`
> Automatically invoke bzip2 using j: `tar cjvf / tjvf / xjvf`

**jar-archives**
> Like tar-archives, options j and z do not apply.

### Burn CDs

**Burn a directory on CD**
> 1. `mkisofs -R -J -o /tmp/image.iso dir`
> 1. `cdrecord speed=16 dev=0,1,0 /tmp/image.iso`
> 1. `rm /tmp/image.iso`

**Burn a directory on CD-RW**
> 1. `mkisofs -R -J -o /tmp/image.iso dir`
> 1. `cdrecord speed=16 dev=0,1,0 blank=all /tmp/image.iso`
> 1. `rm /tmp/image.iso`

**Test iso-image before burning**
> 1. `mkdir /tmp/image`
> 1. `mount -o loop -t iso9660 /tmp/image.iso /tmp/image`
> 1. `ls /tmp/image`
> 1. `umount /tmp/image`
> 1. `rmdir /tmp/image`

