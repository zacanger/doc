# Find

Synopsis:

    find [path] [expression]


Quick and Easy
--------------

Find the `find` binary:

    find /usr/bin -name find

Put more than one path:

    find /usr/bin /usr/local/bin -name find

Expression can be omitted, found files are not filtered:

    find /usr/bin /usr/local/bin

Path can be omitted as well, default to current directory:

    find

which is the same as:

    find .


Greediness
----------

Find is **greedy**, it will search the current directory and all subdirectories:

    find /usr -name find


Date and Time
-------------

Find files that are newer than 2 hours old:

    find -type f -newermt "$(date --date='2 hours ago')"

Find files that are older than 2 hours old (complementary):

    find -type f ! -newermt "$(date --date='2 hours ago')"


Case Sensitivity
----------------

Perform a case-insensitive find:

    find /usr/bin -iname FIND


Execution
---------

Find all compressed files:

    find ~/Downloads -name '*.tar.gz'

Extract all compressed files at once by find command:

    find ~/Downloads -name '*.tar.gz' -exec tar xzpf '{}' \;

`'{}'` matches the file that was found. `\;` terminates the exec command.

Find files named `core` in or below the directory `/tmp` and delete them.

    find /tmp -name core -type f -print | xargs /bin/rm -f

Note that this will work incorrectly if there are any filename containing newlines, single or double quotes, or spaces.

The correct way to handle newlines, single or double quotes, or spaces is using `-print0` instead of `-print`:

    find /tmp -name core -type f -print0 | xargs -0 /bin/rm -f

The `-name` test comes before the `-type` test in order to avoid having to call `stat` on every file. `-print0` prints the full file name on the standard output, followed by a null character (instead of the newline character that `-print` uses). This allows file names that contain newlines or other types of white space to be correctly interpreted by programs that process the find output. This option corresponds to the -0 option of `xargs`.

Find directory named .svn in or below the current directory and delete them.

    find -name .git -type d -print0 | xargs -0 /bin/rm -f

No run if empty:

    find -name .git -type d -print0 | xargs -0 --no-run-if-empty /bin/rm -f

About print options:

    -print:  followed by a newline
    -print0: followed by a null character
    -printf: format printing
