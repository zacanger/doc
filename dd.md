The real dd command 


The basic command is structured as follows:

dd if=<source> of=<target> bs=<byte size>(usually some power of 2, not less than 512 bytes(ie, 512, 1024, 2048, 4096, 8192, 16384, but can be any number.) skip= seek= conv=<conversion>.

Source is the data being read. Target is where the data gets written. If you mess up, and accidentally reverse the source and target, you can wipe out a lot of data.

Examples::

Copy one hard disk partition to another hard disk:

dd if=/dev/sda2 of=/dev/sdb2 bs=4096 conv=notrunc,noerror

sda2, sdb2 are partitions. You want to copy sda2 to sdb2. If sdb2 doesn't exist, dd will start at the beginning of the disk, and create it. Be careful with order of if and of. You can write a blank disk to a good disk if you get confused.

Make an iso image of a CD:

dd if=/dev/hdc of=/home/sam/mycd.iso bs=2048 conv=notrunc

CD sectors are 2048 bytes, so this copies sector for sector. The result will be a hard disk image file of the CD. You can use "chmod a+rwx mycd.iso" to make the image writable. You can mount the image with "mkdir /mnt/mycd", this line in fstab: "/home/sam/mycd.iso /mnt/mycd iso9660 rw,user,noauto 0 0", save fstab, "mount -o loop /mnt/mycd". Then the file system will be viewable as files and directories in the directory /mnt/mycd. You can edit the image as you wish, and the new file will be "/home/sam/mycd.iso" dd does not write to CD's. You need to use a burning utility, or the cdrdao command

Copy a floppy disk:

dd if=/dev/fd0 of=/home/sam/floppy.image bs=2x80x18b conv=notrunc

or

dd if=/dev/fd0 of=/home/sam/floppy.image conv=notrunc

The 18b specifies 18 sectors of 512 bytes, the 2x multiplies the sector size by the number of heads, and the 80x is for the cylinders--a total of 1474560 bytes. This issues a single 1474560-byte read request to /dev/fd0 and a single 1474560 write request to /home/sam/floppy.image. This makes a hard drive image of the floppy, with bootable info intact. The second example uses default "bs=" of 512, which is the sector size of a floppy.

To format a series of floppies: Take one empty, never been used, formatted floppy; and:

dd if=/dev/fd0 of=/home/sam/floppy.bin

and make a hard disk image of a new formatted floppy, then:

load one of the floppies you want to format into the floppy drive, and:

dd if=/home/sam/floppy.bin of=/dev/fd0

This floppy will end up exactly like the never been used floppy you started with

To make a trusted DOS boot floppy

Get DR DOS 7 from http://www.bootdisk.com

You have to use Windows to make the boot disk.

copy the new boot disk:

dd if=/dev/fd0 of=/home/sam/floppy.bin

Open the image in a hex editor and change all references of "DRIVESPACE" to "XXXX.XXXXX" and "DOUBLESPACE" to "XXXXX.XXXXX". Change all references of "C:" to "A:".

This is now a trusted boot floppy. Trusted boot floppies are used to insure no writes are made to the hard drive on a floppy boot.

Copy a hard drive image of a floppy to a floppy:

dd if=/home/sam/floppy.image of=fd0 bs=2x80x18b conv=notrunc

Copy just the MBR and boot sector of a floppy to hard drive image:

dd if=/dev/fd0 of=/home/sam/MBRboot.image bs=512 count=2

This copies the first 2 sectors of the floppy

Fix a floppy hacked by a DRM trojan.

Insert the floppy

dd if=/dev/null of=/dev/fd0 conv=notrunc

dd if=/home/sam/floppy.image of=/dev/fd0 conv=notrunc,noerror

Normally, writing null to the first two sectors of a floppy renders the floppy totally unusable. It cannot even be formatted after that. Thanks to the image of the new, unused floppy, floppy.image, you can write the first two sectors back properly.

Rescue an unreadable floppy.

ddrescue if=/dev/fd0 of=/home/sam/rescue.image bs=1440k conv=notrunc,noerror

with a new floppy in the drive

dd if=/home/sam/rescue.image of=/dev/fd0 bs=512 skip=2 seek=2 conv=notrunc,noerror

Now the new floppy should be readable

This method works similarly well with damaged CD's and DVD's. However, you must mount the resulting .iso image as a loop device and copy all the data that way.

ddrescue if=/dev/sr0 of=/home/sam/rescue.iso bs=2048 conv=notrunc,noerror

Make the following line in /etc/fstab.

/home/sam/rescue.iso /mnt/rescue iso9660 rw,user,noauto 0 0

Execute the following command.

mkdir /mnt/rescue

This makes the mount point you put in /etc/fstab.

Execute the following command.

mount -o loop /mnt/rescue

now all the salvagable data will be in the directory

/mnt/rescue

You can copy it to a new cd.

Echoes "I love Avril" vertically.

echo -n "I love Avril" | dd cbs=1 conv=unblock 2> /dev/null


Cloning an entire hard disk:

dd if=/dev/sda of=/dev/sdb conv=notrunc,noerror

In this example, sda is the source. sdb is the target. Do not reverse the intended source and target. Surprisingly many people do. notrunc means to not truncate. noerror means to keep going if there is an error. Normally dd stops at any error. if you have a question about a hard drive on whether or not it works, you can try to use it as the source drive for the dd command. You should get an error if it is not working. target drives need to be really messed up to give an error in dd.

Copy MBR only of a hard drive:

dd if=/dev/sda of=/home/sam/MBR.image bs=446 count=1

this will copy the first 446 bytes of the hard drive to a file. If you haven't already guessed, reversing the objects of if and of, in the dd command line reverses the direction of the write.

Wipe a hard drive of all data (you would want to boot from a cd to do this) 

http://www.efense.com/helix is a good boot cd

The helix boot environment contains the DoD version of dd called dcfldd. It works the same way, but is has a progress bar.

dd if=/dev/zero of=/dev/sda conv=notrunc

This is useful for getting rid of viruses, DRM trojans and the like.

To view your virtual memory

dd if=/proc/kcore | hexdump -C | less

dumps one screen at a time to the terminal

What filesystems are installed

dd if=/proc/filesystems | hexdump -C | less

all loaded modules

dd if=/proc/kallsyms | hexdump -C | less

interrupt table

dd if=/proc/interrupts | hexdump -C | less

How many seconds has the system been up

dd if=/proc/uptime | hexdump -C | less

partitions and sizes in kb

dd if=/proc/partitions | hexdump -C | less

Memory stats

dd if=/proc/meminfo | hexdump -C | less

there are alot of other things in /proc. I'm not going to go through what they all for. The above are some of the more useful ones.

It would be useful, at this time, to interject a tip:

I have several machines, but on the one I use a lot I have two SATA hard drives. They are exactly the same. Before I do anything dangerous, I boot from the helix CD, run 

dcfldd if=/dev/sda of=/dev/sdb bs=4096 conv=notrunc,noerror

and copy my present working sda drive system to the sdb drive. If I wreck the installation on sda, I just boot with the helix cd and 

dcfldd if=/dev/sdb of=/dev/sda bs=4096 conv=notrunc,noerror

Please note: bs=4096 works fast for machines with at least 128 MB of ram. Dd uses a lot of buffers. At bs=4096, on modern machines, the optimal transfer rate is reached for hard drives.

To make a file of 100 random bytes

dd if=/dev/urandom of=/home/sam/myrandom bs=1 count=100

Here, urandom is the linux random byte device. myrandom is a file. Byte size equals 1 and there are 100 of them. Gpg requires a random seed to generate keys. Generating a file of say 4096 random bytes, which can be passed to Gpg, will allow a truly random seed.

Write random data over a file before deleting it:

first do an ls -l to find filesize. In this case it is 3769

ls -l afile
-rw------- ... 3769 Nov 2 13:41 <filename>

dd if=/dev/urandom of=afile bs=3769 count=1 conv=notrunc

This will write random characters over the entire file.

Copy a disk partition to a file on a different partition. Do not copy a partition to the same partition.

dd if=/dev/sdb2 of=/home/sam/partition.image bs=4096 conv=notrunc,noerror

This will make a file that is an exact duplicate of the sdb2 partition. You can substitue hdb, sda, hda, or whatever the disk is called.

Restore a disk partition from an image file.

dd if=/home/sam/partition.image of=/dev/sdb2 bs=4096 conv=notrunc,noerror

This way you can get a bazonga hard drive and partition it so you can back up your root partition. If you mess up your root partition, you just boot from the helix cd and restore the image.

To covert a file to all uppercase:

dd if=filename of=filename conv=ucase

Copy ram memory to a file:

dd if=/dev/mem of=/home/sam/mem.bin bs=1024


The device /dev/mem is your system memory. You can actually copy any block or character device to a file with dd. Memory capture on a fast system, with bs=1024 takes about 60 seconds. Copying a 120 GB HDD takes about an hour. Copying a CD to hard drive takes about 10 minutes. Copying a floppy to a hard drive takes about 2 minutes. With dd, your floppy drive images will not change at all. If you have a bootable DOS diskette, and you save it to your HDD as an image file, when you restore that image to another floppy it will be bootable. dd is an excellent way to make an image of MS Windows XP install CD's. When you make a copy of such a cd, there is one sector that is of nonstandard length. It is the last sector. dd doesn't pad this sector, making the copy indistinguishable from the original. If you burn the CD using cdrdao, the resulting disk will be an absolutely exact copy of the original.

dd will print to the terminal window if you omit the “of=” part.

dd if=/home/sam/myfile

will print the file myfile to the terminal window.

If you are just curious about what might be on you disk drive, or what an MBR looks like, or maybe what is at the very end of your disk:

dd if=/dev/sda count=1 | hexdump -C

Will show you sector 1, or the MBR. There is the beginning of the loader code and the partition table in there. To see the end of the disk you have to know the total number of sectors for the disk, and the disk has to be set up with Maximum Addressable Sector equal to Maximum Native Address. The helix CD has a utility to set this correctly. In the dd command your seek value will be one less than MNA of the disk.

for a 120 GB Seagate SATA drives

dd if=/dev/sda of=home/sam/myfile skip=234441646

default bs=512, so this reads sector for sector, and writes the last sector to myfile.

Disks, even though there is LBA addressing now, still secretly are read in sectors, cylinders, and heads. There are 63 sectors per cylinder, and 255 heads per cylinder. Then there is a total cylinder count for the disk. You multiply out 512x63x255=bytes per cylinder. 63x255=sectors per cylinder. With dd you usually want to work with sectors per cylinder. With 234441647 total sectors, and 16065 sectors per cylinder, you get some trailing sectors which do not make up an entire cylinder, 14593.317584812. This leaves you with 5102 sectors which cannot be partitioned because to be in a partition you have to be a whole cylinder. Part cylinders do not count. It's like having part of a person. That doesn't really count as a person. So, what happens to these sectors? They become surplus sectors after the last partition. This a perfect place for sneaky programs to play, because you can't ordinarily read in there with an operating system. But, dd can.

It is really a good idea to check for anything writing to surplus sectors. For our Seagate 120 GB drive you subtract total sectors(234441647)-(5102) which don't make up a whole cylinder=234436545 partitionable sectors. Remember, native HDD sectors are 512, or 1b. If you don't specify “bs” in dd it defaults to 512.

dd if=/dev/sda of=/home/sam/myfile skip=234436545

this writes the last 5102 sectors to myfile. Launch “mc” to view the file. I swear, half the time Windows XP has left a weird, mutated MBR there. It like marks the disk for life that XP was there.

If there is something in there, you do not need it for anything. In this case you would write over it with random characters. Many digital rights management programs use surplus sectors to operate from, while enforcing DRM. These trojans, which are corporate trojans, are meant to enforce the security measures in copyrighted software. There are other various means to conceal such a trojan. One of these is a hidden partition. There is an undocumented type of partition which is called hidden. It is not visible to any operating system.

dd if=/dev/urandom of=/dev/sda bs=512 seek=234436545

Will overwrite the 5102 surplus sectors on our 120 GB Seagate drive.

If you want to check out some random area of the disk:

dd if=/dev/sda of=/home/sam/myfile bs=4096 skip=2000 count=1000

will give you 8,000 sectors in myfile, after the first 16,000 sectors. You can open that file with a hex editor, edit some of it, and write the edited part back to disk:

dd if=/home/sam/myfile of=/dev/sda bs=4096 seek=2000 count=1000

So there you got yourself a disk editor. It's not the best, but it works.

You can make a boot floppy: with the boot.img file, which is pretty easy to get. You just need a program that will literally start writing at sector 1.

dd if=boot.img of=/dev/fd0 bs=1440k

This makes a bootable disk you can add stuff to.


If you want to make a partition image on another machine:

on source machine:

dd if=/dev/hda bs=16065b | netcat targethost-IP 1234

on target machine:

netcat -l -p 1234 | dd of=/dev/hdc bs=16065b

Netcat is a program, available by default, on almost every linux installation. It is like a swiss army knife of networking. In the preceding example netcat and dd are piped to one another. One of the functions of the linux kernel is to make pipes. The pipe character looks like two little lines on top of one another, both vertical. Here is how this command behaves:

On the source machine dd is told to read /dev/hda with a byte size which is kind of weird. This byte size is a cylinder. bs=16065b equals one cylinder on an LBA drive. Ok, then the dd command is piped to netcat, which takes as its arguments the IP address of the target(like 192.168.0.1, or any IP address with an open port) and what port you want to use(1234). Don't hit enter yet. Type the command for the target machine first, hit enter on the target machine, hit enter on the source machine. Now the bit stream copy will take place. This is kind of how Norton Ghost works to image a drive to another machine. All you have to do is boot both machines with the helix CD, and don't confuse the source machine with the target machine.

Use rsh(remote shell) to get the remote disk image. This is for when you want to use rsh, and read a drive or partition from a remote machine.

rsh 192.168.xx.yy "dd if=/dev/sda ibs=4096 conv=notrunc,noerror" | dd of=/dev/sda obs=4096


the IP is the IP of the remote machine. the dd command in quotes is to specify this command is to run on the remote host. You need the quotes. The pipe is made on the machine you are on. This pipes the dd output command to the dd input command, but the output command is run on your machine.

Use rsh to send the remote disk image. This is for when you want to use rsh, and write a drive or partition to a remote machine.

dd if=/dev/sda ibs=4096 conv=notrunc,noerror | (rsh 192.168.xx.yy dd of=/dev/sda obs=4096)

Putting parentheses around the remote command creates a subshell. In this instance, the only purpose of such is to cause the desired effect.

To use ssh, replace "rsh" with "ssh"

Ok, say you want to find out if your girlfriend or wife is cheating on you, having cyber sex, or just basically misbehaving with her computer. Even if the computer is secured with a password, you can boot with the:

http://www.efense.com/helix

CD and search the entire drive partition for text strings:

dd if=/dev/sda2 bs=16065 | hexdump -C | grep 'I really don't love him anymore.'

Will search the whole drive partition for the text string specified between the single quotes. Searching an entire disk partition several times can be quite tedious. This particular command string prints the search results to the screen, with the offset where it is located in the partition. dd works in the decimal system. Disk offsets work in hexidecimal.
Say you found that text string in your partition at offset 020d0d90. You convert that to decimal with one of the many calculators found in linux. This is decimal offset 34409872. Dividing by 512b per sector we get 67206.78125. now we know, to read the rest of what ever it is, and these numbers are just guestimates:

dd if=/dev/sda2 bs=16065 skip=2140 count=3 | less

This will put the output to the screen so you don't accidentally write a file over what you want to read. Piping dd to less will give you one screen at a time of output. With this method you search all the deleted files, any chat activity, and emails. It works no matter what security is being employed on the machine. It works with NTFS, ext2, ext3, reiserfs, swap, and FAT partitions. The helix CD is not fussy, and neither is the dd command.

On a related note, you can write the system memory to a CD. This is useful for documenting memory contents without contaminating the HDD. I recommend using a CD-RW so you can practice a little. This doesn't involve dd, but it's cool.

cdrecord dev=ATAPI:0,1,0 -raw tsize=700000000 driveropts=burnfree /dev/mem

to find the cdwriter

cdrecord -scanbus=ATAPI

This method records raw, so you have to do a 

dd if=/dev/hdd | less 

to view the recorded memory. Searching the recorded memory is as above

dd if=/dev/hdd | hexdump -C | grep 'string'

string is any ascii sequence, hex sequence (must be separated with a space: '55<space>aa<space>09' searches for the hex string '55aa09'), list:

'[[:alnum:]]' any alphanumeric characters
'[[:alpha:]]' any alpha character
'[[:digit:]]' any numeric character
'[[:blank:]]' tabs and spaces
'[[:lower:]]' any lower case alpha characters
'[[:upper:]]' any uppercase alpha character
'[[:cntrl:]]' ASCII characters 000 thru 037, and 177 octal
'[[:graph:]]' [:alnum:] and [:punct:]
'[[:punct:]]' any punctuation character
` ! ' # $ % ' ( ) * + - . / : ; < = > ? @ [ \ ] ^ _ { | } ~
'[[:space:]]' tab, newline, vertical tab, form feed, carriage return, and space
'[[:xdigit:]]' any hex digit
ranges('[a-d]' = any, or all abcd, '[0-9]' = any, or all 0123456789)

You can back up your MBR

dd if=/dev/sda of=mbr.bin count=1

Put this on a floppy you make with

dd if=boot.img of=/dev/fd0

Along with dd. Boot from the floppy and

dd if=mbr.bin of=/dev/sda count=1

Will restore the MBR.

I back up all my floppies to HDD. Floppies don't last forever, so I do

dd if=/dev/fd0 of=/home/sam/floppies/backup.bin conv=notrunc

If my floppy fails, I can make unlimited copies

dd if=/home/sam/floppies/backup.bin of=/dev/fd0 conv=notrunc

Here is a command line to read your BIOS, and interfaces

dd if=/dev/mem bs=1k skip=768 count=256 2>/dev/null | strings -n 8


OPERANDS
The following operands are supported:

if=file

Specifies the input path. Standard input is the default. 

of=file

Specifies the output path. Standard output is the default. If the seek=expr conversion is not also specified, the output file will be truncated before the copy begins, unless conv=notrunc is specified. If seek=expr is specified, but conv=notrunc is not, the effect of the copy will be to preserve the blocks in the output file over which dd seeks, but no other portion of the output file will be preserved. (If the size of the seek plus the size of the input file is less than the previous size of the output file, the output file is shortened by the copy.) 

ibs=n

Specifies the input block size in n bytes (default is 512). 

obs=n

Specifies the output block size in n bytes (default is 512). 

bs=n

Sets both input and output block sizes to n bytes, superseding ibs= and obs=. If no conversion other than sync, noerror, and notrunc is specified, each input block is copied to the output as a single block without aggregating short blocks. 

cbs=n

Specifies the conversion block size for block and unblock in bytes by n (default is 0). If cbs= is omitted or given a value of 0, using block or unblock produces unspecified results.
This option is used only if ASCII or EBCDIC conversion is specified. For the ascii and asciib operands, the input is handled as described for the unblock operand except that characters are converted to ASCII before the trailing SPACE characters are deleted. For the ebcdic, ebcdicb, ibm, and ibmb operands, the input is handled as described for the block operand except that the characters are converted to EBCDIC or IBM EBCDIC after the trailing SPACE characters are added. 

files=n 

Copies and concatenates n input files before terminating (makes sense only where input is a magnetic tape or similar device). 

skip=n 

Skips n input blocks (using the specified input block size) before starting to copy. On seekable files, the implementation reads the blocks or seeks past them. On non-seekable files, the blocks are read and the data is discarded. 

iseek=n 

Seeks n blocks from beginning of input file before copying (appropriate for disk files, where skip can be incredibly slow). 

oseek=n 

Seeks n blocks from beginning of output file before copying. 

seek=n 

Skips n blocks (using the specified output block size) from beginning of output file before copying. On non-seekable files, existing blocks are read and space from the current end-of-file to the specified offset, if any, is filled with null bytes. On seekable files, the implementation seeks to the specified offset or reads the blocks as described for non-seekable files. 

count=n 

Copies only n input blocks. 

conv=value[,value. . . ] 

Where values are comma-separated symbols from the following list: 

ascii 

Converts EBCDIC to ASCII. 

asciib 

Converts EBCDIC to ASCII using BSD-compatible character translations. 

ebcdic 

Converts ASCII to EBCDIC. If converting fixed-length ASCII records without NEWLINEs, sets up a pipeline with dd conv=unblock beforehand. 

ebcdicb 

Converts ASCII to EBCDIC using BSD-compatible character translations. If converting fixed-length ASCII records without NEWLINEs, sets up a pipeline with dd conv=unblock beforehand. 

ibm 

Slightly different map of ASCII to EBCDIC. If converting fixed-length ASCII records without NEWLINEs, sets up a pipeline with dd conv=unblock beforehand. 

ibmb 

Slightly different map of ASCII to EBCDIC using BSD-compatible character translations. If converting fixed-length ASCII records without NEWLINEs, sets up a pipeline with dd conv=unblock beforehand. 

The ascii (or asciib), ebcdic (or ebcdicb), and ibm (or ibmb) values are mutually exclusive.

block 

Treats the input as a sequence of NEWLINE-terminated or EOF-terminated variable-length records independent of the input block boundaries. Each record is converted to a record with a fixed length specified by the conversion block size. Any NEWLINE character is removed from the input line. SPACE characters are appended to lines that are shorter than their conversion block size to fill the block. Lines that are longer than the conversion block size are truncated to the largest number of characters that will fit into that size. The number of truncated lines is reported. 

unblock 

Converts fixed-length records to variable length. Reads a number of bytes equal to the conversion block size (or the number of bytes remaining in the input, if less than the conversion block size), delete all trailing SPACE characters, and append a NEWLINE character. 
The block and unblock values are mutually exclusive.

lcase 

Maps upper-case characters specified by the LC_CTYPE keyword tolower to the corresponding lower-case character. Characters for which no mapping is specified are not modified by this conversion. 

ucase 

Maps lower-case characters specified by the LC_CTYPE keyword toupper to the corresponding upper-case character. Characters for which no mapping is specified are not modified by this conversion. 
The lcase and ucase symbols are mutually exclusive.

swab 

Swaps every pair of input bytes. If the current input record is an odd number of bytes, the last byte in the input record is ignored. 

noerror 

Does not stop processing on an input error. When an input error occurs, a diagnostic message is written on standard error, followed by the current input and output block counts in the same format as used at completion. If the sync conversion is specified, the missing input is replaced with null bytes and processed normally. Otherwise, the input block will be omitted from the output. 


notrunc 

Does not truncate the output file. Preserves blocks in the output file not explicitly written by this invocation of dd. (See also the preceding of=file operand.) 

sync 

Pads every input block to the size of the ibs= buffer, appending null bytes. (If either block or unblock is also specified, appends SPACE characters, rather than null bytes.) 
If operands other than conv= are specified more than once, the last specified operand=value is used.
For the bs=, cbs=, ibs=, and obs= operands, the application must supply an expression specifying a size in bytes. The expression, expr, can be:

a positive decimal number
a positive decimal number followed by k, specifying multiplication by 1024
a positive decimal number followed by M, specifying multiplication by 1024*1024
a positive decimal number followed by b, specifying multiplication by 512
two or more positive decimal numbers (with or without k or b) separated by x, specifying the product of the indicated values.
