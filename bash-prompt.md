# Bash Prompt Customization

* Prompts:
  * PS1: Default interactive
  * PS2: Continuation interactive
  * PS3: Select (builtin)
  * PS4: `set -x` uses this to prefix tracing output

| Prompt | Description | Example | Result |
-----------------------------------------
| \a    | ASCII bell character (07)	| \a$	$ | (and beep)
| \d  	| Date in “Weekday Month Date” format	| \d$ |	Wed Mar 08$
| \e  	| ASCII escape character (033 |
| \h  	| Hostname up to the first `.’	| \h$	| beebo$
| \H  	| Hostname	| \H$	| beebo.example.com$
| \j  	| Number of jobs currently managed by the shell	| \j$	| 0$
| \l  	| Basename of the shell’s terminal device name	| \l$	| 1$
| \n  	| Newline	| \d\n\h$	| Wed Mar 08 <newline>beebo$
| \r  	| Carriage return	| \d\r\h$	| beebo$r 08
| \s  	| Shell name, basename of $0 (portion following final slash) | \s$	| bash$
| \t  	| Current time in 24-hour HH:MM:SS format	| \t$	| 07:24:57$
| \T  	| Current time in 12-hour HH:MM:SS format	| \T$	| 07:24:57$
| \@  	| Current time in 12-hour am/pm format	| \@$	| 07:25 AM$
| \u  	| Username of the current user	| \u$	| david$
| \v  	| Version of bash (e.g., 2.00)	| \v$	| 3.1$
| \V  	| Release of bash, version + patchlevel (e.g., 2.00.0)	| \V$	| 3.1.5$
| \w  	| Current working directory	| \w$	| ~/articles/bash-prompts$
| \W  	| Basename of the current working directory	| \W$	| bash-prompts$
| \!  	| History number of this command	| \!$	| 537$
| \#  	| Command number of this command	| \#$	| 40$
| \$  	| If the effective UID is 0, a #, otherwise a $	| \$	| $ or # as root
| \nnn	| Character corresponding to the octal number nnn	| \141$	| a$
| \\  	| Backslash	| \\$	| \$
| \[  	| Begin non-printing character sequence; to embed control sequence into prompt, for example
| \]  	| End non-printing character sequence

Colour: try something like the following:
```
STARTCOLOUR='\e[31m';
ENDCOLOR="\e[0m"
PS1="$STARTCOLOUR\h \u% $ENDCOLOR"
```

Or, if you want to not have weird breaks, and change the
colours if you're root (for safety), maybe something like this:

```
case $(id -u) in
    0)
        STARTCOLOUR='\[\e[36m\]';
        ;;
    *)
        STARTCOLOUR='\[\e[31m\]';
        ;;
esac
ENDCOLOR="\[\e[0m\]"
PS1="$STARTCOLOUR\h \u% $ENDCOLOR";
```

Changing the (xterm) title dynamically:

```
case $(id -u) in
    0)
        STARTCOLOUR='\[\e[36m\]';
        ;;
    *)
        STARTCOLOUR='\[\e[31m\]';
        ;;
esac
ENDCOLOR="\[\e[0m\]"
case $TERM in
    xterm*)
        TITLEBAR='\[\e]0;\h \w\007\]';
        ;;
    *)
        TITLEBAR="";
        ;;
esac

PS1="$TITLEBAR$STARTCOLOUR\h \u% $ENDCOLOR"
```

