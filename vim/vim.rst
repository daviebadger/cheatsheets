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
* ``{visual-block} + A`` - switch to Insert mode at the end of a highlighted block
* ``{visual-block} + I`` - switch to Insert mode at the start of a highlighted block
* ``v`` - switch to Visual mode characterwise
* ``V`` - switch to Visual mode linewise
* ``:`` - switch to Command-line mode



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

Text Object Motions
-------------------

* ``b`` - go to the start of a current or previous "word"
* ``B`` - go to the start of a current or previous word
* ``e`` - go to the end of a current or the next "word"
* ``E`` - go to the end of a current or the next word
* ``ge`` - go to the end of a previous "word"
* ``gE`` - go to the end of a previous word
* ``w`` - go to the start of the next "word"
* ``W`` - go to the start of the next word

Search Motions
--------------

* ``#`` - search the identifier under the cursor backwards
* ``*`` - search the identifier under the cursor forwards
* ``/ + ENTER`` - repeat the last search forwards
* ``? + ENTER`` - repeat the last search backwards
* ``g#`` - partially search the identifier under the cursor backwards
* ``g*`` - partially search the identifier under the cursor forwards
* ``gd`` - go to the local declaration of an identifier under the cursor
* ``gD`` - go to the global declaration of an identifier under the cursor
* ``n`` - repeat the last search
* ``N`` - repeat the last search reversely
* ``/ + {pattern}`` - search the given pattern forwards
* ``? + {pattern}`` - search the given battern backwards

Mark Motions
------------

* ```>`` - go to the end of a previously highlighted text
* ```]`` - go to the end of a previously inserted or pasted text else ``G``
* ```.`` - go to the last change
* ```"`` - go to the position when last editing the file
* `````` - go to the previous position
* ```<`` - go to the start of a previously highlighted text
* ```[`` - go to the start of a previously inserted or pasted text else ``gg``
* ``:ju[mps]`` - show a jump list
* :literal:`\` + {a-z}` - go to the given mark
* ``:marks {a-z}`` - show the given mark
* ``:marks`` - show a list of marks
* ``m + {a-z}`` - create the given mark in the current position

Other Motions
-------------

* ``%`` - go to the matching brace / bracket / parenthesis
* ``H`` - go to the top of a window
* ``L`` - go to the bottom of a window
* ``M`` - go to the center of a window

Scrolling
---------

* ``CTRL + b`` - scroll 1 window backwards
* ``CTRL + d`` - scroll 1/2 window forwards
* ``CTRL + f`` - scroll 1 window forwards
* ``CTRL + u`` - scroll 1/2 window backwards
* ``zb`` - scroll the current line to the bottom of a window
* ``zH`` - scroll 1/2 screen width left (wrap is off)
* ``zh`` - scroll screen width 1 character to left (wrap is off)
* ``zL`` - scroll 1/2 screen width right (wrap is off)
* ``zl`` - scroll screen width 1 character to right (wrap is off)
* ``zt`` - scroll the current line to the top of a window
* ``zz`` - scroll the current line to the center of a window



Operations
==========

Copying/Pasting Text
--------------------

* ``p`` - put a text after the cursor
* ``P`` - put a text before the cursor
* ``{visual} + y`` - yank a highlighted text
* ``y + {motion}`` - yank to the given motion
* ``Y`` - yank the current line
* ``yy`` - yank the current line

Deleting Text
-------------

* ``dd`` - delete the current line
* ``D`` - delete to the end of a line
* ``d + {motion}`` - delete to the given motion
* ``gJ`` - join lines without space
* ``J`` - join lines with space
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
* ``:ce[nter]`` - center align for the current line
* ``c + {motion}`` - change to the given motion
* ``CTRL + a`` - increase a number under the cursor
* ``CTRL + x`` - decrease a number under the cursor
* ``g~ + {motion}`` - switch case to the given motion
* ``g~~`` - switch case in the current line
* ``gu + {motion}`` - lower a text to the given motion
* ``gU + {motion}`` - upper a text to the given motion
* ``guu`` - lower the current line
* ``gUU`` - upper the current line
* ``>>`` - indent the current line
* ``:le[ft]`` - left align for the current line
* ``= + {motion}`` - auto indent to the given motion
* ``> + {motion}`` - indent to the given motion
* ``< + {motion}`` - unindent to the given motion
* ``r + {char}`` - replace a character under the cursor with the given character
* ``:ri[ght]`` - right align for the current line
* ``s`` - change character under the cursor
* ``S`` - change the current line
* ``~`` - switch case under the cursor
* ``<<`` - unindent the current line
* ``{visual} + =`` - auto indent a highlighted text
* ``{visual-block} + C`` - change to the end of a highlighted block
* ``{visual} + c`` - change a highlighted text
* ``{visual} + :ce[nter]`` - center align for the highlighted text
* ``{visual} + >`` - indent the current line
* ``{visual} + :le[ft]`` - left align for the highlighted text
* ``{visual} + :ri[ght]`` - right align for the highlighted text
* ``{visual} + ~`` - switch case of a highlighted text
* ``{visual} + u`` - lower a highlighted text
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

* ``@ + {a-z}`` - execute the content of the given register
* ``q + {A-Z}`` - record typed characters and append to the given register
* ``q + {a-z}`` - record typed characters into the given register
* ``q`` - stop recording
* ``.`` - repeat the last change
* ``@@`` - repeat the previous execution



Mode Specialities
=================

Insert Mode Commands
--------------------

* ``0 + CTRL + d`` - delete indents in the current line
* ``CTRL + a`` - insert a previously inserted text
* ``CTRL + d`` - unindent the current line
* ``CTRL + n`` - complete the word or choose the next match
* ``CTRL + p`` - complete the word or choose the previous match
* ``CTRL + r + {register}`` - insert a text from the given register
* ``CTRL + t`` - indent the current line
* ``CTRL + u`` - delete newly added characters in the current line
* ``CTRL + w`` - delete the current or a previous "word"

Visual Mode Commands
--------------------

* ``gv`` - highlight a recently highlighted text
* ``o`` - go to the opposite edge of a highlighted text

Visual Mode Text Objects
------------------------

* ``a + {bracket}`` - select a text inside a () / {} / [] / <> brackets inclusively
* ``a + p`` - select a paragraph including a newline
* ``a + {quote}`` - select a text inside quotes inclusively
* ``a + s`` - select a sentence including space
* ``a + t`` - select a text inside a HTML / XML tag inclusively
* ``a + w`` - select a "word" including space
* ``a + W`` - select a word including space
* ``i + {bracket}`` - select a text inside a () / {} / [] / <> brackets
* ``i + p`` - select a paragraph
* ``i + {quote}`` - select a text inside quotes
* ``i + s`` - select a sentence
* ``i + t`` - select a text inside a HTML / XML tag
* ``i + w`` - select a "word"
* ``i + W`` - select a word



Miscellaneous
=============

Folding
-------

* ``{visual} + zf`` - fold the given highlighted text
* ``zC`` - close all folds under the cursor upwards
* ``zc`` - close one fold under the cursor
* ``zf + {motion}`` - fold to the given motion
* ``] + z`` - go to the end of an opened fold
* ``[ + z`` - go to the start of an opened fold
* ``zj`` - go to the start of a next fold area
* ``zk`` - go to the end of a previous fold area
* ``zM`` - close all folds
* ``zm`` - close all folds under the same level
* ``zO`` - open all folds under the cursor downwards
* ``zo`` - open one fold under the cursor
* ``zr`` - open all folder uner the same level
* ``zR`` - open all folds

Help
----

* ``:h[elp]`` - open a window with Vim help
* ``:h[help] {subject}`` - open a help for the given subject
* ``:helpg[ep] {pattern}`` - open a quickfix window with grepped results for the given pattern
* ``CTRL + ]`` - jump to a subject under the cursor
* ``CTRL + o`` - jump to the subject back in history
* ``CTRL + i`` - jump to the subject ahead in history

