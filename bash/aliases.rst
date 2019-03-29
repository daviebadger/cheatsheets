************
Bash Aliases
************

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright: `Creative Commons Attribution 4.0 International License`_

.. _Davie Badger: https://github.com/daviebadger
.. _Creative Commons Attribution 4.0 International License: https://creativecommons.org/licenses/by/4.0/

.. contents:: Table of Contents

Aliases
=======

Commands
--------

* ``alias`` - Show all aliases created via ``alias`` command
* ``alias alias_name='<command>'`` - Create one or more aliases
* ``unalias <alias_name>`` - Unalias one or more aliases
* ``unalias -a`` - Unalias all aliases

.. note::

   Aliases work only within the interactive shell, not in a script, unless
   a shell option ``expand_aliases`` is explicitly enabled (not recommended,
   functions should be used instead, they are commands too):

   .. code-block:: sh

      #!/bin/bash

      shopt -s expand_aliases

Storing aliases
---------------

* ``~/.bash_aliases`` - Aliases and functions as commands

.. note::

   On Ubuntu Budgie, ``~/.bash_aliases`` is automatically sourced from
   ``~/.bashrc`` via:

   .. code-block:: sh

      if [ -f ~/.bash_aliases ]; then
          . ~/.bash_aliases
      fi

----

References
==========

* `Bash Reference Manual - Aliases <https://www.gnu.org/software/bash/manual/bash.html#Aliases>`_
