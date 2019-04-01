************
Shell Colors
************

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright: `Creative Commons Attribution 4.0 International License`_

.. _Davie Badger: https://github.com/daviebadger
.. _Creative Commons Attribution 4.0 International License: https://creativecommons.org/licenses/by/4.0/

.. contents:: Table of Contents

Colors
======

Foreground
----------

* ``39`` - Default foreground color - ``\e[39mDefault foreground color``
* ``30`` - Black
* ``31`` - Red
* ``32`` - Green
* ``33`` - Yellow
* ``34`` - Blue
* ``35`` - Magenta
* ``36`` - Cyan
* ``37`` - Light grey
* ``90`` - Dark grey
* ``91`` - Light red
* ``92`` - Light green
* ``93`` - Light yellow
* ``94`` - Light blue
* ``95`` - Light magenta
* ``96`` - Light cyan
* ``97`` - White

.. note::

   Users may change color palette in their terminal emulators, e.g. using
   only 8 colors instead of 16 colors, different color shades or even colors.

.. tip::

   It is a best practice to reset colors back to default colors at the end of
   colored text using ``\e[0m`` escape sequence:

   .. code-block:: console

      $ echo '\e[31mRed color\e[0m'  # sh
      Red color
      $ echo -e '\e[31mRed color\e[0m'  # bash
      Red color

Background
----------

* ``49`` - Default background color - ``\e[49mDefault background color``
* ``40`` - Black
* ``41`` - Red
* ``42`` - Green
* ``43`` - Yellow
* ``44`` - Blue
* ``45`` - Magenta
* ``46`` - Cyan
* ``47`` - Light grey
* ``100`` - Dark grey
* ``101`` - Light red
* ``102`` - Light green
* ``103`` - Light yellow
* ``104`` - Light blue
* ``105`` - Light magenta
* ``106`` - Light cyan
* ``107`` - White

.. note::

   For escaping colors, ``\033`` also can be used, if ``\e`` is not working,
   e.g. in a Python shell:

   .. code-block:: console

      $ python3 -c 'print("\033[31mRed text\033[0m")'
      Red text

.. tip::

   Foreground and background colors can be combined using ``;`` separator:

   .. code-block:: console

      $ echo '\e[30;42mBlack foreground, green background\e[0m'  # sh
      Black foreground, green background
      $ echo -e '\e[30;42mBlack foreground, green background\e[0m'  # bash
      Black foreground, green background

   The same goes for text formatting:

   .. code-block:: console

      $ echo '\e[1;30;42mBold black foreground, green background\e[0m'  # sh
      Bold black foreground, green background
      $ echo -e '\e[1;30;42mBold black foreground, green background\e[0m'  # bash
      Bold black foreground, green background

----

References
==========

* `FLOZz' MISC - Bash tips: Colors and formatting <https://misc.flogisoft.com/bash/tip_colors_and_formatting>`_
