# Emacs Cheatsheet

* M-@ is mark-word, C-M-@ is mark-sexp, and C-M-h is mark-defun
* C-c C-b goes back in a help buffer
* C-h C-n (view-emacs-news) shows Emacs version history
* C-u C-x C-e inserts the result of the last sexp
* C-x 8 RET (insert-char) inserts a character by Unicode name or code point
* M-! is shell-command and M-| is shell-command-on-region
* C-u M-| replaces the region
* M-z " deletes up to the next double quote and M-- M-z " deletes up to the previous double quote
* C-M-k is kill-sexp, M-k is kill-sentence, and C-x DEL is backward-kill-sentence
* C-M-% `<\([^>]+\)> RET <\,(downcase \1)> RET` makes XML tags lowercase
* M-s h l is highlight-lines-matching-regexp and M-s h u removes highlights added by M-s h l
* C-x n n (narrow-to-region) shows only the lines in the region and C-x n w (widen) undoes narrowing
* C-x f is set-fill-column
* C-M-\ indents a region and C-M-q indents a sexp
* C-s C-w searches for the word after the point and C-s C-M-y C-M-y searches for two characters after the point
* you can use C-x r t (string-rectangle) to insert text on multiple lines
* C-M-% [0-9]+ RET \,(1+ \#&) RET adds 1 to numbers, where \#& is the matched string interpreted as a number
* M-x align-regexp RET = RET aligns equals signs by adding spaces before them
* you can use C-h l to see escape sequences for previously pressed keys
* C-x v + is vc-update and C-x v = is vc-diff
* M-x flush-lines deletes lines that match a pattern and M-x keep-lines deletes lines that do not match a pattern
* M-x flyspell-prog-mode checks for spelling in comments and strings
* C-x C-n is set-goal-column and C-u C-x C-n unsets a goal column
* M-m (back-to-indentation) moves the point to the first non-whitespace character on the current line
* C-x RET C-\ is set-input-method
* C-x RET C-\ tex RET \alpha inserts an alpha character
* you can use M-x delete-trailing-whitespace to convert CRLF line endings to LF
* C-u C-u C-x } makes a window 16 characters wider
* C-x 5 0 is delete-frame, C-x 5 1 is delete-other-frames, and C-x 5 2 is make-frame-command
* ido-menu jumps to a definition in the current file
* C-S-backspace is kill-whole-line
* C-x r s 1 saves text to register 1 and C-x r i 1 inserts the text in register 1
* C-x r <SPC> 1 saves the point in register 1 and C-x r j 1 jumps to register 1
* C-x r w 1 saves the window configuration to register 1 and C-x r j 1 restores the window configuration in register 1
* M-x view-register RET 1 shows the contents of the register 1
* C-x r s is copy-to-register
* C-x r i is insert-register
* C-x r <SPC> is point-to-register
* C-x r j is jump-to-register
* C-x r w is window-configuration-to-register
* C-x r f is frame-configuration-to-register
* C-x r r is copy-rectangle-to-register
* C-x * * is calc
* C-x $ is set-selective-display
* M-6 C-x $ hides lines indented by 6 or more columns
* M-1 C-x $ shows only unindented lines
* C-x $ turns off selective display when selective display is enabled
* M-x toggle-truncate-lines toggles between folding and truncating long lines
* C-x 4 0 is kill-buffer-and-window
* C-x 4 c is clone-indirect-buffer-other-window
* M-r is previous-matching-history-element in minibuffer-local-map
* M-x list-command-history shows a list of commands typed in the minibuffer
* C-x <ESC> <ESC> (repeat-complex-command) executes commands from command history
* C-h . (display-local-help) shows tooltip text
* C-h L utf-8 describes the utf-8 language environment
* C-h d searches in the docstrings of built-in symbols and C-u C-h d searches in all docstrings
* C-h p (finder-by-keyword) shows a list of ELPA packages grouped under categories
* C-h P yasnippet RET opens a buffer that describes yasnippet
* C-h e (view-echo-area-messages) opens the *Messages* buffer
* C-<SPC> C-<SPC> sets and deactivates the mark and C-u C-<SPC> jumps to a position marked with C-<SPC> C-<SPC>
* C-h v kill-ring RET displays the contents of the kill ring
* M-x append-to-buffer appends text to a buffer and M-x copy-to-buffer replaces the contents of a buffer
* C-x r y is yank-rectangle and C-x r M-w is copy-rectangle-as-kill
* C-x r o (open-rectangle) inserts a rectangle of spaces
* C-x r c (clear-rectangle) replaces all characters in the rectangle with spaces
* C-x r m is bookmark-set, C-x r j is bookmark-jump, and C-x r l is list-bookmarks
* C-x r m emacs RET sets the bookmark named emacs and C-x r j emacs RET opens the bookmark named emacs
* M-x bookmark-save saves bookmarks to bookmark-default-file
* M-x dired-jump opens a dired buffer for the directory of the current file
* C-x ( is kmacro-start-macro, C-x ) is kmacro-end-macro, and C-x e is kmacro-end-and-call-macro
* M-x check-parens checks for unbalanced parentheses
* M-, is tags-loop-continue
* C-x = (what-cursor-position) shows brief information about the current position and character
* C-u C-x = or M-x describe-char shows detailed information about the current position and character
* M-5 C-x e repeats a macro five times and M-0 C-x e repeats a macro until there is an error
* M-x ff-find-other-file opens a corresponding header or source file
* C-x + is balance-windows and C-x - is shrink-window-if-larger-than-buffer
* M-x load-file loads a Lisp file
* C-a C-o inserts a new line above
* C-M-l (reposition-window) makes the current definition or comment visible
* C-x < is scroll-left and C-x > is scroll-right
* C-x n d is narrow-to-defun
* q deletes a view mode buffer and e exits view mode
* M-x list-faces-display shows currently defined faces
* M-x list-colors-display lists the names of colors
* C-x C-+ or C-x C-= increases text size
* M-x global-font-lock-mode toggles font lock mode in all buffers
* M-x customize-group RET font-lock-faces RET customizes the faces used for syntax highlighting
* M-x replace-regexp RET [0-9]+ RET \,(format "%04d" \#&) RET pads numbers with zeros to four digits
* M-x find-library ido RET opens ido.el.gz
* M-x find-library RET RET opens the elisp file for a package when the point is at the name of the package
* M-x find-function visits the elisp file where a function is defined
* M-x find-function-on-key visits the elisp file where a function assigned to a key is defined
* M-x find-variable visits the elisp file where a variable is defined
* M-0 M-t transposes the words at the mark and the point
* M-x compare-windows compares the text of the current window and the next window
* C-x i (insert-file) inserts the contents of a file
* M-x write-region writes the region to a file and M-x append-to-file appends the region to a file
* C-x 6 2 is 2C-two-columns, C-x 6 b is 2C-associate-buffer, and C-x 6 s is 2C-split
* M-ESC ESC deactivates the mark
* C-u C-/ undoes changes within a region when transient mark mode is not enabled
* M-x ffap-menu shows a list of files and URLs in a buffer
* S-Mouse-3 is ffap-at-mouse and C-S-Mouse-3 is ffap-menu
* M-v is shift-to-completions in the minibuffer
* F10 is menu-bar-open and M-\` is tmm-menubar
* C-u M-; kills a comment and whitespace before the comment
* C-\ is toggle-input-method
* M-g c (goto-char) goes to a buffer position
* M-x list-fontsets lists currently used fontsets
* M-x menu-set-font opens a font picker for changing the font
* C-u M-q fills a paragraph with justification
* M-x kill-compilation or C-x k *compilation* RET terminates a compilation process
* C-x C-\ is comint-quit-subjob in comint-mode
* C-x RET f is set-buffer-file-coding-system
* C-x RET f unix RET converts CRLF to LF
* C-h c is describe-key-briefly
* M-x apropos-value RET ^aa RET searches for variables whose value starts with aa
* M-x customize-changed RET 24.3 RET customizes settings that changed in Emacs 24.3
* TAB is c-indent-line-or-region, C-c C-c is comment-region, and C-c C-q is c-indent-defun in cc-mode
* M-a is c-beginning-of-statement and M-e is c-end-of-statement in cc-mode
* C-u C-h i opens an info file
* M-x color-theme-select opens a buffer for selecting or previewing themes
* C-h i g (elisp) RET or M-x info-display-manual RET elisp RET opens the elisp manual
* C-h i g (coreutils) RET i stat RET opens the section for stat from the coreutils manual
* M-x hl-line-mode toggles highlighting the current line
* M-x scroll-all-mode makes scrolling commands scroll all windows in the current frame
* C-h S is info-lookup-symbol
* M-p goes to the previous work directory in ido-find-file
* M-s searches for files in the work directory history in ido-find-file
* M-m creates a directory in ido-find-file
* C-k kills a buffer in ido-switch-buffer
* M-x follow-mode C-x 3 shows the next page of the current buffer in another window
* C-c / is sgml-close-tag in sgml-mode
* M-x elisp-index-search searches in the index of the elisp manual
* M-x set-face-foreground RET default RET black RET sets the foreground color of the default face to black
* M-x info-apropos searches in the indexes of Info files and M-x apropos-documentation searches in docstrings
* C-h w (where-is) shows what keybindings a function has
* M-x profiler-start starts profiling and M-x profiler-report ends profiling
* C-h F is Info-goto-emacs-command-node and C-h K is Info-go-to-emacs-key-command-node
* C-h F hippie-expand RET opens the info node for hippie-expand
* M-x browse-url-at-point or M-x ffap opens a URL at point
* C-x 8 " a inserts LATIN SMALL LETTER A WITH DIAERESIS and C-x 8 ' e inserts LATIN SMALL LETTER E WITH ACUTE
* M-x getenv displays the value of an environment variable and M-x setenv sets the value of an environment variable
* M-x kill-paragraph kills to the end of a paragraph and M-x backward-kill-paragraph kills to the beginning of a paragraph
* M-x font-lock-mode toggles syntax highlighting
* C-x h <DEL> makes a buffer empty when transient mark mode is enabled but does not add the contents of the buffer to the kill ring
* C-x h C-w makes a buffer empty even when transient mark mode is not enabled and adds the contents of the buffer to the kill ring
* M-x erase-buffer makes a buffer empty but does not add the text of the buffer to the kill ring

## Emacs Lisp Basics

```lisp
(+ (expt (sin .5) 2) (expt (cos .5) 2)) ; 1
(cons 1 (cons 2 (cons 3 nil))) ; (1 2 3)
(float 5) ; 5.0
(apply '+ '(1 2 3)) ; 6
(concat "aa" "bb") ; "aabb"
(length "aa") ; 2
(replace-regexp-in-string "a+" "b" "aac") ; "bc"
(split-string "a,b" ",") ; ("a" "b")
(format "%03d" 2) ; "002"
(string-to-number "3") ; 3
(number-to-string 3) ; "3"
(file-name-directory "/dir/file.txt") ; "/dir/"
(file-name-nondirectory "/dir/file.txt") ; "file.txt"
(file-name-extension "/dir/file.txt") ; "txt"
(file-name-sans-extension "/dir/file.txt") ; "/dir/file"
(lsh 512 -3) ; 64
(logior 1 3) ; 3
(logiand 1 3) ; 1
(substring "xyz" -1) ; "z"
(substring "xyz" 1 3) ; "yz"
(remove 'b '(a b c)) ; (a c)
(remove-duplicates '(1 1 2)) ; (1 2)
(remove-duplicates '("a" "a" "b") :test 'string=) ; ("a" "b")
(nconc '(a b) 'c) ; (a b . c)
(nconc '(a b) '(c d)) ; (a b c d)
(append '(a b) '(c d)) ; (a b c d)
(last '(a b c d e) 2) ; (d e)
(butlast '(a b c d e) 2) ; (a b c)
(number-sequence 1 7 3) ; (1 4 7)
(mapcar 'car '((a b) (c d))) ; (a c)
(mapcar '1+ [1 2 3]) ; (2 3 4)
(mapcar* 'cons '(a b) '(1 2)) ; ((a . 1) (b . 2))
(member "c" '("a" "b")) ; nil
(expt 16 4) ; 65536
(regexp-quote "a+") ; "a\\+"
(string-equal "c" (substring "abc" -1)) ; t
(read-from-string "abcde") ; (abcde . 5)
(read-from-string "abcde" 2) ; (cde . 5)
(prin1-to-string 'aa) ; "aa"
(all-completions "aa" '(("aab" 1) ("aac" 2) ("bb" 3))) ; ("aab" "aac")
(/= 15 5) ; t
(shell-quote-argument "\\'\"${[<|") ; "\\\\\\'\\\"\\$\\{\\[\\<\\|"
(buffer-local-value 'major-mode (get-buffer "*Messages*")) ; fundamental-mode
(lognot #b1001) ; -10
(aref [7 8 9] 2) ; 9
(elt [7 8 9] 2) ; 9
(elt '(7 8 9) 2) ; 9
(string (elt "1234" 2)) ; "3"
(make-string 3 65) ; "AAA"
(md5 "a") ; "0cc175b9c0f1b6a831c399e269772661"
(natnump -1) ; nil
(nreverse '(1 2 3)) ; 3 2 1
(apply-partially +1 1 2) ; (closure (t) (&rest args) (apply (quote 1) (quote 1) (quote 2) args))
(regexp-quote ".*") ; "\\.\\*"
(nth 2 '(1 2 3 4)) ; 3
(mapcar (lambda (x) (nth 1 x)) '((a b c) (d e f))) ; (b e)
(char-to-string 97) ; "a"
(zerop (mod 9 3)) ; t
(make-vector 3 0) ; [0 0 0]
(cons 1 '(2 3)) ; (1 2 3)
(cons '(1 2) '(3 4)) ; ((1 2) 3 4)
(append '(1 2) '(3 4)) ; (1 2 3 4)
(mapcar '1+ '(1 2 3)) ; (2 3 4)
(url-hexify-string " %") ; "%20%25"
(url-unhex-string "%20%25") ; " %"
(truncate-string-to-width "aaa" 2) ; "aa"
(eq '() nil) ; t
(let (l) (push 1 l) l) ; (1)
(remove-if-not (lambda (c) (string-prefix-p "a" c)) '("aa" "ba")) ; ("aa")
(sort '("b" "a") #'string<) ; ("a" "b")
(default-value 'fill-column) ; 70
(split-string "aa;bb;" ";") ; ("aa" "bb" "")
(split-string "aa;bb;" ";" t) ; ("aa" "bb")
(format "%S" "a\"\\") ; "\"a\\\"\\\\\""
(decode-time (date-to-time "27-Sep-83 12:35:59 EST")); (59 35 19 27 9 1983 2 nil 7200)
(float-time (date-to-time "13 Feb 2009 23:31:30 UTC")); 1234560690.0
(format-time-string "%F %T" (seconds-to-time 1234585890)) ; "2009-02-13 23:31:30"
(format-seconds "%Y %D %h:%m:%s" (1- (* 400 24 3600))) ; "1 year 34 days 23:59:59"
(with-temp-buffer (insert "aabbcc") (goto-char (point-min)) (re-search-forward "b+") (point)) ; 5
(with-temp-buffer (insert "aabbcc") (goto-char (point-min)) (looking-at "a")) ; t
(string= "bb" (nth 1 '("aa" "bb" "cc"))) ; t
(nreverse '("aa" "bb" "cc")); ("cc" "bb" "aa")
(rx-to-string '(or "aa" "bb")) ; "\\(?:\\(?:aa\\|bb\\)\\)"
(regexp-opt '("aa" "bb")) ; "\\(?:aa\\|bb\\)"
(apply #'vector (mapcar #'1+ [1 2 3])) ; [2 3 4]
(cl-map 'vector #'1+ [1 2 3]) ; [2 3 4]

(random 3) ; random number between 0 and 2
(set-buffer "*scratch*")
(kill-buffer "*scratch*")
(directory-files "/usr/share/emacs/site-lisp/" nil "\\.el$")
(count-lines (window-start) (window-end))
(if (null (get-buffer-process (current-buffer))) (kill-buffer))
(setenv "PATH" (concat (getenv "HOME") "/bin:" (getenv "PATH")))
(erase-buffer)
(delete-region 1 10)
(file-directory-p "/bin")
(switch-to-buffer (generate-new-buffer "temp"))
(if (not (one-window-p) (delete-window)))
(mapc 'kill-buffer (delq (current-buffer) (buffer-list))) ; kill other buffers
(insert-file-contents "~/file.txt")
(thing-at-point 'word)
(thing-at-point 'symbol)
(bounds-of-thing-at-point 'line)
(rename-file "/tmp/a" "/tmp/b")
(delete-char 5) ; delete five characters forward
(defmacro comment (rest body) nil)
(kill-new (buffer-file-name)) ; save the name of the buffer to the kill ring
(browse-url (concat "file://" (buffer-file-name)))
(propertize "a" 'face 'italic)
(dotimes (i 20) (insert (format "%d\n" (1+ i))))
(setq buffer-read-only t)
(buffer-disable-undo)
(expand-file-name (concat user-emacs-directory "elisp"))
(format-kbd-macro (read-key-sequence "key? " nil t))
(setq mode-line-format nil) ; hide the mode line
(skip-chars-forward "\n ") ; move to the first character that is not space or \n
(region-active-p) ; t if transient mark mode is enabled and the mark is active
(manual-entry (current-word)) ; open the man page for the word at point
(let (minibuffer-allow-text-properties) (read-from-minibuffer "Prompt: "))
(file-name-directory (buffer-file-name))
(setq echo-keystrokes 0.1) ; echo unfinished commands after 0.1 seconds
(set-window-text-height (selected-window) 7)
(text-scale-increase 5)
(defun xor (a b) (if a (not b) b))
(select-window (split-window-horizontally))
(setq history-add-new-input nil) ; do not add elements to minibuffer history
(read-from-minibuffer "Prompt: ")
(read-buffer "Buffer: ")
(read-command "Eval: ")
(if (looking-at "//") (delete-char 2))
(string-equal system-type "gnu/linux")
(insert-file-contents "file.txt")
(if (region-active-p) (region-beginning) (line-beginning-position))
(kill-buffer (current-buffer))
(switch-to-buffer-other-window "*info*")
(directory-files "/usr/local") ; names of files and directories
(directory-files "/usr/local" t) ; absolute paths of files and directories
(if (> (length (window-list)) 1) (delete-other-windows) (bury-buffer))
(shell-command-on-region (mark) (point) "python -mjson.tool" (buffer-name) t)))
(if (and (buffer-modified-p) (buffer-file-name)) (write-file (buffer-file-name))
(interactive "p") ; prefix arg converted to number
(interactive "P") ; prefix arg in raw form
(delete-indentation t) ; delete indentation forward
(set-frame-parameter nil 'alpha '(85 50))
(find-alternate-file (concat "/sudo::" (buffer-file-name)))
(set-frame-parameter (selected-frame) 'fullscreen 'fullboth)
(floor (* 0.6 (x-display-pixel-width)))
(kill-region (point) (point-max)) ; kill to the end of a buffer
(executable-interpret (buffer-file-name))
(find-function 'f) ; jump to the definition of f
(symbol-file 'f) ; get the file where f is defined
(if (window-system) (set-frame-height (selected-frame 60)))
(setq message-log-max nil) ; do not add any messages to the messages buffer
(message "%s" (propertize "message" 'face '(:foreground "red")))
(read-passwd "Password: ")
(delq nil (mapcar 'buffer-file-name (buffer-list))) ; list the files of buffers
(mapconcat 'identity (delq nil (mapcar 'buffer-file-name (buffer-list))) "\n")
(set-frame-width (selected-frame) 100)
(unless (bolp) (beginning-of-line))
(and (bolp) (eolp)) ; test if the point is on an empty line
(skip-chars-backward " \t")
(region-active-p) ; test if the region is active
(use-region-p) ; test if the region is active and not empty
(equal last-input-event 'backspace)
(get-char-property (point) 'face)
(indent-region (point-min) (point-max)) ; reindent a buffer
(eq major-mode 'Info-mode)
(window-buffer) ; get the buffer of the current window
(window-buffer (second (window-list)))
(other-window 1 nil) ; select the next window in the current frame
(other-window -1 t) ; select the previous window including all frames
(get-buffer-window "*scratch*") ; return the first window that displays the scratch buffer
(add-hook 'after-save-hook 'check-parens)
(select-window (previous-window))
(global-unset-key "\C-x\C-c")
(shell-command-on-region (region-beginning) (region-end) "pbcopy")
(buffer-local-variables)
(ido-completing-read "Prompt: " '("aa" "bb"))
(equal (tty-type) "xterm-vt220")
(setq split-height-threshold nil split-width-threshold 0)
(setq message-log-max t) ; do not truncate the messages buffer
(if (window-system) (set-frame-height (selected-frame) 60))
(set-face-attribute 'default nil :height 120)
(display-graphic-p) ; test if DISPLAY is a graphic display
(window-edges (selected-window))
(defmacro command (&rest body) `(lambda () (interactive) ,@body))
(find-font (font-spec :family "Times"))
(eq 0 (nth 2 (file-attributes "/file"))) ; test if /file is owned by root
(find-file "/sudo::/etc/hosts")
(propertize "aa" 'face '(:foreground "green"))
(custom-theme-visit-theme 'custom)
(load-file "~/.emacs.d/custom-theme.el")
(inhibit-field-text-motion t) ; make motion commands ignore fields
(goto-char (next-overlay-change (point))) ; go to the next position where an overlay starts or ends
(let ((inhibit-field-text-motion t)) (end-of-line))
(vertical-motion 3) ; move the point three lines down
(window-buffer (selected-window))
(buffer-substring (line-beginning-position) (line-beginning-position 2))
(and mark-active transient-mark-moe)
(delete-and-extract-region (point) (mark))
(move-to-column 7)
(set-frame-font "Times 20")
(load-file "~/.emacs") ; apply changes to .emacs in the current buffer
(delete-region (point) (save-excursion (skip-syntax-backward "^ ") (point)))
(save-some-buffers 1) ; save all buffers that are visiting a file
(save-some-buffers t) ; save all buffers that are visiting a file and some buffers that are not visiting a file
(and (buffer-file-name) (buffer-modified-p))
(let ((fill-column (point-max))) (fill-paragraph nil)) ; unfill a paragraph
(let ((fill-column (point-max))) (fill-region (region-beginning) (region-end) nil))
(set-buffer-modified-p nil)
(shell-command-on-region (point-min) (point-max) (read-shell-command ""))
(= 32 (following-char)) ; test if the next character is an ASCII space
(= (char-syntax (preceding-char)) ?w)
(if (menu-bar-non-minibuffer-window-p) (kill-buffer-if-not-modified (current-buffer)))
(save-excursion (beginning-of-buffer) (call-interactively 'replace-regexp))
(indent-rigidly (region-beginning) (region-end) 2)
(delete-file (buffer-file-name))
(file-writable-p (file-name-directory buffer-file-name))
(save-some-buffers t) ; also consider some buffers that are not visiting a file
(if (and (buffer-modified-p) (not buffer-read-only) (buffer-file-name)) (save-buffer))
(read-from-minibuffer "" (thing-at-point 'symbol))
(set-frame-size (selected-frame) 74 48)
(set-frame-position (selected-frame) 1100 22)
(frame-pixel-width (selected-frame))
(set-window-dedicated-p (selected-window) t) ; do not display other buffers in the current window
(cd "/tmp") ; change the default-directory of the current buffer
(current-column)
(line-number-at-pos)
(eq (syntax-class (syntax-after (point))) 5) ; test if the preceding character is a closing paren
(move-to-column (save-excursion (goto-char (mark)) (current-column)))
(max (region-beginning) (region-end))
(define-key ctl-h-map (kbd "C-l") 'find-library) ; C-h C-l to find-library
(define-key 'help-command (kbd "C-l") 'find-library) ; C-h C-l to find-library
(set-face-attribute 'mode-line nil :background "#ff0")
(string-equal (format-time-string "%u") "4")
(if (> (length (window-list)) 1) (delete-window))
(> (length (process-list)) 0)
(dolist (x (buffer-list)) (kill-buffer-if-not-modified x))
(revert-buffer-with-coding-system 'iso-latin-1)
(switch-to-buffer (generate-new-buffer "Untitled"))
(kill-new (buffer-substring-no-properties (point-min) (point-max)))
(delete-region (point) (save-excursion (forward-word 5) (point)))
(kill-new (buffer-substring-no-properties (point) (mark)))
(how-many "aa" (point-min) (point-max)) ; display how many lines match a regex
(re-search-forward "[^\x00-\x7e]") ; go to next non-ASCII character
(setq show-trailing-whitespace (not show-trailing-whitespace))
(insert (format-time-string "%Y-%m-%d"))
(= (following-char) ?\n)
(set-face-foreground 'minibuffer-prompt "white")
(minibuffer-window-active-p (minibuffer-window))
(fill-region (point-min) (point-max))
(and (bolp) (eolp)) ; test if the current line is empty
(re-search-forward "a+" nil t) ; search for a+ and do not show an error if there are no matches
(char-equal (char-after) 126) ; test if the next character is a tilde
(save-excursion (goto-char (point-min)) (comment-kill (count-lines (point-min) (point-max))))
(flush-lines "^$" (point-min) (point-max))
(clipboard-kill-ring-save (point) (line-end-position))
(kill-ring-save (line-beginning-position) (line-end-position))
(get-text-property (point) 'face)
(defun characterp (x) (and (integerp x) (> x 0) (<= x #x3fffff)))
(widget-button-press (point))
(how-many ")" (point) (line-beginning-position))
(window-buffer (next-window))
(eq (selected-window) (frame-first-window))
(current-kill 0 t) ; return the latest kill without moving the yanking point
(when (not (file-exists-p "/tmp/dir")) (make-directory "/tmp/dir"))
(dotimes (i 128) (insert (format "%4d \\%03o \\x%02x %c\n" i i i i)))
(message (prin1-to-string buffer-file-coding-system))
(delete-other-windows (get-buffer-window "*Help*"))
(setq outline-regexp "#") ; treat lines that start with a hash character as headings for outline-mode
(if (one-window-p) (split-window))
(with-current-buffer "*Shell Command Output*" (kill-region (point-min) (point-max)))
(set-window-buffer (next-window) "*Shell Command Output*")
(forward-button 1)
(= (line-number-at-pos) (line-number-at-pos (point-max)))
(buffer-name (process-buffer (car (last (process-list)))))
(comment-or-uncomment-region (line-beginning-position) (line-end-position))
(find-alternate-file (concat "/sudo:root@localhost:" buffer-file-name))
(defun my-reverse (list) (let ((r '())) (dolist (e list) (push e r)) r))
(add-text-properties (point-min) (point-max) '(face variable-pitch))
(version< emacs-version "24.1")
(find-file-other-window "~/.bashrc")
(browse-url (concat "http://google.com/search?q=" (url-hexify-string "aa")))
(and (looking-at "[ \t]$") (> (current-left-margin) 0))
(looking-at "[0-9]+") ; test if the text after the point matches [0-9]+
(looking-back "[0-9]+") ; test if the text before the point matches [0-9]+
(goto-line (line-number-at-pos) (window-buffer (next-window))
(with-current-buffer "*eshell*" (goto-char (point-max)) (insert "text") (eshell-send-input))
(server-eval-at "servername" '(+ 1 2))
(eval-minibuffer "Prompt: ") ; like (eval (read-minibuffer "Prompt: "))
(gethash (selected-window) which-func-table) ; current function
(load site-run-file 'no-error 'no-message) ; load site-start.el
(ignore-errors (read-from-minibuffer ""))
(char-to-string (char-after (point)))
(kill-all-local-variables) ; switch to fundamental mode, reset syntax table, etc
(goto-char (point-max)) ; like (end-of-buffer)
(split-window-vertically 10) ; split vertically and make the current window 10 rows tall
(split-window-vertically -10) ; split vertically and make the new window 10 rows tall
(format-time-string "%Y-%m-%d")
(delete-region (point) (progn (forward-line 1) (point))) ; like kill-line
(delete-region (line-beginning-position) (line-end-position)) ; like kill-whole-line
(delete-region (point) (progn (forward-word 1) (point))) ; like kill-word
(delete-region (point) (save-excursion (forward-sentence 1) (point))) ; like kill-sentence
(+ (random 6) 1)
(clipboard-kill-ring-save (line-beginning-position) (line-end-position))
(time-add (current-time) (seconds-to-time 30))
(url-copy-file "http://example.com" "/tmp/example.html")
(- (nth 3 (window-inside-pixel-edges)) (nth 1 (window-inside-pixel-edges))) ; get the height of the current window in pixels
(count-lines (window-start) (window-end)) ; get the number of visible lines in the current window
(eq this-command last-command)
(= ?w (char-syntax (char-before)))
(let ((inhibit-message t)) (message "aa")) ; inhibit echo area messages in Emacs 25
(with-current-buffer (get-buffer " *Echo Area 0*") (setq-local face-remapping-alist '((default (:height 0.9) variable-pitch)))) ; change the echo area face
(with-current-buffer "*scratch*" (write-file "/tmp/scratch"))
(x-popup-menu (list '(0 0) (selected-frame)) (mouse-menu-bar-map)) ; show menu bar items in a context menu
(if (region-active-p) (buffer-substring-no-properties (region-beginning) (region-end)) (thing-at-point 'symbol))
(let ((message-log-max nil)) (message "message")) ; display a message in the echo area without adding it to the *Messages* buffer
(set-face-attribute 'vertical-border nil :foreground "black") ; change the color of the vertical border between windows
```

## Misc

* evil is a successor to vimpulse and vim-mode which are no longer maintained
* viper is a basic vi emulation mode that comes with emacs, but evil, vimpulse, and vim-mode add features like visual selection and text objects
* ejacs is a JavaScript interpreter written in elisp
* git-timemachine displays old git versions
* rainbow-delimiters highlights parentheses with different colors based on nesting depth, and rainbow-blocks is a similar mode that highlights whole blocks
* diff-hl highlights uncommitted changes
* defadvice and letf are not allowed in Emacs source code
* hsymbols are case-insensitive in Common Lisp but case-sensitive in Emacs Lisp
* ;;; -*- lexical-binding: t -*- has enabled lexical binding since 24.1
* point-max is (1+ (buffer-size)) unless narrowing is in effect
* before-advice, after-advice, and around-advice are advice classes
* get-buffer-create returns an existing buffer or creates a new buffer, but generate-new-buffer always creates a new buffer
* /* -*- compile-command: "gcc -Wall" -*- */ changes the command used by M-x compile
* <right> invokes right-char in Emacs 24 and forward-char in Emacs 23
* (zerop (length "string")) is constant time, but (equal "string" "string") and (string-equal "string" "string") are linear time
* profile-dotemacs.el runs each sexp in .emacs through benchmark-run
* minor-mode-list is set to a list of all minor mode functions
* Emacs regular expressions do not support \d, \w, or \s
* Emacs regular expressions support \` and \' but not \A or \Z
* iswitchb-mode was made obsolete in Emacs 24.4
* (read t) reads from the minibuffer or from STDIN in batch mode, and (read nil) always reads from STDIN
* inactive minibuffers have the major mode minibuffer-inactive-mode
* the fifth argument to read-from-minibuffer defaults to minibuffer-history
* add-to-history removes duplicates if history-delete-duplicates is non-nil
* resize-mini-windows is set to grow-only by default
* max-mini-window-height is 0.25 by default
* enable-recursive-minibuffers is nil by default
* the emacs22 completion style is like the basic completion style but it ignores text after the point
* the partial-completion completion style splits words around spaces and hyphens
* the initials completion style makes for example lch match list-command-history
* completion-ignored-extensions contains for example .o and ~ by default
* winner-mode makes for example C-c <left> undo changes in window configuration
* kill-ring-max is set to 60 by default
* cider used to be called nrepl.el
* bookmarks are saved in ~/.emacs.d/bookmarks
* abnormal hooks end with -hooks or -functions
* scroll-up-command considers scroll-error-top-bottom but scroll-up does not
* the vertical-border face is used for the vertical border between windows in text terminals
* font-lock-maximum-decoration is set to t by default
* diff-switches is -c by default
* initial-major-mode is lisp-interaction-mode by default
* electric-indent-mode indents when electric-indent-functions returns non-nil
* electric-layout-mode automatically inserts newlines around some characters
* - indicates no special charset on the modeline, = indicates no conversion, and 1 indicates Latin-1
* C-z (suspend-display) calls iconify-or-deiconify-frame in a graphical display
* DEL is delete-backward-char and <deletechar> is delete-forward-char
* paragraph-indent-minor-mode causes paragraphs to be delimited by leading spaces
* a special display buffer is always displayed in a dedicated frame
* each symbol has a name, a value cell, a function cell, and a plist
* a disembodied plist is independent of any symbol
* a lambda expression is a sext that evaluates to a cons whose car is lambda
* an atom is a Lisp entity that is not a cons
* an alist is a list where each element is a cons
* (let ((a 1) (b 2)) (+ a b)) is equivalent to ((lambda (a b) (+ a b)) 1 2)
* -nw (--no-window-system) opens Emacs in a terminal ignoring DISPLAY
* --no-site-file disables loading site-start.el
* --debug-init shows information about errors in init files
* strings, vectors, char-tables, and bool-vectors are arrays
* strings can have text properties but vectors can not
* csexp is a binary encoding form for a subset of general sexps
* message-log-max is set to 50 by default
* window-system can be set to for example x, ns, w32, or nil
* prefix-numeric-value returns the numeric value of a raw prefix argument
* show-paren-mode highlights parentheses using show-paren-style after show-paren-delay seconds
* Man-switches is empty by default
* if package-install does not find a package, try to run package-refresh-contents
* 0 is whitespace, 1 is punctuation, 2 is word, 3 is symbol, and 4 is open parenthesis
* find-function, find-variable, and find-library are included in find-func.el
* adding comint-truncate-buffer to comint-output-filter-functions limits the length of shell buffers
* string= is an alias for string-equal
* string= ignores text properties
* hi-lock-line-face-buffer is an alias for highlight-lines-matching-regexp
* kill-all-local-variables does not remove variables with a non-nil permanent-local property
* bookmark-default-file is ~/.emacs.d/bookmarks by default
* (global-set-key "a" 'a) is like (define-key global-map "a" 'a)
* boundp returns t if the value of a symbol is not void, and fboundp returns t if the function definition of a symbol is not void
* term-buffer-maximum-size is 2048 by default but setting it to 0 disables truncating term buffers
* killall -SIGUSR2 Emacs makes Emacs attempt to break out of the current loop into the Lisp debugger
* filter-buffer-substring calls filter-buffer-substring-function, which is set to buffer-substring--filter by default
* kill-ring-save is similar to copy-region-as-kill but it also gives visual feedback that indicates the extent of the region that is copied
* scroll-other-window is bound to M-next and C-M-v and scroll-other-window-down is bound to M-prior and C-M-S-v
* with (global-set-key (kbd "C-h o") 'info-display-manual), C-h o coreutils RET i stat RET opens the section for stat from the coreutils info page

* (setq whitespace-style '(face)) enables all visualizations that use special faces
* M-x size-indication-mode shows the buffer size in the mode line
* line numbers are not shown if a buffer is larger than line-number-display-limit
* (setq display-time-24hr-format t) makes display-time-mode use a 24 hour clock
* display-battery-mode uses battery-mode-line-format
* (set-face-attribute 'mode-line nil :box nil) removes the borders around the mode line
* (setq mode-line-in-non-selected-windows nil) disables using the mode-line-inactive face
* (setq visible-cursor nil) makes text terminals use the visible cursor instead of the very visible cursor
* (setq cursor-in-non-selected-windows nil) hides the cursor in non-selected windows
* M-x toggle-truncate-lines changes the truncate-lines variable locally
* visual-line-mode changes C-a to beginning-of-visual-line
* (setq display-hourglass nil) disables changing the pointer to an hourglass
* hourglass-delay is 1 by default
* (setq make-pointer-invisible nil) disables hiding the pointer when typing
* underline-minimum-offset is 1 by default
* (setq isearch-lazy-highlight nil) disables highlighting other matches
* M-e is isearch-edit-string in isearch-mode-map
* (setq search-whitespace-regexp nil) disables lax space matching for isearch
* M-<TAB> is isearch-complete in isearch-mode-map
* C-w yanks a word, C-M-y yanks a character, and M-s C-e yanks the rest of the line in isearch-mode-map
* (setq isearch-allow-scroll t) makes C-v and M-v not exit isearch
* C-r searches in minibuffer history when the minibuffer is active
* M-s w is isearch-toggle-word when incremental search is active
* M-s w is isearch-forward-word when incremental search is not active
* M-r is isearch-toggle-regexp
* \= matches the empty string at the point
* \_< matches the beginning of a symbol and \_> matches the end of a symbol
* \s. matches punctuation characters and \s- matches whitespace characters
* \S. matches non-punctuation characters and \S- matches non-whitespace characters
* (setq case-fold-search nil) makes searching and matching functions consider case
* (setq tags-case-fold-search nil) makes tag operations consider case
* (setq replace-lax-whitespace t) enables lax space matching for query-replace
* \# is 0 during the first replacement, 1 during the second replacement, and so on
* \? prompts for a replacement
* \#& is the whole match converted to a number
* \#1 is the first backreference converted to a number
* M-x multi-isearch-buffers searches in multiple buffers
* M-x occur shows matching lines in a new buffer
* M-3 M-x occur shows three lines of context before and after each matching line
* pressing RET over a line in an occur buffer shows the line in the original buffer
* C-x \` selects the next occurrence in an occur buffer
* pressing e in an occur buffer enters occur-edit-mode
* C-c C-c exits occur-edit-mode
* list-matching-lines is an alias for occur
* M-s o runs occur when incremental search is active
* M-x multi-occur searches in multiple buffers
* M-x multi-occur-in-matching-buffers searches in buffers matching a regexp
* M-x how-many shows the number of matches for a regexp after the point
* undo-limit is 80000 by default, undo-strong-limit is 120000 by default, and undo-outer-limit is 120000000 by default
* M-x undo-only never redoes changes
* C-M-t is transpose-sexps
* M-x ispell applies to region or buffer
* M-x ispell-buffer applies to a buffer and M-x ispell-region applies to a region
* M-x flyspell-prog-mode enables flyspell for comments and strings
* <F3> is kmacro-start-macro-or-insert-counter
* <F4> is kmacro-end-or-call-macro
* C-u <F3> executes the last macro and then adds keys to it
* C-u C-u <F3> adds keys to the last macro
* (setq kmacro-execute-before-append nil) makes C-u <F3> not execute a macro
* C-x C-k r is apply-macro-to-region-lines
* C-x ( is kmacro-start-macro and C-x ) is kmacro-end-macro
* C-x e is kmacro-end-and-call-macro
* M-4 C-x ) executes a macro four times
* C-x C-k C-n is kmacro-cycle-ring-next and C-x C-k C-p is kmacro-cycle-ring-previous
* C-x C-k C-i inserts a counter starting from 1
* C-u C-x C-k C-i inserts a counter starting from 0
* C-x C-k C-f specifies a format for the counter
* M-5 C-x C-k C-a adds 5 to the counter and C-u C-x C-k C-a resets the counter
* C-x q is kbd-macro-query
* C-x C-k b gives a temporary keybinding for the last macro
* C-x C-k b 4 binds the last macro to C-x C-k 4
* C-x C-k n NAME RET gives a command name for the last macro
* M-x insert-kdb-macro RET NAME RET inserts Lisp code for the NAME macro
* C-x C-k C-e (kmacro-edit-macro) edits the last macro
* C-x C-k l (kmacro-edit-lossage) edits the last 300 keystrokes as a macro
* C-x C-k SPC is kmacro-step-edit-macro
* (setq insert-default-directory nil) disables inserting a default directory in the minibuffer
* large-file-warning-threshold is 10000000 by default
* C-x C-v (find-alternate-file) kills the current buffer and visits a new file
* (setq find-file-run-dired nil) disables invoking dired when visiting a directory
* M-x find-file-literally disables format conversion and automatic uncompression
* M-x find-file-literally ignores require-final-newline
* find-file-not-found-functions is run before find-file-hook
* M-~ is not-modified
* C-u M-~ marks the current buffer as changed
* M-x set-visited-file-name changes the name that is used when saving the buffer
* C-u C-x C-s backs up the buffer on the next save
* C-u C-u C-x C-s saves the previous file as a backup and saves the buffer
* M-x auto-revert-mode enables auto revert for the current buffer
* (setq global-auto-revert-non-file-buffers t) enables auto revert for all buffers
* the buffer menu reverts automatically every auto-revert-interval seconds
* (setq auto-save-visited-file-name t) performs auto-save in place
* (setq delete-auto-save-files nil) disables deleting auto-save files on save
* auto-save-interval is 300 by default and auto-save-timeout is 30 by default
* M-x recover-file restores an auto-save file
* M-x recover-session recovers auto-save files from the previous session
* (setq find-file-visit-truename t) enables resolving symlinks when visiting files
* C-u C-x C-d shows a verbose directory listing
* list-directory-brief-switches is -CF by default
* list-directory-verbose-switches is -l by default
* (setq delete-by-moving-to-trash t) makes M-x delete-file use the trash
* (setq trash-directory "~/.Trash") changes the trash directory
* diff-switches is -c by default
* M-n is diff-hunk-next in diff-mode
* M-x make-symbolic-link creates a symbolic link
* M-x add-name-to-file creates a hard link
* chmod is an alias for set-file-modes
* in tar-mode e extracts a file, v opens a file in view mode, and o opens a file in a new window
* (setq ange-ftp-make-backup-files t) enables backups for files accessed via ftp
* C-<tab> completes from the file name cache in the minibuffer
* M-x file-cache-add-directory RET /dir RET adds files in /dir to the file cache
* M-x recentf-save-list saves recentf-file-list to a file
* (filesets-init) enables filesets
* M-x filesets-add-buffer RET NAME RET adds a buffer to the fileset NAME
* M-x filesets-open visits all files in a fileset
* C-u M-g M-g goes to a line in the previous buffer
* M-x view-buffer opens a buffer in view-mode
* M-x kill-matching-buffers kills buffers whose names match a regexp
* M-x clean-buffer-list kills buffers that have not been visited in three days by default
* midnight-hook includes only clean-buffer-list by default
* C-x 4 c is clone-indirect-buffer-other-window
* truncate-partial-width-windows is 50 by default
* C-x 4 C-o (iswitchb-display-buffer) opens a buffer in another window without selecting the window
* C-x 4 0 is kill-buffer-and-window
* C-x ^ (enlarge-window) makes a window taller
* C-x - is shrink-window-if-larger-than-buffer
* C-x + (balance-windows) makes windows the same width or height
* buffers in same-window-buffer-names are always displayed in the selected window
* (setq pop-up-frames t) makes display-buffer create new frames
* (windmove-default-keybindings) binds for example <S-right> to windmove-right
* C-x 5 1 is delete-other-frames and C-x 5 2 is make-frame-command
* (setq use-dialog-box nil) makes mouse commands not use graphical dialogs
* enable-multibyte-characters is non-nil in multibyte buffers
* C-h L is describe-language-environment
* C-h L UTF RET describes the UTF-8 language environment
* exit-language-environment-hook is run before set-language-environment-hook
* C-h C is describe-coding-system
* C-h C utf-8-unix RET  describes the utf-8-unix coding system
* the raw-text coding system sets enable-multibyte-characters to nil
* C-x RET r is revert-buffer-with-coding-system
* C-x RET f dos RET enables using CRLF line endings when saving the buffer
* emacs -fn fontset-standard uses the standard fontset instead of the default fontset
* standard-fontset-spec is -*-fixed-medium-r-normal-*-16-*-*-*-*-*-fontset-standard
* the japanese-jisx0208 charset has the highest priority in the Japanese language environment
* -*-Lisp-*- is equivalent to -*-mode:Lisp;-*-
* interpreter-mode-alist contains elements like ("bash" . sh-mode)
* auto-mode-alist contains elements like ("\\.rb\\'" . ruby-mode) and ("\\.bz2\\'" nil jka-compr)
* magic-fallback-mode-alist contains elements like `("<\\?xml " . xml-mode)`
* M-x indent-relative indents a line to have the same indentation level as the previous non-blank line
* C-M-o is split-line
* (setq indent-tabs-mode nil) makes indentation commands use spaces
* M-x untabify converts tabs to spaces based on tab-width
* (setq indent-for-tab-command t) makes tab attempt completion if the current line is already indented
* (setq indent-for-tab-command nil) makes tab indent only at the left margin and at the indentation
* C-x [ is backward-page, C-x C-p is mark-page, and C-x l is count-lines-page
* C-x f is set-fill-column
* M-o M-s (center-line) centers a line within the current fill column
* breaking a line is disabled if a function in fill-nobreak-predicate returns non-nil
* C-x . is set-fill-prefix
* M-x fill-individual-paragraphs fills paragraphs delimited by changes in indentation
* lines that do not start with the fill prefix are considered to start a paragraph
* M-<TAB> is ispell-complete-word in text mode
* outline-mode uses C-c as a prefix and outline-minor-mode uses C-c @ as a prefix
* C-c C-n is outline-next-visible-heading in outline-mode
* C-c C-f is outline-forward-same-level and C-c C-u is outline-up-heading in outline-mode
* C-c C-c is hide-entry and C-c C-e is show-entry in outline mode
* M-x reveal-mode enables automatically unhiding text near the point in outline mode
* (eval-after-load "outline" '(require 'foldout)) adds folding commands to outline mode
* foldout binds C-c C-z to foldout-zoom-subtree in outline mode
* C-c C-t is org-todo, C-c C-s is org-schedule, and C-c C-d is org-deadline
* tex-default-mode is latex-mode by default
* latex-mode, plain-tex-mode, and doctex-mode are child modes of tex-mode
* C-c { (tex-insert-braces) inserts braces and C-c } (up-list) moves to a closing brace in tex-mode
* C-c C-o (tex-latex-block) inserts \begin and \end in latex-mode
* C-c C-e is tex-close-latex-block in latex-mode
* latex-electric-env-pair-mode inserts \end tags automatically
* C-c C-b is tex-buffer, C-c C-r is tex-region, and C-c C-f is tex-file
* C-c C-p is tex-print
* C-c C-v (tex-view) shows the output of a command like tex-buffer in an external program
* C-c C-v uses tex-dvi-view-command and C-c C-p uses tex-dvi-print-command
* C-c C-l scrolls a *tex-shell* buffer so that the last line is visible
* C-c C-k is tex-kill-job
* the header used by C-c C-r starts with \documentclass or \documentstyle in latex mode
* tex-start-commands is "\\nonstopmode\\input" by default
* C-c <TAB> (tex-bibtex-file) runs tex-bibtex-command to produce a .bbl file
* C-c C-n (sgml-name-char) inserts a named entity in sgml mode and HTML mode
* C-c C-t (sgml-tag) inserts an opening and closing tag
* C-c / is sgml-close-tag
* C-c C-f is sgml-skip-tag-forward and C-c C-d is sgml-delete-tag
* 2C-two-columns is bound to <F2> 2 and C-x 6 2
* C-M-h is c-mark-function in C mode
* M-x imenu jumps to a definition
* M-x indent-code-rigidly indents code but not comments or strings
* C-M-q is c-indent-exp in C mode and indent-pp-sexp in Lisp mode
* c-indent-exp and indent-pp-sexp are like mark-sexp (C-M-SPC) followed by indent-region (C-M-\)
* C-c C-q is c-indent-defun in C mode
* <TAB> is c-indent-command in C mode
* c-tab-always-indent is t by default
* C-c . (c-set-style) changes the indentation style in C mode
* C-M-<SPC> is mark-sexp
* C-M-n is forward-list, C-M-p is backward-list, C-M-u is backward-up-list, and C-M-d is down-list
* blink-matching-delay is 1 by default
* C-u M-; (comment-kill) kills a comment on the current line
* C-x ; is comment-set-column
* comment-region is bound to C-c C-c in C-like modes
* C-c @ C-h is hs-hide-block and C-c @ C-s is hs-show-block
* C-c @ C-c is hs-toggle-hiding
* C-c @ C-M-h is hs-hide-all and C-c @ C-M-s is hs-show-all
* C-c @ C-l is hs-hide-level
* (setq hs-hide-comments-when-hiding-all t) makes hs-hide-all also hide comments
* C-M-i is completion-at-point in many programming modes
* completion-at-point uses semantic parser data for completion when semantic mode is enabled
* M-x glasses-mode adds underscores to camel case words
* M-x semantic-mode makes some modes use a semantic parser instead of syntax tables
* semantic mode applies to C, C++, Scheme, JavaScript, Java, HTML, and Make
* C-c , j is semantic-complete-jump-local and C-c , J is semantic-complete-jump
* C-c , <SPC> (semantic-complete-analyze-inline) shows a list of completions for a symbol at point
* C-c , l (semantic-analyze-possible-completions) shows a list of completions in another window
* C-c C-l is c-toggle-electric-state and C-c C-a is c-toggle-auto-newline
* C-c <DEL> (c-hungry-delete-backwards) deletes whitespace before the point
* C-c C-d (c-hungry-delete-forward) deletes whitespace after the point
* (subword-mode 1) enables treating uppercase characters in camelcase identifiers as word boundaries
* C-c C-s (c-show-syntactic-information) shows syntactic information abount the current line
* cwarn-mode highlights for example assignments in expressions and semicolons after if, for, and while
* M-x ff-find-related-file finds a corresponding header or source file
* M-x recompile invokes a compiler with the same command as the last invocation of M-x compile
* the default compile-command is make -k where -k continues after errors
* M-g n is next-error and M-g p is previous-error
* M-} is compilation-next-file and M-{ is compilation-previous-file in compilation mode
* C-c C-f toggles next-error-follow-minor-mode in compilation mode
* compilation-skip-threshold is 1 by default
* (setq compilation-skip-threshold 2) makes next-error and previous-error also skip warnings
* compilation-error-regexp-alist is used to match errors
* find-grep is an alias for grep-find
* (setq grep-highlight-matches t) enables --color
* M-x lgrep is like M-x grep but it uses prompts to construct the grep command
* M-x rgrep is like M-x grep-find but it uses prompts to construct the grep command
* grep-files-aliases makes for example ch match *.[ch]
* grep-find-ignored-directories is used by rgrep but not by grep-find
* grep-find-ignored-directories includes for example .git and .svn by default
* M-x load-library loads a file in load-path
* C-M-x (eval-defun) evaluates the top-level form containing the point or after the point
* C-u M-: inserts the result
* C-j is eval-print-last-sexp in the scratch buffer
* M-x run-lisp starts a Lisp session and M-x run-scheme starts a Scheme session
* - indicates that a file is unmodified
* : indicates that a file has been modified
* ! indicates that a file contains merge conflicts or was removed from version control
* ? indicates that a file is missing from the working tree
* C-x v v is vc-next-action
* M-x emerge-files merges files and M-x emerge-buffers merges buffers
* C-x a g (add-global-abbrev) adds an abbreviation for the word before the point
* C-u 0 M-x a g adds an abbreviation for the region
* M-x define-global-abbrev asks for both an abbreviation and an expansion
* M-x abbrev-mode enables expanding abbreviations after whitespace and punctuation characters
* C-x a e (expand-abbrev) expands an abbrev before point
* C-u - C-x a g removes an abbrev definition
* M-x kill-all-abbrevs removes all abbrev definitions
* abbrev-expand-functions is run when an abbreviation is expanded
* M-x edit-abbrevs is the same as M-x list-abbrevs but it moves focus to the *Abbrevs* buffer
* M-x write-abbrev-file and M-x read-abbrev-file default to abbrev-file-name or ~/.emacs.d/abbrev_defs
* quietly-read-abbrev-file is like read-abbrev-file but it does not display a message in the echo area
* (setq save-abbrevs nil) makes C-x s and C-x C-c not save abbrevs
* M-x insert-abbrevs inserts a description of all abbrevs to the current buffer
* C-M-/ is dabbrev-completion
* (setq dabbrev-check-all-buffers nil) makes M-/ not search other buffers
* dabbrev-case-fold-search is case-fold-search by default
* q (quit-window) buries a dired buffer
* <SPC> and n are equivalent to C-n in dired
* d is dired-flag-file-deletion and x is dired-do-flagged-delete
* <DEL> (dired-unmark-backward) unmarks a line and moves to the previous line
* # flags all autosave files and ~ flags all backup files
* . (dired-clean-directory) marks all but the oldest and newest few backups of each file for deletion
* the files kept by dired-clean-directory are determined by dired-kept-versions and kept-old-versions
* % & (dired-flag-garbage-files) marks files that match dired-garbage-files-regexp
* dired-garbage-files-regexp matches .aux, .bak, .log, and .orig by default
* % d (dired-flag-files-regexp) marks files that match a regex
* f and e are dired-find-file
* o is dired-find-file-other-window
* C-o (dired-display-file) is like o but it does not select the other window
* v (dired-view-file) opens a file in view mode
* ^ is dired-up-directory
* */ is dired-mark-directories and * s is dired-mark-subdir-files
* * * is dired-mark-executables and * @ is dired-mark-symlinks
* U is dired-unmark-all-marks
* t is dired-toggle-marks
* (setq dired-dwim-target t) uses a directory in another dired window as the default target directory
* C is dired-do-copy, R is dired-do-rename, and D is dired-do-delete
* (setq dired-copy-preserve-time t) makes dired-do-copy act like cp -p
* D (dired-do-delete) applies to marked files and x (dired-do-flagged-delete) applies to flagged files
* H is dired-do-hardlink and S is dired-do-symlink
* M is dired-do-chmod, O is dired-do-chown, and G is dired-do-chgrp
* T is dired-do-touch
* Z (dired-do-compress) uncompresses or compresses files
* B (dired-do-byte-compile) byte compiles elisp files
* A (dired-do-search) searches in the marked files
* Q (dired-do-query-replace-regexp) performs query-replace-regexp in the marked files
* M-, goes to the next result for A or Q
* ! is dired-do-shell-command and & is dired-do-async-shell-command
* ! and & replace * surrounded by whitespace with filenames and take multiple files at a time
* ! and & replace ? surrounded by whitespace with filenames and run the command once for each file
* ! and & do not update the dired buffer
* % R ^.*$ <RET> aa-\& <RET> prepends aa- to filenames
* a numeric argument of zero makes R and C consider directory names
* C-u k removes a subdirectory
* l is dired-do-redisplay
* C-u s SWITCHES RET specifies a new value for dired-listing-switches
* M-x find-name-dired finds files by name and M-x find-grep-dired finds files by contents
* M-x find-dired allows specifying arguments for find
* find-ls-option is used by find-name-dired, find-grep-dired, and find-dired
* C-x C-q (dired-toggle-read-only) enters wdired mode
* C-c C-c (wdired-finish-edit) exits wdired mode and applies changes
* M-x image-dired shows a directory in an image-dired buffer
* C-t d (image-dired-display-thumbs) shows thumbnails for the marked files
* image tags are stored in image-dired-db-file
* + is dired-create-directory
* w (dired-copy-filename-as-kill) copies basenames and M-0 w copies absolute paths
* M-s a C-s (dired-do-isearch) searches in the marked files
* M-x shell reads ~/.emacs_* where * is the name of the invoked shell
* M-x shell sets EMACS to t and INSIDE_EMACS to a value like 24.3.1,comint
* (setq shell-completion-fignore '("~" "#" "%")) ignores files ending with ~, #, or %
* M-? is comint-dynamic-list-filename-completions
* C-d is comint-delchar-or-maybe-eof
* C-c C-a is comint-bol-or-process-mark
* C-c <SPC> inserts a newline
* C-c C-c is comint-interrupt-subjob and C-c C-\ is comint-quit-subjob
* C-c C-o (comint-delete-output) deletes the output of the previous command
* C-c C-s (comint-write-output) writes the output of the previous command to a file
* comint-show-output (C-c C-r or C-M-l) scrolls to the top of the output of the previous command
* C-c C-b moves a command matching shell-command-regexp backward
* C-c C-f moves a command matching shell-command-regexp forward
* (setq comint-use-prompt-regexp t) disables dividing comint buffers to prompt and output fields
* shell-prompt-pattern is used to recognize prompts if comint-use-prompt-regexp is non-nil
* shell-prompt-pattern is always used to delimit paragraphs
* shell-prompt-pattern is "^[^#$%>\n]*[#$%>] *" by default
* M-p selects the previous command, M-n selects the next command, and M-r and M-s search in history
* C-c . inserts the last argument of the previous command
* C-c C-l (comint-dynamic-list-input-ring) shows command history in another buffer
* C-c C-x is comint-get-next-from-history
* C-c C-p is comint-previous-prompt and C-c C-n is comint-next-prompt
* C-C <RET> (comint-copy-old-input) inserts the line at point
* Mouse-2 (comint-insert-input) inserts an input command
* comint-insert-input requires comint-user-prompt-regexp to be set to nil
* setting comint-input-autoexpand to input enables expanding history references when sending a command
* binding space to comint-magic-space makes space perform history expansion
* (setq comint-scroll-to-bottom-on-input t) makes insertion and yank commands scroll to the bottom
* (setq comint-input-ignoredups) removes successive duplicate inputs from the input history
* (setq comint-completion-addsuffix t) adds a space or slash after a fully completed file or directory name
* (setq comint-completion-autolist t) lists completions when the completion is not exact
* in line mode term-mode acts like shell-mode
* in char mode each character except C-c is sent directly to the subshell
* term-mode uses faces like term-color-red and term-color-bold
* you can make another term-mode buffer by renaming the first buffer with M-x rename-uniquely
* shell-mode tracks the current directory by examining the input but term-mode does not
* some shells like bash support indicating the current directory to term-mode automatically
* C-c C-j is term-line-mode and C-c C-k is term-char-mode
* C-c C-q toggles displaying one page of output at a time
* you can run another emacs server by changing the server-name variable
* C-x # (server-edit) saves a file and tells emacsclient to exit if there are no more files
* emacsclient -s specifies a server name
* emacsclient -c creates a new client frame
* M-x kill-emacs kills Emacs when Emacs is started as a daemon
* M-2 M-x sort-fields sorts by the second field
* M-2 M-x sort-numeric-fields sorts by the second field numerically
* M-x reverse-region reverses lines
* M-x sort-columns sorts lines by the columns between the point and the mark
* (desktop-save-mode 1) enables saving and restoring the desktop automatically
* M-x desktop-revert reverts to the previously loaded desktop
* M-x desktop-clear kills all buffers except internal buffers
* C-M-c is exit-recursive-edit
* C-] (abort-recursive-edit) is like C-M-c but it aborts the command that requested the recursive edit
* M-x top-level exits all recursive editing levels
* M-x browse-url opens a URL and M-x browse-url-at-point opens a URL at point
* M-x goto-address-mode buttonizes URLs and email addresses in the current buffer
* C-c <RET> is goto-address-at-point in goto-address-mode
* in the package menu i is package-menu-mark-install, U is package-menu-mark-upgrades, and x is package-menu-execute
* setting package-enable-at-startup to nil disables loading packages automatically
* package-initialize can be used to load packages when package-enable-at-startup is set to nil
* a package file can be an elisp file or a tar file
* M-x package-install-file installs a package from a package file
* package-user-dir is ~/.emacs.d/elpa by default
* M-x customize-apropos searches for options, faces, and groups to customize
* M-x customize-option customizes a specific option
* M-x customize-browse creates a tree browser for the customize hierarchy
* C-M-i (widget-complete) completes values like file names and command names in a customization field
* C-c C-c is Custom-set and C-x C-s is Custom-save
* M-x customize-themes opens a buffer for custom themes
* (setq custom-safe-themes t) treats all custom themes as safe
* the currently used custom theme or themes are stored in custom-enabled-themes
* M-x load-theme loads a specific custom theme from a file
* M-x enable-theme enables a specific custom theme that has been loaded before
* M-x customize-create-theme opens a buffer for creating a custom theme
* the names of abnormal hooks end with -functions or -hooks instead of -hook
* M-x make-local-variable makes a variable local
* M-x kill-local-variable makes a local variable global
* setq-default changes the global value of a variable even when the variable has a local value
* C-x is ctl-x-map, C-h is help-map, C-x 4 is ctl-x-4-map, and C-c is mode-specific-map
* minibuffer-local-completion-map is used for permissive completion
* minibuffer-local-must-match-map is used for strict completion and cautious completion
* (put 'delete-region 'disabled t) disables the delete-region command
* (modify-syntax-entry ?\$ "." text-mode-syntax-table) makes dollar sign a punctuation character in text mode

## Example Emacs Config

```lisp
; Make `C-w` kill the current line when the mark is not active.
(defadvice kill-region (before slick-cut activate compile)
  (interactive
   (if mark-active
       (list (region-beginning) (region-end))
     (list (line-beginning-position) (line-beginning-position 2)))))

; Make `M-w` copy the current line when the mark is not active.
(defadvice kill-ring-save (before slick-copy activate compile)
  (interactive
   (if mark-active
       (list (region-beginning) (region-end))
     (list (line-beginning-position) (line-beginning-position 2)))))

(defun save-and-browse-url-of-buffer ()
  (interactive)
  (if (buffer-modified-p) (save-buffer))
  (browse-url-of-buffer))

(global-set-key (kbd "s-O") 'save-and-browse-url-of-buffer)

(defun rm ()
  (interactive)
  (let ((filename (buffer-file-name))
        (buffer (current-buffer))
        (name (buffer-name)))
    (if (not (and filename (file-exists-p filename)))
        (error "Buffer '%s' is not visiting a file!" name)
      (set-buffer-modified-p nil)
      (kill-buffer buffer)
      (delete-file filename))))

(global-set-key (kbd "<H-backspace>") 'rm)

(defun toggle-comment ()
  (interactive)
  (save-excursion
    (let (beg end)
      (if (region-active-p)
          (progn
            (setq beg (region-beginning) end (region-end))
            (goto-char beg)
            (setq beg (line-beginning-position))
            (goto-char end)
            (if (bolp) (backward-char))
            (setq end (line-end-position)))
        (setq beg (line-beginning-position) end (line-end-position)))
      (comment-or-uncomment-region beg end))))

(defun comment-paragraph ()
  (interactive)
  (save-excursion
    (mark-paragraph)
    (toggle-comment)))

(global-set-key (kbd "M-;") 'toggle-comment)
(global-set-key (kbd "M-'") 'comment-paragraph)

(defun unfill-paragraph ()
  (interactive)
  (let ((fill-column (point-max)))
    (fill-paragraph nil)))

(global-set-key (kbd "M-Q") 'unfill-paragraph)

(defun yank-and-mark ()
  (interactive)
  (let ((deactivate-mark nil))
    (yank)
    (exchange-point-and-mark)))

(global-set-key (kbd "C-z") 'yank-and-mark)

(defun yank-and-indent ()
  (interactive)
  (yank)
  (call-interactively 'indent-region))

(global-set-key (kbd "H-y") 'yank-and-indent)

(defun kill-first-page ()
  (interactive)
  (beginning-of-buffer)
  (scroll-up-command)
  (kill-region 1 (point)))

(global-set-key (kbd "H-v") 'kill-first-page)

(defun duplicate-line (&optional n)
  (interactive "*p")
  (let ((use-region (use-region-p)))
    (save-excursion
      (let ((text (if use-region
                      (buffer-substring (region-beginning) (region-end))
                    (prog1 (thing-at-point 'line)
                      (end-of-line)
                      (if (< 0 (forward-line 1))
                          (newline))))))
        (dotimes (i (abs (or n 1)))
          (insert text))))
    (if use-region nil
      (let ((pos (- (point) (line-beginning-position))))
        (if (> 0 n)
            (comment-region (line-beginning-position) (line-end-position)))
        (forward-line 1)
        (forward-char pos)))))

(global-set-key (kbd "H-d") 'duplicate-line)

(defun shift-region (x)
  (interactive)
  (let (beg end deactivate-mark)
    (if (region-active-p)
        (progn
          (setq beg (region-beginning) end (region-end))
          (save-excursion
            (setq beg (progn (goto-char beg) (line-beginning-position))
                  end (progn (goto-char end) (line-end-position)))))
      (setq beg (line-beginning-position)
            end (line-end-position)))
    (indent-rigidly beg end x)))

(global-set-key (kbd "s-u") (lambda () (interactive) (shift-region -2)))
(global-set-key (kbd "s-y") (lambda () (interactive) (shift-region 2)))
(global-set-key (kbd "s-U") (lambda () (interactive) (shift-region -1)))
(global-set-key (kbd "s-Y") (lambda () (interactive) (shift-region 1)))

(defun kill-whole-paragraph ()
  (interactive)
  (mark-paragraph)
  (kill-region (region-beginning) (region-end)))

(defun copy-whole-paragraph ()
  (interactive)
  (save-excursion
    (mark-paragraph)
    (kill-ring-save (region-beginning) (region-end))))

(global-set-key (kbd "H-w") 'kill-whole-paragraph)
(global-set-key (kbd "H-h") 'copy-whole-paragraph)

; This is like `M-x erase-buffer` but this adds contents of the buffer
; to the kill ring.
(defun kill-whole-buffer ()
  (interactive)
  (kill-region (point-min) (point-max)))

(defun copy-whole-buffer ()
  (interactive)
  (kill-ring-save (point-min) (point-max)))

(global-set-key (kbd "H-u") 'kill-whole-buffer)
(global-set-key (kbd "H-b") 'copy-whole-buffer)

(defun copy-word ()
  (interactive)
  (let ((bounds (bounds-of-thing-at-point 'word)))
    (copy-region-as-kill (car bounds) (cdr bounds))))

(global-set-key (kbd "H-g") 'copy-word)

(defun shell-command-replace ()
  (interactive)
  (let ((cmd (read-from-minibuffer "" nil nil nil 'shell-command-history))
        (p (if mark-active (region-beginning) 0))
        (m (if mark-active (region-end) 0)))
    (if (= p m)
        (shell-command cmd)
      (shell-command-on-region p m cmd t t))))

(defun shell-command-insert ()
  (interactive)
  (let ((cmd (read-from-minibuffer "" nil nil nil 'shell-command-history))
        (p (if mark-active (region-beginning) 0))
        (m (if mark-active (region-end) 0)))
    (if (= p m)
        (shell-command cmd t)
      (shell-command-on-region p m cmd))))

(global-set-key (kbd "M-r") 'shell-command-replace)
(global-set-key (kbd "M-i") 'shell-command-insert)

(defun mark-line ()
  (interactive)
  (let (beg end)
    (if (region-active-p)
        (progn
          (setq beg (region-beginning) end (region-end))
          (save-excursion
            (setq beg (progn (goto-char beg) (line-beginning-position))
                  end (progn (goto-char end) (line-end-position)))))
      (setq beg (line-beginning-position)
            end (line-end-position)))
    (goto-char end)
    (set-mark beg)))

(global-set-key (kbd "C-l") 'mark-line)

(defun my-newline-and-indent ()
  (interactive)
  (if (and (eolp) (bolp)) (newline) (newline-and-indent)))

(global-set-key (kbd "<RET>") 'my-newline-and-indent)

(defun open-line-above ()
  (interactive)
  (beginning-of-line)
  (newline)
  (forward-line -1)
  (indent-according-to-mode))

(defun open-line-below ()
  (interactive)
  (end-of-line)
  (newline-and-indent))

(defun open-line-above-without-indentation ()
  (interactive)
  (beginning-of-line)
  (newline)
  (forward-line -1))

(defun open-line-below-without-indentation ()
  (interactive)
  (end-of-line)
  (newline))

(global-set-key (kbd "<S-return>") 'open-line-above)
(global-set-key (kbd "<s-return>") 'open-line-below)
(global-set-key (kbd "<C-return>") 'open-line-above-without-indentation)
(global-set-key (kbd "<M-return>") 'open-line-below-without-indentation)

(defun kill-to-indentation ()
  (interactive)
  (let ((end (point)))
    (back-to-indentation)
    (kill-region (point) end)))

(global-set-key (kbd "<C-backspace>") 'kill-to-indentation)

(defun kill-to-beginning-of-buffer ()
  (interactive)
  (kill-region (point-min) (point)))

(defun kill-to-end-of-buffer ()
  (interactive)
  (kill-region (point) (point-max)))

(global-set-key (kbd "H-,") 'kill-to-beginning-of-buffer)
(global-set-key (kbd "H-.") 'kill-to-end-of-buffer)

(defun copy-to-beginning-of-line ()
  (interactive)
  (kill-ring-save (line-beginning-position) (point)))

(defun copy-to-end-of-line ()
  (interactive)
  (kill-ring-save (point) (line-end-position)))

(global-set-key (kbd "H-a") 'copy-to-beginning-of-line)
(global-set-key (kbd "H-e") 'copy-to-end-of-line)

(defun delete-indentation-and-spaces ()
  (interactive)
  (delete-indentation)
  (delete-horizontal-space))

(global-set-key (kbd "s-6") 'delete-indentation-and-spaces)

(defun save-and-kill-this-buffer ()
  (interactive)
  (if (and (buffer-modified-p) (not buffer-read-only) (buffer-file-name)) (save-buffer))
  (kill-this-buffer))

(global-set-key (kbd "s-w") 'save-and-kill-this-buffer)

(defun copy-lines-without-newline ()
  (interactive)
  (let (beg end)
    (if (region-active-p)
        (progn
          (setq beg (region-beginning) end (region-end))
          (save-excursion
            (setq beg (progn (goto-char beg) (line-beginning-position))
                  end (progn (goto-char end) (line-end-position)))))
      (setq beg (line-beginning-position)
            end (line-end-position)))
    (clipboard-kill-ring-save beg end)))

(defun kill-lines-without-newline ()
  (interactive)
  (let (beg end)
    (if (region-active-p)
        (progn
          (setq beg (region-beginning) end (region-end))
          (save-excursion
            (setq beg (progn (goto-char beg) (line-beginning-position))
                  end (progn (goto-char end) (line-end-position)))))
      (setq beg (line-beginning-position)
            end (line-end-position)))
    (kill-region beg end)))

(global-set-key (kbd "H-m") 'copy-lines-without-newline)
(global-set-key (kbd "H-q") 'kill-lines-without-newline)

(defun reverse-zap-to-char (x) "" (interactive "*cZap to char: ")
  (let ((case-fold-search nil))
    (kill-region (point) (progn (search-backward (char-to-string x)) (point)))))

(defun exclusive-zap-to-char (x) "" (interactive "*cZap to char: ")
  (let ((case-fold-search nil))
    (kill-region (point) (progn (search-forward (char-to-string x)) (backward-char) (point)))))

(defun exclusive-reverse-zap-to-char (x) "" (interactive "*cZap to char: ")
  (let ((case-fold-search nil))
    (kill-region (point) (progn (search-backward (char-to-string x)) (forward-char) (point)))))

(global-set-key (kbd "s-z") 'reverse-zap-to-char)
(global-set-key (kbd "H-x") 'exclusive-zap-to-char)
(global-set-key (kbd "H-z") 'exclusive-reverse-zap-to-char)

(global-set-key (kbd "H-f") (lambda () (interactive) (ido-find-file-in-dir "~/")))
(global-set-key (kbd "H-n") (lambda () (interactive) (ido-find-file-in-dir "~/n")))

(global-font-lock-mode 0)

(global-set-key (kbd "<s-backspace>") (lambda () (interactive) (kill-line -0)))

; Exchange the point and mark, deactivate the mark if it is active,
; and do not reactivate it if it is not.
(global-set-key (kbd "s-x") (lambda () (interactive) (exchange-point-and-mark t)))

(global-set-key (kbd "<s-up>") (lambda () (interactive) (scroll-down 8)))
(global-set-key (kbd "<s-down>") (lambda () (interactive) (scroll-up 8)))

; Make for example `C-h o coreutils RET` open the coreutils Info page.
(global-set-key (kbd "C-h o") 'info-display-manual)

; Make `C-h e search-phrase RET` like `C-h i g (elisp) RET i search-phrase RET`.
(global-set-key (kbd "C-h e") 'elisp-index-search)

; Append the contents of the region to a file.
(global-set-key (kbd "H-2") 'append-to-file)

(global-set-key (kbd "s-~") (lambda () (interactive) (find-file "~/.emacs.d/custom-theme.el")))
(global-set-key (kbd "H-`") (lambda () (interactive) (custom-theme-visit-theme 'custom)))
(global-set-key (kbd "s-`") (lambda () (interactive) (save-some-buffers t) (load-file "~/.emacs.d/custom-theme.el")))

(global-set-key (kbd "H-9") (lambda() (interactive) (switch-to-buffer "*interpretation*")))
(global-set-key (kbd "s-K") 'kill-compilation)
(global-set-key (kbd "s-I") (lambda () (interactive) (kill-buffer "*interpretation*")))

(global-set-key (kbd "s-f") 'ido-find-file)
(global-set-key (kbd "s-F") 'ido-find-file-other-window)
(global-set-key (kbd "s-b") 'ido-switch-buffer)
(global-set-key (kbd "s-B") 'ido-switch-buffer-other-window)
(global-set-key (kbd "s-e") 'previous-buffer)
(global-set-key (kbd "s-i") 'next-buffer)
(global-set-key (kbd "s-t") 'other-window)
(global-set-key (kbd "s-o") 'delete-other-windows)
(global-set-key (kbd "s-d") 'delete-window)
(global-set-key (kbd "s-p") 'backward-paragraph)
(global-set-key (kbd "s-n") 'forward-paragraph)
(global-set-key (kbd "s-k") 'kill-this-buffer)
(global-set-key (kbd "s-s") (lambda () (interactive) (save-some-buffers t)))
(global-set-key (kbd "s-\\") 'indent-region)
(global-set-key (kbd "s-8") 'scroll-other-window-down)
(global-set-key (kbd "s-9") 'scroll-other-window)

(global-set-key (kbd "C-,") 'beginning-of-buffer)
(global-set-key (kbd "C-.") 'end-of-buffer)
(global-set-key (kbd "C-6") 'delete-indentation)

(global-set-key (kbd "C-7") (lambda () (interactive) (insert "ä")))
(global-set-key (kbd "C-8") (lambda () (interactive) (insert "ö")))
(global-set-key (kbd "C-9") (lambda () (interactive) (insert "Ä")))
(global-set-key (kbd "C-0") (lambda () (interactive) (insert "Ö")))

(setenv "LANG" "en_US.UTF-8")

(setenv "MANWIDTH" "80")

; Save buffers when changing to another application. `focus-out-hook`
; was added in Emacs 24.4. Setting `inhibit-message` to `t` disables
; the message about what files are saved, which would otherwise even
; be shown over the minibuffer when the minibuffer is active.
; `inhibit-message` was added in Emacs 25.
(add-hook 'focus-out-hook (lambda () (let ((inhibit-message t)) (save-some-buffers t))))

(defadvice switch-to-buffer (before save-buffer-now activate)
  (when buffer-file-name (let ((inhibit-message t)) (save-some-buffers t))))

(defadvice other-window (before other-window-now activate)
  (when buffer-file-name (let ((inhibit-message t)) (save-some-buffers t))))

; Automatically revert a buffer when its file changes on disk.
(global-auto-revert-mode 1)

; Open Emacs in full screen by default.
(setq initial-frame-alist '((fullscreen . fullboth)))

; Make `shell-command` and `shell-command-on-region` use a newer
; version of Bash and make them invoke Bash as a login shell so that
; it reads `~/.bash_profile`.
(setq shell-file-name "/usr/local/bin/bash")
(setq shell-command-switch "-lc")

; Wrap text at word boundaries. `(visual-line-mode t)` also does that,
; but it makes commands like `C-a`, `C-e`, and `C-k` apply to screen
; lines instead of logical lines.
(setq-default word-wrap t)

; Cycle through previously edited points in the current buffer.
(require 'goto-chg)
(global-set-key (kbd "s-.") 'goto-last-change)
(global-set-key (kbd "s-,") 'goto-last-change-reverse)

; Jump to a character visible in the current buffer with few
; keystrokes.
(require 'ace-jump-mode)
(global-set-key (kbd "s-j") 'ace-jump-char-mode)

; Make `C-up` add a cursor above and `C-down` add a cursor below.
(require 'multiple-cursors)
(global-set-key (kbd "<C-up>") 'mc/mark-previous-like-this)
(global-set-key (kbd "<C-down>") 'mc/mark-next-like-this)

; `expand-region` increases the region by semantic units,
; `change-inner` kills text within paired characters excluding the
; paired characters, and `change-outer` kills text within paired
; characters including the paired characters.
(require 'expand-region)
(require 'change-inner)
(require 'smart-forward)
(global-set-key (kbd "C-1") 'er/expand-region)
(global-set-key (kbd "H-i") 'change-inner)
(global-set-key (kbd "H-o") 'change-outer)

(setq ns-command-modifier 'super)
(setq ns-right-control-modifier 'hyper)

; Use a custom implementation for full screen in OS X so that there is
; no animation when switching between Emacs and another application.
(setq-default ns-use-native-fullscreen nil)

; Disable the audible bell. If in OS X the alert volume is set to
; zero, the audible bell is not played, but it causes the sound output
; to be activated in a way that a quiet hiss is produced for some
; period of time.
(setq ring-bell-function 'ignore)

; Use a Japanese instead of a Chinese font to display Japanese and
; Chinese characters in OS X.
(set-fontset-font "fontset-default" 'japanese-jisx0208 '("Hiragino Kaku Gothic ProN" . "iso10646-1"))

; Copy text to the clipboard in a text terminal in OS X.
(defun pbcopy ()
  (interactive)
  (let ((deactivate-mark t))
    (call-process-region (point) (mark) "pbcopy")))

(defun pbpaste ()
  (interactive)
  (call-process-region (point) (if mark-active (mark) (point)) "pbpaste" t t))

(defun pbcut ()
  (interactive)
  (pbcopy)
  (kill-region (region-beginning) (region-end)))
```
