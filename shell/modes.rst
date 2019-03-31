***********
Shell Modes
***********

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright: `Creative Commons Attribution 4.0 International License`_

.. _Davie Badger: https://github.com/daviebadger
.. _Creative Commons Attribution 4.0 International License: https://creativecommons.org/licenses/by/4.0/

.. contents:: Table of Contents

Modes
=====

Types of modes
--------------

* ``interactive shell`` - user can directly interact with a shell (the shell is connected to user's terminal)
* ``non-interactive shell`` - user cannot directly interact with a shell

Furthermore, these types of shells can be also:

* ``login shell`` - shell run after successful user's login
* ``non-login shell`` - subshell from the login shell or other subshell

.. note::

   All these modes can combined:

   * ``interactive`` and ``login`` shell
   * ``interactive`` and ``non-login`` shell
   * ``non-interactive`` and ``login`` shell (e.g. ssh to a server with instructions in a redirected input)
   * ``non-interactive`` and ``non-login`` shell (e.g. a script run in a subshell)

Mode detection
--------------

* interactive vs non-interactive shell:

  .. code-block:: console

     $ case "$-" in *i*) echo 'interactive';; *) echo 'non-interactive';; esac
     interactive
     $ # or
     $ [ ! -z "$PS1" ] && echo 'interactive' || echo 'non-interactive'
     interactive

* login vs non-login shell:

  .. code-block:: console

     $ case "$0" in -*) echo 'login';; *) echo 'non-login';; esac

----

References
==========

* `Ask Ubuntu - Differentiate Interactive login and non-interactive non-login shell <https://askubuntu.com/questions/879364/differentiate-interactive-login-and-non-interactive-non-login-shell>`_
* `Bash Reference Manual - Interactive Shells <https://www.gnu.org/software/bash/manual/bash.html#Interactive-Shells>`_
* `The UNIX School: Login shell or a non-login shell?  <http://www.theunixschool.com/2010/05/login-shell-or-non-login-shell.html>`_
