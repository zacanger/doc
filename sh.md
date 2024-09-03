sh

    # man pages
    1   User Commands
    2   System Calls
    3   C Library Functions
    4   Devices and Special Files
    5   File Formats and Conventions
    6   Games et. Al.
    7   Miscellanea
    8   System Administration tools and Deamons

    # File testing in sh
    -b filename     block special file
    -c filename     special character file
    -d dirname      check for directory existence
    -e filename     check for file existence
    -f filename     check for regular file existence not a directory
    -G filename     check if file exists and is owned by effective group ID.
    -g filename     true if file exists and is set-group-id.
    -k filename     sticky bit
    -L filename     symbolic link
    -O filename     true if file exists and is owned by the effective user id.
    -r filename     check if file is a readable
    -S filename     check if file is socket
    -s filename     check if file is nonzero size
    -u filename     check if file set-user-id bit is set
    -w filename     check if file is writable
    -x filename     check if file is executable
    -z <string> ... true if the length of the string is non-zero
    # example
    #!/usr/bin/env bash
    file=./file
    if [ ! -e "$file" ]; then
      echo "File does not exist"
    else
      echo "File exists"
    fi

    # Pipe stdout to multiple commands
    $ cat file.txt | tee >(pbcopy) >(do_stuff) >(do_more_stuff) | grep errors

    # Find and replace in multiple files
    $ ag -l <pattern> | xargs sed -i '' -E 's/<old>/<new>/g'

    # Delete a range of lines
    $ cat file.txt | sed -e '1,2d'

    # Manipulate columns with awk
    $ cat file.txt | awk '{$3=$1; gsub(/0[12345]_/, "", $3); $2="|"}{print}'

    # Check for value, fill in if it doesn't exist
    $ screen_width=${COLUMNS:-$(tput cols)}

    # Connect to ssh server
    ssh -i <path/to/file> <name>@<ip>
    # or with a `~/.ssh/configfile`
    ssh <Host>

    # list all open files for user
    lsof -u <ownername>

    # named pipes / inter-shell communication
    # create background procs, address them by name
    # creates physical file on system for use by any process
    # example code below passes `pipe` output to `cat` which
    # writes to `output`
    # anything passed to `pipe` here just goes through and out
    # the other end
    $ mkfifo pipe
    $ cat < pipe > output
    $ curl http://zacanger.com > pipe

    # follow logs as they grow
    $ tail -r <file>

    # execute a command in npm module dir
    npm ex <module name> <command> ...

    # dig (DNS lookup utility)
    $ dig @127.0.0.1 -p 5000 something.foo +short
    1.1.1.1

    # vim-like file manager
    vifm

    # better vim-like file manager
    ranger

    # system & gfx config tools, http://smxi.org/
    smxi
    sgfxi

    # boot manager: http://www.rodsbooks.com/refind
    refind

    # list all pci devices
    lspci

    # List all available devices. Useful to determine how to partition.
    lsblk

    # repair machines w/o root access, reset pid of process tree (lol docker), etc.
    chroot

    # manage audio players
    $ playerctl

    # pipe stderr to stdout
    # bash
    $ <command> 2>&1 /dev/null
    # POSIX sh
    $ <command> >/dev/null 2>&1

    # print multiline string
    cat << EOF
      oh my, such nice text
    EOF

    # detect if script is sourced
    if [ "$_" = "$0" ]
      then echo 'yup, script is directly called'
      else echo 'nope, script is not directly called'
    fi

    # Switch statement
    case $1 in
      "")         usage; exit 1 ;;
      -h|--help)  usage; exit ;;
      -l|--link)  link "$@" ;;
      *)          readonly name=$1 ;;
    esac

    # Format text to be &lt;80 chars
    $ fmt -80

    # Create random file name
    $ echo $RANDOM

