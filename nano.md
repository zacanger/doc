# NANO

It's not a great editor. But I know a lot of folks just don't have the time to get comfortable with vi/vim.
If that's you, and you need to be in a terminal-only situation, just use Nano. It's there. It's easy.
Here are some things to make it easier.
(Also, definitely grab my [.nanorc](https://github.com/zacanger/z/blob/master/.nanorc_) and these
[syntax highlighting files](https://github.com/zacanger/z/tree/master/.nano) to make your Nano experience
a little less gross and bland!)

* Files
  * `nano file.ext` opens (or creates) that file
  * `CTRL+o Y ENTER` saves changes
  * `ALT+>` switches to next file buffer
  * `ALT+<` switches to previous
  * `CTRL+X` quits
* Navigation
  * `CTRL+a` moves to beginning of line
  * `CTRL+e` moves to end of line
  * `CTRL+v` goes down one page
  * `CTRL+y` goes up one page
  * `ALT+\` to beginning of file
  * `ALT+/` to the end
  * `ALT+g` to jump to a line
  * `ALT+]` to jump to matching symbol (like vim's `%`)
  * `ALT+a ALT+}` selects and indents that block
  * `ALT+a ALT+{` selecets and outdents that block
* Operations
  * `ALT+a` to select or deselect a block
  * `ALT+a ALT+^` copy that block to primary (clipboard)
  * `ALT+a CTRL+k` cut to same
  * `CTRL+k` Cut from cursor to the end of the line
  * `CTRL+u` Uncut (paste)
  * `CTRL+w` to search for a string
  * `ALT+w` to repeat the search
  * `ALT+r` to search and replace

