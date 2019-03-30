**************
Bash Variables
**************

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright: `Creative Commons Attribution 4.0 International License`_

.. _Davie Badger: https://github.com/daviebadger
.. _Creative Commons Attribution 4.0 International License: https://creativecommons.org/licenses/by/4.0/

.. contents:: Table of Contents

Variables
=========

* ``BASH`` - Absolute path to the executable file of current Bash instance
* ``BASHOPTS`` - List of enabled shell options separated by ``:``
* ``BASHPID`` - Current Bash process ID
* ``BASH_VERSINFO`` - Array with version information (major, minor, patch, etc.)
* ``BASH_VERSION`` - Current Bash version
* ``COLUMNS`` - Terminal width
* ``HISTCMD`` - Current command index in history
* ``HISTCONTROL`` - List of rules for saving commands in history separated by ``:``
* ``HISTFILE`` - Absolute path to the history file
* ``HISTFILESIZE`` - Number of lines to keep in the history file
* ``HISTSIZE`` - Number of commands to remember in history
* ``HOSTNAME`` - Current hostname
* ``LANG`` - Default locale language with charset for other ``LC_`` variables (time, numbers, etc.)
* ``LINES`` - Terminal height
* ``OLDPWD`` - Previous working directory
* ``PPID`` - Shell's parent process ID
* ``PROMPT_COMMAND`` - Command to be executed before printing ``PS1`` (may be already set by system)
* ``PROMPT_DIRTRIM`` - Number of trailling directories to show after ``\w`` expansion
* ``PS4`` - Prompt string displayed before commands when using ``set -x`` for debugging
* ``PWD`` - Current working directory
* ``RANDOM`` - Random number between 0 and 32767
* ``SECONDS`` - Number of seconds since shell was started
* ``SHELL`` - Absolute path to user's shell
* ``SHLVL`` - Current shell level (in nested shells)
* ``UID`` - Currents user's ID

.. note::

   In Ubuntu Budgie, the ``PROMPT_COMMAND`` variable is used by Tilix via VTE
   (Virtual Terminal Emulator) widget to feed itself with additional
   information from the shell:

   .. code-block:: console

      $ echo $PROMPT_COMMAND
      __vte_prompt_command

.. tip::

   Another variables may be set by various programs, for example the ``login``
   program sets:

   * ``LOGNAME`` - current user's username
   * ``TERM`` - terminal type

   Current user's username may be also set in ``USER`` variable and language in
   ``LANGUAGE`` variable.

----

References
==========

* `Bash Reference Manual - Bash Variables <https://www.gnu.org/software/bash/manual/bash.html#Bash-Variables>`_
* `Tilix Documentation - VTE Configuration <https://gnunn1.github.io/tilix-web/manual/vteconfig/>`_
* `Unix & Linux Stack Exchange - Who sets $USER and $USERNAME environment variables? <https://unix.stackexchange.com/questions/76354/who-sets-user-and-username-environment-variables>`_
