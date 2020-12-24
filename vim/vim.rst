=====
 Vim
=====
-------------------------
 All-Purpose Text Editor
-------------------------

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright:
   `Creative Commons Attribution-ShareAlike 4.0 International Public License`__

.. contents::

.. sectnum::
   :suffix: .

__ https://creativecommons.org/licenses/by-sa/4.0/

.. _Davie Badger: https://github.com/daviebadger



Modes
=====

* ``a`` - switch to Insert mode after the cursor
* ``A`` - switch to Insert mode at the end of a line
* ``CTRL + v`` - switch to Visual mode blockwise
* ``ESC`` - switch to Normal mode
* ``I`` - switch to Insert mode at the start of a line
* ``i`` - switch to Insert mode in place of the cursor
* ``O`` - switch to Insert mode in a new line above the cursor
* ``o`` - switch to Insert mode in a new line below the cursor
* ``:`` - switch to Command-line mode
* ``{visual-block} + A`` - switch to Insert mode at the end of a highlighted block
* ``{visual-block} + I`` - switch to Insert mode at the start of a highlighted block
* ``v`` - switch to Visual mode characterwise
* ``V`` - switch to Visual mode linewise



Motions
=======

Left-Right Motions
------------------

* ``$`` - go to the last character in a line
* ``0`` - go to the first character in a line
* ``F + {char}`` - go to the given character left in a line
* ``f + {char}`` - go to the given character right in a line
* ``g$`` - go to the last character in a screen line (wrap is on)
* ``g0`` - go to the first character in a screen line (wrap is on)
* ``g^`` - go to the first non-blank character in a screen line (wrap is on)
* ``g_`` - go to the last non-blank character in a line
* ``gM`` - go to the center of a line
* ``gm`` - go to the center of a screen line
* ``^`` - go to the first non-blank character in a line
* ``h`` - go 1 character left
* ``l`` - go 1 character right
* ``{number} + |`` - go to the given column
* ``,`` - repeat ``f``, ``F``, ``t``, ``T`` backwards
* ``;`` - repeat ``f``, ``F``, ``t``, ``T`` forwards
* ``T + {char}`` - go before the given character left in a line
* ``t + {char}`` - go before the given character right in a line

Up-Down Motions
---------------

* ``gg`` - go to the first line
* ``G`` - go to the last line
* ``gj`` - go 1 screen line down (wrap is on)
* ``gk`` - go 1 screen line up (wrap is on)
* ``+`` - go 1 line down to a non-blank character
* ``-`` - go 1 line up to a non-blank character
* ``j`` - go 1 line down
* ``k`` - go 1 line up
* ``{number} + G`` - go to the given line
* ``{number} + %`` - go to the given percentage line

Word Motions
------------

* ``b`` - go to the start of a current or previous "word"
* ``B`` - go to the start of a current or previous word
* ``e`` - go to the end of a current or the next "word"
* ``E`` - go to the end of a current or the next word
* ``ge`` - go to the end of a previous "word"
* ``gE`` - go to the end of a previous word
* ``w`` - go to the start of the next "word"
* ``W`` - go to the start of the next word

Text Object Motions
-------------------

