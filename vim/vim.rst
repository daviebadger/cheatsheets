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

* ``a`` - switch to Insert mode after the cursor
* ``A`` - switch to Insert mode at the end of a line
* ``CTRL + v`` - switch to Visual mode blockwise
* ``ESC`` - switch to Normal mode
* ``I`` - switch to Insert mode at the start of a line
* ``i`` - switch to Insert mode in place of the cursor
* ``o`` - switch to Insert mode in a new line below the cursor
* ``O`` - switch to Insert mode in a new line above the cursor
* ``v`` - switch to Visual mode characterwise
* ``V`` - switch to Visual mode linewise
* ``{visual-block} + I`` - switch to Insert mode at the start of a highlighted block
* ``{visual-block} + A`` - switch to Insert mode at the end of a highlighted block

Left-Right Motions

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
* ``T + {char}`` - go before to the given character left in a line
* ``t + {char}`` - go before to the given character right in a line

Up-Down Motions

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

Other Motions

* ``%`` - go to matching brace, bracket, parenthesis
* ``H`` - go to the top of a window
* ``M`` - go to the center of a window
* ``L`` - go to the bottom of a window

Text Object Motions

* ``b`` - go to the start of a current or previous "word"
* ``B`` - go to the start of a current or previous word
* ``e`` - go to the end of a current or the next "word"
* ``E`` - go to the end of a current or the next word
* ``ge`` - go to the end of a previous "word"
* ``gE`` - go to the end of a previous word
* ``w`` - go to the start of the next "word"
* ``W`` - go to the start of the next word

Scrolling

* ``CTRL + b`` - scroll 1 window backwards
* ``CTRL + d`` - scroll 1/2 window forwards
* ``CTRL + f`` - scroll 1 window forwards
* ``CTRL + u`` - scroll 1/2 window backwards
* ``zb`` - scroll current line to the bottom of a window
* ``zH`` - scroll 1/2 screen width left (wrap is off)
* ``zh`` - scroll screen width 1 character to left (wrap is off)
* ``zL`` - scroll 1/2 screen width right (wrap is off)
* ``zl`` - scroll screen width 1 character to right (wrap is off)
* ``zt`` - scroll current line to the top of a window
* ``zz`` - scroll current line to the center of a window

Deleting Text

* ``dd`` - delete current line
* ``D`` - delete to the end of a line
* ``d + {motion}`` - delete to the given motion
* ``gJ`` - join lines without space
* ``J`` - join lines with space
* ``{visual} + d`` - delete highlighted text
* ``{visual} + gJ`` - join highlighted lines without space
* ``{visual} + J`` - join highlighted lines with space
* ``x`` - delete a chara
* ``X`` - delete a character before the cursor

Copying/Pasting Text

* ``p`` - put text after the cursor
* ``P`` - put text before the cursor
* ``{visual} + y`` - yank highlighted text
* ``y + {motion}`` - yank to the given motion
* ``Y`` - yank current line
* ``yy`` - yank current line

Undo/Redo Changes

* ``u`` - undo the last change
* ``U`` - undo a whole recently changed line
* ``CTRL + r`` - redo the last change

Visual Mode Commands

* ``o`` - go to the opposite edge of a highlighted text
* ``gv`` - highlight a recently highlighted text
