*********************
Shell Text Formatting
*********************

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright: `Creative Commons Attribution 4.0 International License`_

.. _Davie Badger: https://github.com/daviebadger
.. _Creative Commons Attribution 4.0 International License: https://creativecommons.org/licenses/by/4.0/

.. contents:: Table of Contents

Text Formatting
===============

Set
---

* ``1`` - Bold - ``\e[1mBold text`` or ``\033[1mBold text``
* ``2`` - Dim
* ``3`` - Italic
* ``4`` - Underline (aso ``4:1``)
* ``4:2`` - Double underline (aso ``21``)
* ``4:3`` - Curly underline
* ``5`` - Blink
* ``7`` - Reverse foreground and background colors
* ``8`` - Hidden (but copy-pasteable)
* ``9`` - Strikethrough
* ``53`` - Overline

.. note::

   Terminal emulators should support these text formats unlike real terminals.

.. tip::

   Text formats can be also combined using ``;`` separator:

   .. code-block:: console

      $ echo '\e[1;3;4mBold and italic and underline\e[0m'  # sh
      Bold and italic and underline
      $ echo -e '\e[1;3;4mBold and italic and underline\e[0m'  # bash
      Bold and italic and underline

Reset
-----

* ``0`` - Reset to normal text, default foreground and background colors - ``\e[0m`` or ``\033[0m``

.. note::

   ``0`` can be used also as normal text for colored text, if the first code
   is right ``0``, otherwise it will reset all attributes (text formatting
   and colors):

   .. code-block:: console

      $ echo '\e[0;30;42mNormal black foreground, green background\e[0m'  # sh
      Normal black foreground, green background
      $ echo -e '\e[0;30;42mNormal black foreground, green background\e[0m'  # bash
      Normal black foreground, green background
      $ # vs
      $ echo '\e[30;42;0mNormal default foreground, default background\e[0m'  # sh
      Normal default foreground, default background
      $ echo -e '\e[30;42;0mNormal default foreground, default background\e[0m'  # bash
      Normal default foreground, default background

----

References
==========

* `Ask Ubuntu - How to do: underline, bold, italic, strikethrough, color, background, and size in Gnome Terminal? <https://askubuntu.com/questions/528928/how-to-do-underline-bold-italic-strikethrough-color-background-and-size-i>`_
* `FLOZz' MISC - Bash tips: Colors and formatting <https://misc.flogisoft.com/bash/tip_colors_and_formatting>`_