* ``}`` - go to the next paragraph including a newline
* ``)`` - go to the next sentence
* ``{`` - go to the previous paragraph including a newline
* ``(`` - go to the previous sentence

Search Motions
--------------

* ``? + ENTER`` - repeat the last search backwards
* ``/ + ENTER`` - repeat the last search forwards
* ``gD`` - go to the global declaration of an identifier under the cursor
* ``gd`` - go to the local declaration of an identifier under the cursor
* ``g#`` - partially search the identifier under the cursor backwards
* ``g*`` - partially search the identifier under the cursor forwards
* ``n`` - repeat the last search
* ``N`` - repeat the last search reversely
* ``? + {pattern}`` - search the given battern backwards
* ``/ + {pattern}`` - search the given pattern forwards
* ``#`` - search the identifier under the cursor backwards
* ``*`` - search the identifier under the cursor forwards

Mark Motions
------------

* ``:delm[arks]!`` - delete all local marks
* ``:delm[arks] {mark} [mark]`` - delete the given mark or marks
* :literal:`\` + {mark}` - go to the given mark
* ``' + {mark}'`` - go to the given mark to the first non-blank character
* ``:marks {mark} [mark]`` - show the given mark or marks
* ``:marks`` - show a list of marks
* ``m + {mark}`` - set the given mark at the current position
* ``:[range]ma[rk] {mark}`` - set the given mark at a specific line

Other Motions
-------------

* ``%`` - go to the matching brace / bracket / parenthesis
* ``H`` - go to the top of a window
* ``L`` - go to the bottom of a window
* ``M`` - go to the center of a window

Jumps
-----

* ``:changes`` - show a list of changes
* ``:cle[arjumps]`` - clear the current window jump list
* ``CTRL + i`` - go to the newer cursor position in a jump list
* ``CTRL + o`` - go to the older cursor position in a jump list
* ``g,`` - go to the newer change position in a change list
* ``g;`` - go to the older change position in a change list
* ``:ju[mps]`` - show a list of jumps

Scrolling
---------

* ``CTRL + b`` - scroll 1 window backwards
* ``CTRL + d`` - scroll 1/2 window forwards
* ``CTRL + e`` - scroll 1 screen line forwards
* ``CTRL + f`` - scroll 1 window forwards
* ``CTRL + u`` - scroll 1/2 window backwards
* ``CTRL + y`` - scroll 1 screen line backwards
* ``:sync[bind]`` - synchronous scrolling for the same buffer (scrollbind is on)
* ``zb`` - scroll the current line to the bottom of a window
* ``ze`` - scroll the current character to the end of a screen line (wrap is off)
* ``zH`` - scroll 1/2 screen width left (wrap is off)
* ``zh`` - scroll screen width 1 character to left (wrap is off)
* ``zL`` - scroll 1/2 screen width right (wrap is off)
* ``zl`` - scroll screen width 1 character to right (wrap is off)
* ``z+`` - scroll to the next screen
* ``z^`` - scroll to the previous screen
* ``zs`` - scroll the current character to the start of a screen line (wrap is off)
* ``zt`` - scroll the current line to the top of a window
* ``zz`` - scroll the current line to the center of a window



Operations
==========

Copying/Pasting Text
--------------------

* ``gp`` - put a text after the cursor and move the cursor after it
* ``gP`` - put a text before the cursor and move the cursor after it
* ``:[line]pu[t][!] [register]`` - put a text after a line (with ``!`` before a line)
* ``p`` - put a text after the cursor
* ``]p`` - put a text after the cursor and adjust the indent
* ``P`` - put a text before the cursor
* ``[P`` - put a text before the cursor and adjust the indent
* ``:[range]y[ank] [register]`` - yank text in lines
* ``:reg[isters] {register}`` - show content in the given register
* ``:reg[isters]`` - show a list of content in registers
* ``" + {register}`` - use the given register for the next yank / put / delete operation
* ``{visual} + y`` - yank a highlighted text
* ``y + {motion}`` - yank to the given motion
* ``Y`` - yank the current line
* ``yy`` - yank the current line

Deleting Text
-------------

* ``dd`` - delete the current line
* ``D`` - delete to the end of a line
* ``d + {motion}`` - delete to the given motion
* ``gJ`` - join the current and the next line without space
* ``J`` - join the current and the next line with space
* ``:[range]d[elete] [register]`` - delete specific lines
* ``:[range]j[oin][!]`` - join specific lines (without spaces with ``!``)
* ``{visual-block} + D`` - delete to the end of a highlighted block
* ``{visual} + d`` - delete the highlighted text
* ``{visual} + gJ`` - join highlighted lines without space
* ``{visual} + J`` - join highlighted lines with space
* ``X`` - delete a character before the cursor
* ``x`` - delete a character under the cursor

Changing Text
-------------

* ``==`` - auto indent the current line
* ``cc`` - change the current line
* ``C`` - change to the end of a line
* ``c + {motion}`` - change to the given motion
* ``!! + {command}`` - apply an external command to the current line
* ``CTRL + a`` - increase a number under the cursor
* ``CTRL + x`` - decrease a number under the cursor
* ``g~ + {motion}`` - switch case to the given motion
* ``gq + {motion}`` - justify text in lines to the given motion
* ``gqq`` - justify text in the current line
* ``g&`` - repeat the last substitution in the whole file with the same flags for the last search
* ``g~~`` - switch case in the current line
* ``gu + {motion}`` - lower a text to the given motion
* ``gU + {motion}`` - upper a text to the given motion
* ``guu`` - lower the current line
* ``gUU`` - upper the current line
* ``gw + {motion}`` - justify text in lines to the given motion and keep the cursor position before change
* ``gww`` - justify text in the current line and keep the cursor position before change
* ``>>`` - indent the current line
* ``= + {motion}`` - auto indent lines to the given motion
* ``! + {motion} + {command}`` - apply an external command to lines to the given motion
* ``> + {motion}`` - indent lines to the given motion
* ``< + {motion}`` - unindent lines to the given motion
* ``:[range]ce[nter]`` - center align in lines
* ``:[range]c[hange][!]`` - change specific lines (respect indent with ``!``)
* ``:{range}!{filter}`` - apply an external command to lines
* ``:[range]&{flags}`` - repeat the last substitution in lines with the given flags
* ``:[range]~{flags}`` - repeat the last substitution in lines with the given flags for the last search
* ``:[range]&&[flags]`` - repeat the last substitution in lines with the same or given flags
* ``:[range]~&[flags]`` - repeat the last substitution in lines with the same or given flags for the last search
* ``:[range]>`` - indent lines as many ``>`` repeats
* ``:[range]le[ft]`` - left align in lines
* ``:[range]ri[ght]`` - right align in lines
* ``:[range]s[ubstitute]/{pattern}/{string}/[flags]`` - substitute the given pattern with the given string in lines
* ``:[range]<`` - unindent lines as many ``<`` repeats
* ``r + {char}`` - replace a character under the cursor with the given character
* ``&`` - repeat the last substitution in the current line without flags
* ``:~`` - repeat the last substitution in the current line without flags for the last search
* ``s`` - change character under the cursor
* ``S`` - change the current line
* ``~`` - switch case under the cursor
* ``<<`` - unindent the current line
* ``{visual} + =`` - auto indent a highlighted text
* ``{visual-block} + C`` - change to the end of a highlighted block
* ``{visual} + c`` - change a highlighted text
* ``{visual} + :ce[nter]`` - center align for the highlighted text
* ``{visual} + :{command}`` - apply a Command-line command for the highlighted text
* ``{visual} + !{command}`` - apply an external command for the highlighted lines
* ``{visual} + CTRL + a`` - increase numbers in highlighted text
* ``{visual} + CTRL + x`` - decrease numbers in highlighted text
* ``{visual} + g + CTRL + a`` - sequentially increase numbers in highlighted lines
* ``{visual} + g + CTRL + x`` - sequentially decrease numbers in highlighted lines
* ``{visual} + gq`` - justify a highlighted text
* ``{visual} + gw`` - justify a highlighted text and keep the cursor position before change
* ``{visual} + >`` - indent a highlighted text
* ``{visual} + :le[ft]`` - left align for the highlighted text
* ``{visual} + r + {char}`` - replace a highlighted text with the given character
* ``{visual} + :ri[ght]`` - right align for the highlighted text
* ``{visual} + ~`` - switch case of a highlighted text
* ``{visual} + u`` - lower a highlighted text
* ``{visual} + <`` - unindent a highlighted text
* ``{visual} + <`` - unindent the current line
* ``{visual} + U`` - upper a highlighted text

Undo/Redo Changes
-----------------

* ``CTRL + r`` - redo the last change
* ``:ea[rlier] {number}d`` - go to a text state before the given days
* ``:ea[rlier] {number}f`` - go to the oldest text state before the given file writes
* ``:ea[rlier] {number}h`` - go to a test state before the given hours
* ``:ea[rlier] {number}m`` - go to a test state before the given minutes
* ``:ea[rlier] {number}s`` - go to a test state before the given seconds
* ``g+`` - go to a newer text state
* ``g-`` - go to an older text state
* ``:lat[er] {number}d`` - go to a text state after the given days
* ``:lat[er] {number}f`` - go to the newest text state after the given file writes
* ``:lat[er] {number}h`` - go to a text state after the given hours
* ``:lat[er] {number}m`` - go to a text state after the given minutes
* ``:lat[er] {number}s`` - go to a text state after the given seconds
* ``:undol[ist]`` - show a list of undo branches
* ``:un[do] {number}`` - go to the given undo branch
* ``U`` - undo a recently changed line
* ``u`` - undo the last change

Repeating Commands
------------------

* ``q + {register}`` - record typed characters into the given register
* ``q`` - stop recording
* ``@ + {register}`` - execute the content of the given register
* ``.`` - repeat the last change
* ``@:`` - repeat the last command in Command-line
* ``@@`` - repeat the previous execution



Mode Specialities
=================

Command-Line Commands
---------------------

* ``:as[cii]`` - show the ASCII, hex and octal number of the current character
* ``|`` - a separator for executing more commands at once
* ``:!{command}`` - execute the given command in a shell
* ``:[range]norm[al][!] {commands}`` - execute Normal mode commands (mappins are ignored with ``!``)
* ``:redi[r] END`` - end redirecting
* ``:redi[r] >> {file}`` - start redirecting commands output by appending to the given file
* ``:redi[r][!] > {file}`` -  start redirecting commands output to the given file (override the file with ``!``)
* ``:redi[r] @{register}>>`` - start redirecting commands output by appending to the given register
* ``:redi[r] @{register}>`` - start redirecting commands output to the given register
* ``:!!`` - repeat the last ``:!{command}``
* ``:=`` - show the last line number
* ``:sil[ent][!] {command}`` - do not show the given command output (ignore errors with ``!``)
* ``:sw[apname]`` - show a path to the swap file
* ``:ve[rsion]`` - show a Vim version

Insert Mode Commands
--------------------

* ``0 + CTRL + d`` - delete indents in the current line
* ``CTRL + a`` - insert a previously inserted text
* ``CTRL + d`` - unindent the current line
* ``CTRL + @`` - insert a previously inserted text and stop Insert mode
* ``CTRL + r + {register}`` - insert a text from the given register
* ``CTRL + t`` - indent the current line
* ``CTRL + u`` - delete newly added characters in the current line
* ``CTRL + w`` - delete the current or a previous "word"
* ``:[range]r[ead] !{command}`` - insert an external command output below the cursor
* ``:[range]r[ead] [file]`` - insert a file content below the cursor (default is the current file)

Insert Mode Completition
------------------------

* ``CTRL + e`` - exit a popup and remove the completed text
* ``CTRL + n`` - complete the word or choose the next match from a popup
* ``CTRL + p`` - complete the word or choose the previous match from a popup
* ``CTRL + x + CTRL + f`` - complete the path from the current working directory
* ``CTRL + x + CTRL + l`` - complete the line
* ``CTRL + x + CTRL + n`` - complete the word from words in the current file

Insert Mode Motions
-------------------

* ``END`` - go to the last character in a line
* ``HOME`` - go to the first character in a line
* ``SHIFT + DOWN`` - scroll 1 window backwards
* ``SHIFT + LEFT`` - go to the start of the next "word"
* ``SHIFT + RIGHT`` - go to the start of a current or previous "word"
* ``SHIFT + UP`` - scroll 1 window forwards

Visual Mode Commands
--------------------

* ``gN`` - highlight a recently searched pattern backwards or up to the previous one
* ``gn`` - highlight a recently searched pattern forwards or up to the next one
* ``gv`` - highlight a recently highlighted text
* ``o`` - go to the opposite edge of a highlighted text
* ``O`` - go to the opposite line edge of a blockwise highlighted text

Visual Mode Text Objects
------------------------

* ``a + {bracket}`` - select a text inside () / {} / [] / <> brackets inclusively
* ``a + p`` - select a paragraph including a newline
* ``a + {quote}`` - select a text inside "" '' `` quotes inclusively
* ``a + s`` - select a sentence including space
* ``a + t`` - select a text inside a HTML / XML tag inclusively
* ``a + w`` - select a "word" including space
* ``a + W`` - select a word including space
* ``i + {bracket}`` - select a text inside () / {} / [] / <> brackets
* ``i + p`` - select a paragraph
* ``i + {quote}`` - select a text inside "" '' `` quotes
* ``i + s`` - select a sentence
* ``i + t`` - select a text inside a HTML / XML tag
* ``i + w`` - select a "word"
* ``i + W`` - select a word



Miscellaneous
=============

Buffers
-------

* ``:bd[elete][!]`` - delete the current buffer
* ``:bd[elete][!] {number} [number]`` - delete the given buffer or buffers (discard changes with ``!``)
* ``:bf[irst][!]`` - go to the first buffer (keep changes with ``!``)
* ``:bl[ast][!]`` - go to the last buffer (keep changes with ``!``)
* ``:bn[ext][!]`` - go to the next buffer (keep changes with ``!``)
* ``:bn[ext][!] {number}`` - go to the given number forwards (keep changes with ``!``)
* ``:bp[revious][!]`` - go to the previous buffer (keep changes with ``!``)
* ``:bp[revious][!] {number}`` - go to the given number backwards (keep changes with ``!``)
* ``:b[uffer][!] {number}`` - go to the given buffer (keep changes with ``!``)
* ``:ls`` - show a list of buffers
* ``:[range]bufdo[!] {command}`` - apply a Command-line command to all or specific buffers in the buffer list (leave changed buffers with ``!``)
* ``:sbf[irst][!]`` - split the window horizontally and go to the first buffer (keep changes with ``!``)
* ``:sbl[ast][!]`` - split the window horizontally and go to the last buffer (keep changes with ``!``)
* ``:sbn[ext][!] {number}`` - split the window horizontally and go to the given number forwards (keep changes with ``!``)
* ``:sbn[ext][!]`` - split the window horizontally and go to the next buffer (keep changes with ``!``)
* ``:sbp[revious][!] {number}`` - split the window horizontally and go to the given number backwards (keep changes with ``!``)
* ``:sbp[revious][!]`` - split the window horizontally and go to the previous buffer (keep changes with ``!``)
* ``:sb[uffer] {number}`` - split the window horizontally and go to the given buffer (keep changes with ``!``)

CLI Arguments/Options
---------------------

* ``-C`` - open in a Vi-compatible mode (plugins or settings may break it)
* ``-d`` - open in a diff mode
* ``[files]`` - open Vim with an empty buffer or loaded buffers (1 active buffer, other hidden)
* ``--help`` - show a CLI help
* ``-h`` - show a CLI help
* ``-m`` - open in a stricter read-only mode (changes allowed, writing disallowed)
* ``-M`` - open in a strictest read-only mode (changes disallowed, writing disallowed)
* ``-n`` - do not use a swap file
* ``-N`` - open in a not Vi-compatible mode (plugins or settings may break it)
* ``--noplugin`` - load the vimrc and defaults without plugins
* ``+[number]`` - go to the given line number in the first active buffer (default is the last)
* ``-o`` - open buffers in horizontal windows
* ``-O`` - open buffers in vertical windows
* ``-`` - open Vim with text from stdin
* ``+/{pattern}`` - go to the first pattern occurrence in the first active buffer (quotes for words)
* ``-p`` - open buffers in tab pages
* ``-r {file}`` - recover the given file from the ``file name`` row
* ``-R`` - open in a read-only mode (changes allowed, writing allowed with ``!``)
* ``-r`` - show a list of files to recover
* ``--startuptime {file}`` - log startup time to the given file
* ``-u DEFAULTS`` - load defaults without the vimrc and plugins
* ``-u {file.vim}`` - load the given file as the vimrc without plugins and defaults
* ``-u NONE`` - load without the vimrc, plugins and defaults
* ``--version`` - show a Vim version

Folds
-----

* ``:[range]folddoc[losed] {command}`` - apply a Command-line command to folded lines
* ``:[range]foldd[open] {command}`` - apply a Command-line command to not folded lines
* ``:{range}fo[ld]`` - fold lines
* ``{visual} + zf`` - fold the given highlighted lines
* ``zC`` - close all folds under the cursor recursively upwards
* ``zc`` - close one fold under the cursor
* ``zf + {motion}`` - fold lines to the given motion
* ``] + z`` - go to the end of an opened fold
* ``[ + z`` - go to the start of an opened fold
* ``zj`` - go to the start of a next fold area
* ``zk`` - go to the end of a previous fold area
* ``zM`` - close all folds
* ``zm`` - close all folds under the same level
* ``zO`` - open all folds under the cursor recursively downwards
* ``zo`` - open one fold under the cursor
* ``zr`` - open all folder under the same level
* ``zR`` - open all folds

Help
----

* ``CTRL + i`` - jump to the subject ahead in history
* ``CTRL + ]`` - jump to a subject under the cursor
* ``CTRL + o`` - jump to the subject back in history
* ``:helpg[ep] {pattern}`` - open a quickfix window with grepped results for the given pattern
* ``:h[elp]`` - open a window with Vim help
* ``:h[help] {subject}`` - open a help for the given subject

Tabs
----

* ``CTRL + w + gf`` - open the file under the cursor in a new tab
* ``CTRL + w + gF`` - open the file under the cursor in a new tab and jump to the line number following the file
* ``gt`` - go to the next tab
* ``gT`` - go to the previous tab
* ``{number} + gt`` - go to the given tab (starting since 1)
* ``:[position]tab {command}`` - create a new tab with the given command output (must be long)
* ``:[position]tabnew [file]`` - create an empty tab or open the given file in a new tab
* ``:[range]tabd[o] {command}`` - apply a Command-line command to all or specific tabs and their first window
* ``:tabc[lose][!] $`` - close the last tab (keep changes with ``!``)
* ``:tabc[lose][!]`` - close the tab (keep changes with ``!``)
* ``:tabc[lose][!] {number}`` - close the given tab (starting since 1, keep changes with ``!``)
* ``:tabfir[st]`` - go to the first tab
* ``:tabl[ast]`` - go to the last tab
* ``:tabm[ove] $`` - move the tab to the end of a tab line
* ``:tabm[ove] 0`` - move the tab to the start of a tab line
* ``:tabm[ove] -{number}`` - move the tab the given tabs backwards
* ``:tabm[ove] +{number}`` - move the tab the given tabs forwards
* ``:tabn[ext] -{number}`` - go the given tabs backwards
* ``:tabn[ext] +{number}`` - go the given tabs forwards
* ``:tabon[only][!] $`` - close all tabs except for the last tab (keep changes with ``!``)
* ``:tabon[only][!]`` - close all tabs except for the current tab (keep changes with ``!``)
* ``:tabon[only][!] {number}`` - close all tabs except for the given tab (starting since 1, keep changes with ``!``)
* ``:tabs`` - show a list of tabs and their windows

Windows
-------

* ``:abo[veleft] {command}`` - create a new window above horizontally with the given command output (must be long)
* ``:bel[owright] {command}`` - create a new window below horizontally with the given command output (must be long)
* ``:bo[tright] {command}`` - create a new window at the bottom horizontally with the given command output (must be long)
* ``:clo[se][!]`` - close the window (keep changes with ``!``)
* ``CTRL + w + b`` - go to the bottom-right window
* ``CTRL + w + c`` - close the window (stay in Vim)
* ``CTRL + w + -`` - decrease the window height
* ``CTRL + w + <`` - decrease the window width
* ``CTRL + w + f`` - open the file under the cursor in a new window horizontally
* ``CTRL + w + F`` - open the file under the cursor in a new window horizontally and jump to the line number following the file
* ``CTRL + w + H`` - move the window to the most left
* ``CTRL + w + h`` - on to the window left
* ``CTRL + w + +`` - increase the window height
* ``CTRL + w + >`` - increase the window width
* ``CTRL + w + j`` - go to the window down
* ``CTRL + w + J`` - move the window to the most down
* ``CTRL + w + k`` - go to the window up
* ``CTRL + w + K`` - move the window to the most up
* ``CTRL + w + l`` - go to the window right
* ``CTRL + w + L`` - move the window to the most right
* ``CTRL + w + =`` - make all windows equal
* ``CTRL + w + _`` - make the window highest posible
* ``CTRL + w + |`` - make the window widest posible
* ``CTRL + w + o`` - close all windows except for the current window
* ``CTRL + w + p`` - go to the previous window
* ``CTRL + w + q`` - close the window (may quit Vim)
* ``CTRL + w + r`` - move the window downwards / rightwards
* ``CTRL + w + R`` - move the window upwards / leftwards
* ``CTRL + w + s`` - split the current window horizontally
* ``CTRL + w + t`` - go to the top-left window
* ``CTRL + w + T`` - move the window to a new tab
* ``CTRL + w + v`` - split the current window vertically
* ``CTRL + w + w`` - go to the next below / right window
* ``CTRL + w + W`` - go to the previous above / left window
* ``CTRL + w + x`` - swap the current window and the next window
* ``{height} + CTRL + _`` - set the given height to the window
* ``:new`` - create an empty window horizontally
* ``:on[ly][!]`` - close all windows except for the current window (keep changes with ``!``)
* ``:q[uit][!]`` - close the window (discard changes with ``!``)
* ``:[range]windo {command}`` - apply a Command-line command to all or specific windows in the current tab
* ``:sp[lit] [file]`` - split the current window or open the given file horizontally
* ``:sp[lit] #{number}`` - open the given buffer horizontally
* ``:sp[lit] #`` - open the last buffer horizontally
* ``:to[pleft] {command}`` - create a new window at the top horizontally with the given command output (must be long)
* ``:vert[ical] {command}`` - create a new window vertically with the given command output (must be long)
* ``:vne[w]`` - create an empty window vertically
* ``:vs[plit] [file]`` - split the current window or open the given file vertically
* ``:vs[plit] #{number}`` - open the given buffer vertically
* ``:vs[plit] #`` - open the last buffer vertically
* ``{width} + CTRL + |`` - set the given width to the window



Technicalities
==============

Help Subjects
-------------

TODO

Ranges
------

* ``$`` - the last line
* ``\/`` - a line containing the previously searched pattern backwards
* ``\?`` - a line containing the previously searched pattern backwards
* ``\&`` - a line containing the previously substituted pattern forwards
* ``,`` - a separator for a range from to
* ``%`` - a shortcut for ``1,$``
* ``'{mark}`` - a line of a mark
* ``{number}`` - a specific line (from 1 for most use cases, from 0 for searches)
* ``-[number]`` - an offset backwards (default 1)
* ``+[number]`` - an offset forwards (default 1)
* ``?{pattern}?`` - a line containing the given pattern backwards
* ``/{pattern}/`` - a line containing the given pattern forwards
* ``.`` - the current line (default when no range set explicitly)

Mark Types
----------

* ``{0-9}`` - automatically set marks from ``~/.viminfo`` (single number)
* ``{A-Z}`` - user-defined global marks across buffers (single letter, overridable)
* ``{a-z}`` - user-defined local marks per buffer (single letter, overridable)
* ``>`` - the end of a previously highlighted text (overridable)
* ``]`` - the end of a previously inserted or pasted text before writing (overridable)
* ``.`` - the position when last changed
* ``"`` - the position when last exiting the file
* ``^`` - the position when last writing the file
* ``'`` - the previous position when using with ``'``
* ````` - the previous position when using with `````
* ``<`` - the start of a previously highlighted text (overridable)
* ``[`` - the start of a previously inserted or pasted text before writing (overridable)

Register Types
--------------

* ``"0`` - the last yank
* ``"{1-9}`` - the last delete / change operations (single number, from recent to oldest)
* ``"_`` - a black hole like ``/dev/null``
* ``"{A-Z}`` - appending text to ``"{a-z}`` registers
* ``"{a-z}`` - user-defined registers (single letter)
* ``""`` - text from the last ``c`` / ``d`` / ``s`` / ``x`` / ``y`` operation
* ``"%`` - the current filename
* ``":`` - the last command in Command-line
* ``"-`` - the last deleted text inline
* ``".`` - the last inserted text
* ``"/`` - the last searched pattern
* ``"+`` - the system clipboard
* ``"*`` - the system selection in GUI

Search Patterns
---------------

TODO

Substitution Flags
------------------

* ``c`` - confirm each substitution

  * ``a`` - substitute all matches
  * ``CTRL + e`` - scroll 1 screen line forwards
  * ``CTRL + y`` - scroll 1 screen line backwards
  * ``l`` - substitute this match and quit
  * ``n`` - skip this match
  * ``q`` - quit
  * ``y`` - substitute this match

* ``e`` - do not show an error message when no match found
* ``g`` - substitute all occurrences in a line
* ``I`` - do not ignore case sensitivity (ignore Vim settings)
* ``i`` - ignore case sensitivity (ignore Vim settings)
* ``&`` - keep flags from the last substitution (must be the first flag in order)
* ``n`` - show a report of potencial matches
