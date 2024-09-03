# vi(m) cheat sheet

[source](http://www.lagmonster.org/docs/vi2.html)

1\. Before doing anything to a document, type the following command followed by a carriage return: :set showmode

2\. VI is CaSe SEnsItiVe!!! So make sure Caps Lock is OFF.

#### **Starting VI**

| vi _filename_             | Edits _filename_                                                  |
| ------------------------- | ----------------------------------------------------------------- |
| vi -r _filename_          | Edits last save version of _filename_ after a crash               |
|                           |                                                                   |
| vi + n _filename_         | Edits _filename_ and places curser at line n                      |
|                           |                                                                   |
| vi + _filename_           | Edits _filename_ and places curser on last line                   |
|                           |                                                                   |
| vi +/_string_ _filename_  | Edits _filename_ and places curser on first occurance of _string_ |   |
|                           |                                                                   |   |
| vi _filename_ _file2_ ... | Edits _filename_, then edits _file2_ ... After the save, use :n   |
|                           |                                                                   |
|                           |                                                                   |
| **Ending VI**             |                                                                   |
| ZZ or :wq or :x           | Saves and exits VI                                                |
| :w                        | Saves current file but doesn't exit                               |
| :w!                       | Saves current file overriding normal checks but doesn't exit      |
| :w _file_                 | Saves current as _file_ but doesn't exit                          |
| :w! _file_                | Saves to _file_ overriding normal checks but doesn't exit         |
| :n,mw _file_              | Saves lines n through m to _file_                                 |
| :n,mw >>_file_            | Saves lines n through m to the end of _file_                      |
| :q                        | Quits VI and may prompt if you need to save                       |
| :q!                       | Quits VI and without saving                                       |
| :e!                       | Edits file discarding any unsaved changes (starts over)           |
| :we!                      | Saves and continues to edit current file                          |

| h | Move left |
| j | Move down |
| k | Move up |
| l | Move right |
| Arrow Keys | These do work, but they may be too slow on big files. Also may have unpredictable results when arrow keys are not mapped correctly in client. |
| w | Move to next word |
| W | Move to next blank delimited word |
| b | Move to the beginning of the word |
| B | Move to the beginning of blank delimted word |
| ^ | Moves to the first non-blank character in the current line |
| \+ or  | Moves to the first character in the next line |
| - | Moves to the first non-blank character in the previous line |
| e | Move to the end of the word |
| E | Move to the end of Blank delimited word |
| ( | Move a sentence back |
| ) | Move a sentence forward |
| { | Move a paragraph back |
| } | Move a paragraph forward |
| [[ | Move a section back |
| ]] | Move a section forward |
| 0 or | | Move to the begining of the line |
| n| | Moves to the column n in the current line |
| $ | Move to the end of the line |
| 1G | Move to the first line of the file |
| G | Move to the last line of the file |
| nG | Move to nth line of the file |
| :n | Move to nth line of the file |
| fc | Move forward to c |
| Fc | Move back to c |
| H | Move to top of screen |
| nH | Moves to nth line from the top of the screen |
| M | Move to middle of screen |
| L | Move to botton of screen |
| nL | Moves to nth line from the bottom of the screen |
| Control-d | Move forward screen |
| Control-f | Move forward one full screen |
| Control-u | Move backward screen |
| Control-b | Move backward one full screen |
| CTRL-e | Moves screen up one line |
| CTRL-y | Moves screen down one line |
| CTRL-u | Moves screen up page |
| CTRL-d | Moves screen down page |
| CTRL-b | Moves screen up one page |
| CTRL-f | Moves screen down one page |
| CTRL-I | Redraws screen |
| z  | z-carriage return makes the current line the top line on the page |
| nz  | Makes the line n the top line on the page |
| z. | Makes the current line the middle line on the page |
| nz. | Makes the line n the middle line on the page |
| z- | Makes the current line the bottom line on the page |
| nz- | Makes the line n the bottom line on the page |
| % | Move to associated ( ), { }, [ ] |

| x | Delete character to the right of cursor |
| nx | Deletes n characters starting with current; omitting n deletes current character only |
| X | Delete character to the left of cursor |
| nX | Deletes previous n characters; omitting n deletes previous character only |
| D | Delete to the end of the line |
| d$ | Deletes from the cursor to the end of the line |
| dd or :d | Delete current line |
| ndw | Deletes the next n words starting with current |
| ndb | Deletes the previous n words starting with current |
| ndd | Deletes n lines beginning with the current line |
| :n,md | Deletes lines n through m |
| d_Motion_cmd___ | Deletes everything included in the Motion Command (e.g., dG would delete from current position to the end of the file, and d4 would delete to the end of the fourth sentence).  |
| "np | Retrieves the last nth delete (last 9 deletes are kept in a buffer) |
| "1pu.u. | Scrolls through the delete buffer until the desired delete is retrieved (repeat u.) |

| C | Change to the end of the line |
| cc or S | Change the whole line until ESC is pressed |
| xp | Switches character at cursor with following character |
| s_text_ | Substitutes text for the current character until ESC is used |
| cw_text_ | Changes current word to text until ESC is used |
| C_text_ | Changes rest of the current line to text until ESC is used |
| c_Motion_cmd_ | Changes to text from current position to Motion Command until ESC is used |
| << or >> | Shifts the line left or right (respectively) by one shift width (a tab) |
|  | |
| n<< or n>> | Shifts n lines left or right (respectively) by one shift width (a tab) |
|  | |
| <_Motion_cmd_ or >_Motion_cmd_ | Use with Motion Command to shift multiple lines left or right |

| /_string_ | Search forward for _string_ |
| ?_string_ | Search back for _string_ |
| n | Search for next instance of _string_ |
| N | Search for previous instance of _string_ |
| % | Searches to beginning of balancing ( ) [ ] or { } |
| f_c_ | Searches forward in current line to _char_ |
| F_c_ | Searches backward in current line to _char_ |
| t_c_ | Searches forward in current line to character before char |
| Tchar | Searches backward in current line to character before char |
| ?str | Finds in reverse for str |
| :set ic | Ignores case when searching |
| :set noic | Pays attention to case when searching |
| :n,ms/_str1_/_str2_/_opt_ | Searches from n to m for _str1_; replaces _str1_ to _str2_; using opt-opt can be g for global change, c to confirm change (y to acknowledge,  to suppress), and p to print changed lines |
| & | Repeats last :s command |
| :g/_str_/_cmd_ | Runs _cmd_ on all lines that contain _str_ |
| :g/_str1_/s/_str2_/_str3_/ | Finds the line containing _str1_, replaces _str2_ with _str3_ |
| :v/_str_/_cmd_ | Executes _cmd_ on all lines that do not match _str_ |
| , | Repeats, in reverse direction, last / or ? search command |

[...] - Set Examples
| [A-Z] | The SET from Capital A to Capital Z |
| [a-z] | The SET from lowercase a to lowercase z |
| [0-9] | The SET from 0 to 9 (All numerals) |
| [./=+] | The SET containing . (dot), / (slash), =, and + |
| [-A-F] | The SET from Capital A to Capital F and the dash (dashes must be specified first) |
| [0-9 A-Z] | The SET containing all capital letters and digits and a space |
| [A-Z][a-zA-Z] | In the first position, the SET from Capital A to Capital Z
In the second character position, the SET containing all letters |
| [a-z]{m} | Look for _m_ occurances of the SET from lowercase a to lowercase z |
| [a-z]{m,n} | Look for at least m occurances, but no more than n occurances of the SET from lowercase a to lowercase z |

Regular Expression Examples
| /Hello/ | Matches if the line contains the value Hello |
| /^TEST$/ | Matches if the line contains TEST by itself |
| /^[a-zA-Z]/ | Matches if the line starts with any letter |
| /^[a-z].*/ | Matches if the first character of the line is a-z and there is at least one more of any character following it |
| /2134$/ | Matches if line ends with 2134 |
| /(21|35)/ | Matches is the line contains 21 or 35
Note the use of ( ) with the pipe symbol to specify the 'or' condition |
| /[0-9]*/ | Matches if there are zero or more numbers in the line |
| /^[^#]/ | Matches if the first character is not a # in the line |
| Notes:
1\. Regular expressions are case sensitive
2\. Regular expressions are to be used where _pattern_ is specified |  |

| :! cmd | Executes shell command cmd; you can add these special characters to indicate:% name of current file# name of last file edited |
| !! cmd | Executes shell command cmd, places output in file starting at current line |
| :!! | Executes last shell command |
| :r! cmd | Reads and inserts output from cmd |
| :f file | Renames current file to file |
| :w !cmd | Sends currently edited file to cmd as standard input and execute cmd |
| :cd dir | Changes current working directory to dir |
| :sh | Starts a sub-shell (CTRL-d returns to editor) |
| :so file | Reads and executes commands in file (file is a shell script) |
| !_Motion_cmd_ | Sends text from current position to Motion Command to shell command _cmd_ |
| !}sort | Sorts from current position to end of paragraph and replaces text with sorted text |

Note: Options given are default. To change them, enter type :set option to turn them on or :set no_optioni_ to turn them off.To make them execute every time you open VI, create a file in your HOME directory called .exrc and type the options without the colon (:) preceding the option
| Set | Default | Description |
| :set ai | noai | Turns on auto indentation |
| :set all | \-- | Prints all options to the screen |
| :set ap | aw | Prints line after d c J m :s t u commands |
| :set aw | noaw | Automatic write on :n ! e# ^^ :rew ^} :tag |
| :set bf | nobf | Discards control characters from input |
| :set dir=_tmp_ | dir = /tmp | Sets _tmp_ to directory or buffer file |
| :set eb | noed | Precedes error messages with a bell |
| :set ed | noed | Precedes error messages with a bell |
| :set ht= | ht = 8 | Sets terminal hardware tabs |
| :set ic | noic | Ignores case when searching |
| :set lisp | nolisp | Modifies brackets for Lisp compatibility. |
| :set list | nolist | Shows tabs (^l) and end of line ($) |
| :set magic | magic | Allows pattern matching with special characters |
| :set mesg  | mesg | Allows others to send messages |
| :set no_option_ | \-- | Turns off _option_ |
| :set nu | nonu | Shows line numbers |
| :set opt | opt | Speeds output; eliminates automatic RETURN |
| :set para= | para = LIlPLPPPQPbpP | macro names that start paragraphs for { and } operators |
| :set prompt | prompt | Prompts for command input with : |
| :set re | nore | Simulates smart terminal on dumb terminal |
| :set remap | remap | Accept macros within macros |
| :set report | noreport | Indicates largest size of changes reported on status line |
| :set ro | noro | Changes file type to "read only" |
| :set scroll=n | scroll = 11 | set n lines for CTRL-d and z |
| :set sh=_shell_path_ | sh = /bin/sh | set shell escape (default is /bin/sh) to _shell_path_ |
| :set showmode | nosm | Indicates input or replace mode at bottom |
| :set slow | slow | Pospone display updates during inserts |
| :set sm | nosm | Show matching { or ( as ) or } is typed |
| :set sw=n | sw = 8 | Sets shift width to n characters |
| :set tags=x | tags = /usr/lib/tags | Path for files checked for tags (current directory included in default) |
| :set term | $TERM | Prints terminal type |
| :set terse | noterse | Shorten messages with terse |
| :set timeout | noto | Eliminates one-second time limit for macros |
| :set tl=n | tl = 0 | Sets significance of tags beyond n characters (0 means all) |
| :set ts=n | ts = 8 | Sets tab stops to n for text input |
| :set wa | nowa | Inhibits normal checks before write commands |
| :set warn | warn |  | Warns "no write since last change" |
| :set window=n | window = n | Sets number of lines in a text window to n |  |
| :set wm=n | wm = 0 | Sets automatic wraparound n spaces from right margin. |
| :set ws | ws | Sets automatic wraparound n spaces from right margin. |

