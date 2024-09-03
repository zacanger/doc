# more advanced vi(m)

* `vimtutor` or (in vim) `:tutor`: learn vim
* `vim -u NONE -N`: load vim with no plugins
* `"0p`: the zero register, where the most recently yanked text is always stored (never deletes)
* 1-9 hold the most recent deletes (1 being the most recent)
* using vim-commentary:
  * `gcc`: comment out a line
  * `gc`: comment out the target of a motion
  * `gcap`: comment out a paragraph
* using vim-surround:
  * `cs"'`: change surroundings from `"` to `'`
  * `cs'`: delete the `'` surroundings
  * `ysiw]`: change surroundings `]`
* vim-abolish:
  * `:%Subvert/facilit{y,ies}/building{,s}/g`: substitute multiple variants of a word
* vim-unimpaired: plugin for accessing pairs of mappings (newlines, next files, etc.)
* marks:
  * `ma`: set mark at current cursor
  * `'a`: jump to mark `a`
  * `\`a`: jump to line and column of mark `a`
  * `:marks`: list all marks
* `C-z`: stash window in the background
  * `fg` to bring it back
* `Gundoshow`: show undo trees (with gundo.vim installed)
* `:g/<regex>/d`: delete all lines that match `<regex>`
* windows:
  * `Cw-s`: horizontal split
  * `Cw-v`: vertical split
  * `Cw-` with `h j k l`: focus window in that direction
  * `Cw-w`: focus next window
* line numbers:
  * `:set nu`: enable
  * `:set nonu`: disable
  * `:set nu!`: toggle
* `:sort u`: sort lines alphabetically
* visual block mode:
  * this is really useful for working with patterns that are difficult with regex (mostly columns)
  * `C-v`: enter mode
  * `A` and `I`: insert mode
  * `esc`: execute changes made while in insert mode
* `:set tw=80`, then `gq`: format text to fit lines at 80 characters
* jump to character:
  * `f<char>`: jump to char
  * `F<char>`: jump back to char
  * `t<char>`: jump to char before match
  * `;`: repeat jump
  * `,`: repeat jump back
* modes:
  * `n`: normal only
  * `v`: visual and select
  * `o`: operator-pending
  * `x`: visual only
  * `s`: select only
  * `i`: insert
  * `c`: command-line
  * `l`: insert, command-line, regex (and more; called 'Lang-Arg' pseudo-mode)
* Buffers:
  * probably _the_ most underused vim feature.
  * other editors have tabs. vim has buffers. vim also has tabs, actually.
  * tabs: open one per feature/project (basically workspaces)
  * buffers: open one per _file_ (nested under workspaces)
  * tabs are different views on buffers. buffers manage files.
  * buffers are kind of annoying to use; use `ctrlp` to make them convenient!
  * `enew`: open empty buffer
  * `bd`: close buffer
  * `<buffer number>bd`: close specific buffer
  * `ls`: list open buffers
  * `ls!`: list all open buffers (includes unlisted)

