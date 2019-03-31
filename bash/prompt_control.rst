*******************
Bash Prompt Control
*******************

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright: `Creative Commons Attribution 4.0 International License`_

.. _Davie Badger: https://github.com/daviebadger
.. _Creative Commons Attribution 4.0 International License: https://creativecommons.org/licenses/by/4.0/

.. contents:: Table of Contents

Prompt
======

Special characters
------------------

* ``\@`` - time in 12-hour HH:MM format
* ``\A`` - time in 24-hour HH:MM format
* ``\D{format}`` - formatted date using format controls from ``date`` command
* ``\h`` - hostname up to the first ``.``
* ``\H`` - hostname
* ``\e`` - escape character for ANSI colors
* ``\n`` - newline
* ``\t`` - time in 24-hour HH:MM:SS format
* ``\T`` - time in 12-hour HH:MM:SS format
* ``\u`` - current user's username
* ``\w`` - current working directory, with ``$HOME`` as ``~``
* ``\W`` - basename of ``$PWD``, with ``$HOME`` as ``~``
* ``\$`` - ``#`` for the root user, otherwise ``$`` for other users
* ``\[`` - begin a sequence of non-printing characters
* ``\]`` - end a sequence of non-printing characters

.. note::

   ``\[`` and ``\]`` are usually used for escaping colors in prompt strings:

   .. code-block: sh

      "\[\e[32m\]\w\[\e[0m\] \$"

Variables
---------

* ``PROMPT_COMMAND`` - Command to be executed before printing ``PS1``
* ``PROMPT_DIRTRIM`` - Number of trailling directories to show after ``\w`` expansion
* ``PS1`` - Prompt string displayed before a command
* ``PS2`` - Prompt string displayed before multi-line text
* ``PS4`` - Prompt string displayed before commands when using ``set -x`` for debugging

.. note::

   Prompt strings are just quoted strings with / without substitutions, escaped
   ANSI colors or special characters.

.. tip::

   ``PS1`` should be set inside a ``PROMPT_COMMAND`` function in order to
   prevent other programs to modify ``PS1`` value, e.g. virtualenvs in Python,
   if this behaviour is not desired.

Storing prompt settings
-----------------------

* ``~/.bashrc`` - Prompt strings

.. tip::

   Complex prompt strings with several lines of code should be set in
   ``~/.bash_prompt`` and sourced from a startup file.

----

References
==========

* `Bash Reference Manual - Bash Variables <https://www.gnu.org/software/bash/manual/bash.html#Bash-Variables>`_
* `Bash Reference Manual - Bourne Shell Variables <https://www.gnu.org/software/bash/manual/bash.html#Bourne-Shell-Variables>`_
* `Bash Reference Manual - Controlling the Prompt <https://www.gnu.org/software/bash/manual/bash.html#Controlling-the-Prompt>`_
