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

Editing
-------

* ``ALT + C`` - Capitalize to the end of the current or following word
* ``ALT + L`` - Lowercase to the end the current or following word
* ``ALT + R`` - Undo all changes
* ``ALT + T`` - Transpose two words
* ``ALT + U`` - Uppcase to the end of the current or following word
* ``CTRL + T`` - Trasponse two characters
* ``CTRL + _`` - Undo the last change

History
-------

* ``ALT + >`` - Move to the end of history (empty line)
* ``CTRL + N`` - Show the next command (also ``DOWN``)
* ``CTRL + P`` - Show the previous command (also ``UP``)
* ``CTRL + R`` - Search backward for a command by ``CTRL + R``
* ``CTRL + S`` - Search forward for a command by ``CTRL + S`` (also ``CTRL + SHIFT + R``)

.. note::

   ``CTRL + S`` is reserved for freezing the terminal by default, unless
   ``CTRL + Q`` is pressed for unfreezing the terminal. This behaviour may be
   disabled via:

   .. code-block:: console

      $ [[ $- == *i* ]] && stty -ixon

Movement
--------

* ``ALT + B`` - Move backward a word
* ``ALT + F`` - Move forward a word
* ``CTRL + A`` - Move to the start of the line
* ``CTRL + B`` - Move back one character (also ``LEFT``)
* ``CTRL + E`` - Move to the end of the line
* ``CTRL + F`` - Move forward one character (also ``RIGHT``)

----

References
==========

* `Bash Reference Manual`_ - Command Line Editing
* `Unix & Linux Stack Exchange`_ - How to cycle through reverse-i-search in BASH?
* `Unix & Linux Stack Exchange`_ - How to unfreeze after accidentally pressing Ctrl-S in a terminal?

.. _Bash Reference Manual: https://www.gnu.org/software/bash/manual/bash.html
.. _Unix & Linux Stack Exchange: https://unix.stackexchange.com
