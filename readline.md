* `Ctrl + a` – go to the start of the command line
* `Ctrl + e` – go to the end of the command line
* `Ctrl + k` – delete from cursor to the end of the command line
* `Ctrl + u` – delete from cursor to the start of the command line
* `Ctrl + w` – delete from cursor to start of word (i.e. delete backwards one word)
* `Ctrl + y` – paste word or text that was cut using one of the deletion shortcuts (such as the one above) after the cursor
* `Ctrl + xx` – move between start of command line and current cursor position (and back again)
* `Alt + b` – move backward one word (or go to start of word the cursor is currently on)
* `Alt + f` – move forward one word (or go to end of word the cursor is currently on)
* `Alt + d` – delete to end of word starting at cursor (whole word if cursor is at the beginning of word)
* `Alt + c` – capitalize to end of word starting at cursor (whole word if cursor is at the beginning of word)
* `Alt + u` – make uppercase from cursor to end of word
* `Alt + l` – make lowercase from cursor to end of word
* `Alt + t` – swap current word with previous
* `Ctrl + f` – move forward one character
* `Ctrl + b` – move backward one character
* `Ctrl + d` – delete character under the cursor
* `Ctrl + h` – delete character before the cursor
* `Ctrl + t` – swap character under cursor with the previous one
* `Ctrl + r` – search the history backwards
* `Ctrl + g` – escape from history searching mode
* `Ctrl + p` – previous command in history (i.e. walk back through the command history)
* `Ctrl + n` – next command in history (i.e. walk forward through the command history)
* `Alt + .` – use the last word of the previous command
* `Ctrl + l` – clear the screen
* `Ctrl + s` – stops the output to the screen (for long running verbose command)
* `Ctrl + q` – allow output to the screen (if previously stopped using command above)
* `Ctrl + c` – terminate the command
* `Ctrl + z` – suspend/stop the command

Other:
* `!!` – run last command
* `!blah` – run the most recent command that starts with ‘blah’ (e.g. `!ls`)
* `!blah:p` – print out the command that `!blah` would run (also adds it as the latest command in the command history)
* `!$` – the last word of the previous command (same as `Alt + .`)
* `!$:p` – print out the word that `!$` would substitute
* `!*` – the previous command except for the last word (e.g. if you type ‘find some_file.txt /‘, then `!*` would give you ‘find some_file.txt‘)
* `!*:p` – print out what `!*` would substitute
* `^^` Substitution, eg `ls -l`, then `^-l^-o`
