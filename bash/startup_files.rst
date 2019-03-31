******************
Bash Startup Files
******************

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright: `Creative Commons Attribution 4.0 International License`_

.. _Davie Badger: https://github.com/daviebadger
.. _Creative Commons Attribution 4.0 International License: https://creativecommons.org/licenses/by/4.0/

.. contents:: Table of Contents

Startup Files
=============

Login shell
-----------

Both interactive and non-interactive shells after login:

#. ``/etc/profile.d/*.sh``
#. ``/etc/profile``
#. ``~/.bash_profile`` or ``~/.bash_login`` or ``~/.profile`` (first matched in that order)

Both interactive and non-interactive shells after logout (exit):

#. ``~/.bash_logout``

.. note::

   Terminal emulators run commands as a non-login shell by default, although
   users are logged in. This behaviour may be changed in settings to run
   commands as a login shell.

.. tip::

   On Ubuntu Budgie, both ``~/.bash_profile`` and ``~/.bash_login`` do not
   exists. The first one should be used for shell customization with sourcing
   ``~/.bashrc`` like in ``~/.profile`` (best practice):

   .. code-block:: sh

      #!/bin/bash

      if [ -f ~/.bashrc ]; then
        . ~/.bashrc
      fi

Non-login shell
---------------

Interactive shell:

#. ``/etc/bash.bashrc``
#. ``~/.bashrc``

Non-interactive shell:

#. no startup files

.. note::

   ``/etc/bash.bashrc`` is also sourced in a login shell from ``/etc/profile``.

References
==========

* `Bash Reference Manual - Bash Startup Files <https://www.gnu.org/software/bash/manual/bash.html#Bash-Startup-Files>`_
* ``/etc/`` - System configuration files
