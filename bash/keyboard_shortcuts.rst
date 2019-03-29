************************************
Bash Command Line Keyboard Shortcuts
************************************

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright: `Creative Commons Attribution 4.0 International License`_

.. _Davie Badger: https://github.com/daviebadger
.. _Creative Commons Attribution 4.0 International License: https://creativecommons.org/licenses/by/4.0/

.. contents:: Table of Contents

Shortcuts
=========

Deleting
--------

* ``ALT + D`` - Delete to the end of current or following word
* ``ALT + W`` - Delete to the start of current or previous word
* ``CTRL + D`` - Delete the character at point (also ``DELETE``)
* ``CTRL + K`` - Delete text to the end of line
* ``CTRL + U`` - Delete text to the start of line
* ``CTRL + W`` - Delete to the start of current or previous word (until first space)

.. note::

   If there is no character in the command line, then ``CTRL + D`` means to
   exit from the shell, e.g. Bash, Python3, Psql or any other shell using
   Readline library.

Editing
-------

* ``ALT + C`` - Capitalize to the end of current or following word
* ``ALT + L`` - Lowercase to the end current or following word
* ``ALT + R`` - Undo all changes
* ``ALT + T`` - Transpose two words
* ``ALT + U`` - Uppcase to the end of current or following word
* ``CTRL + T`` - Trasponse two characters
* ``CTRL + _`` - Undo last change

History
-------

* ``ALT + >`` - Move to the end of history (empty line)
* ``CTRL + N`` - Show next command (also ``DOWN``)
* ``CTRL + P`` - Show previous command (also ``UP``)
* ``CTRL + R`` - Search backward for a command by ``CTRL + R``
* ``CTRL + S`` - Search forward for a command by ``CTRL + S`` (not working by default)

.. note::

   ``CTRL + S`` is reserved for freezing the terminal, unless ``CTRL + Q`` is
   pressed for unfreezing the terminal. This behaviour may be disabled via:

   .. code-block:: console

      $ [[ $- == *i* ]] && stty -ixon

Miscellaneous
-------------

* ``CTRL + L`` - Clear screen
* ``CTRL + X, CTRL + E`` - Open current command in an editor

.. tip::

   Single ``TAB`` for autocompliting commands, files or variables and double
   ``TAB`` for showing possible completions if there is no auto completion.

Movement
--------

* ``ALT + B`` - Move backward a word
* ``ALT + F`` - Move forward a word
* ``CTRL + A`` - Move to the start of the line
* ``CTRL + B`` - Move back one character (also ``LEFT``)
* ``CTRL + E`` - Move to the end of the line
* ``CTRL + F`` - Move forward one character (also ``RIGHT``)

Pasting
-------

* ``CTRL + Y`` - Paste the deleted text

----

References
==========

* `Bash Reference Manual - Command Line Editing <https://www.gnu.org/software/bash/manual/bash.html#Command-Line-Editing>`_
* `Unix & Linux Stack Exchange - How to cycle through reverse-i-search in BASH? <https://unix.stackexchange.com/questions/73498/how-to-cycle-through-reverse-i-search-in-bash>`_
* `Unix & Linux Stack Exchange - How to unfreeze after accidentally pressing Ctrl-S in a terminal? <https://unix.stackexchange.com/questions/12107/how-to-unfreeze-after-accidentally-pressing-ctrl-s-in-a-terminal>`_