Tabs
----

* ``CTRL + w + gf`` - open the file under the cursor in a new tab
* ``CTRL + w + gF`` - open the file under the cursor in a new tab and jump to the line number following the file
* ``gt`` - go to the next tab
* ``gT`` - go to the previous tab
* ``{number} + gt`` - go to the given tab (starting since 1)
* ``:tabc[lose][!] $`` - close the last tab (keep changes with ``!``)
* ``:tabc[lose][!]`` - close the tab (keep changes with ``!``)
* ``:tabc[lose][!] {number}`` - close the given tab (starting since 1, keep changes with ``!``)
* ``:tab {command}`` - create a new tab with the given command output (must be long)
* ``:tabfir[st]`` - go to the first tab
* ``:tabl[ast]`` - go to the last tab
* ``:tabm[ove] $`` - move the tab to the end of a tab line
* ``:tabm[ove] 0`` - move the tab to the start of a tab line
* ``:tabm[ove] -{number}`` - move the tab the given tabs backwards
* ``:tabm[ove] +{number}`` - move the tab the given tabs forwards
* ``:tabnew [file]`` - create an empty tab or open the given file in a new tab
* ``:tabn[ext] -{number}`` - go the given tabs backwards
* ``:tabn[ext] +{number}`` - go the given tabs forwards
* ``:tabon[only][!] $`` - close all tabs except for the last tab (keep changes with ``!``)
* ``:tabon[only][!]`` - close all tabs except for the current tab (keep changes with ``!``)
* ``:tabon[only][!] {number}`` - close all tabs except for the given tab (starting since 1, keep changes with ``!``)
* ``:tabs`` - show a list of tabs and their windows

Windows
-------

* ``:clo[se][!]`` - close the window (keep changes with ``!``)
* ``CTRL + _`` - make the window highest posible
* ``CTRL + |`` - make the window widest posible
* ``CTRL + w + b`` - go to the bottom window
* ``CTRL + w + -`` - decrease the window height
* ``CTRL + w + <`` - decrease the window width
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
* ``CTRL + w + p`` - go to the previous window
* ``CTRL + w + R`` - move the window backwards
* ``CTRL + w + r`` - move the window forwards
* ``CTRL + w + t`` - go to the top window
* ``CTRL + w + T`` - move the window to a new tab
* ``CTRL + w + x`` - swap the current window and the next window
* ``{height} + CTRL + _`` - set the given height to the window
* ``:new`` - create an empty window horizontally
* ``:on[ly][!]`` - close all windows except for the current window (keep changes with ``!``)
* ``:q[uit][!]`` - close the window (discard changes with ``!``)
* ``:sp[lit] [file]`` - split the current window or open the given file horizontally
* ``:vnew`` - create an empty window vertically
* ``:vs[plit] [file]`` - split the current window or open the given file vertically
* ``{width} + CTRL + |`` - set the given width to the window



Technicalities
==============

Help Subjects
-------------

TODO

Search Patterns
---------------

TODO
