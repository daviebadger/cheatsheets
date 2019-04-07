****************
Shell Parameters
****************

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright: `Creative Commons Attribution 4.0 International License`_

.. _Davie Badger: https://github.com/daviebadger
.. _Creative Commons Attribution 4.0 International License: https://creativecommons.org/licenses/by/4.0/

.. contents:: Table of Contents

Parameters
==========

Special
-------

* ``$*`` - Expand positional parameters to words delimited by space if not double quoted else to single string
* ``$@`` - Expand positional parameters to words delimited by space if not double quoted else to multiple strings
* ``$#`` - Expand number of positional parameters
* ``$?`` - Expand exit status of the most recently executed foreground pipeline
* ``$-`` - Expand option flags set to the shell upon invocation or via ``set`` command
* ``$$`` - Expand process ID of the shell (same in current shell and in subshells)
* ``$!`` - Expand process ID of the job most recently placed into background
* ``$0`` - Expand name of the shell or shell script (if starts with ``-``, it is a login shell)
* ``$_`` - Expand the last argument of the last foreground command after expansion or command name or variable name

.. note::

   Shell may be run with implicitly set option flags:

   .. code-block:: console

      $ echo $-
      himBHs
      $ bash  # subshell
      $ echo $-
      himBHs
      $ exit
      $ bash -c 'echo $0'
      hBc

   Options:

   * ``B`` - perform brace expansion
   * ``c`` - execute the command
   * ``H`` - enable history substitution with ``!``
   * ``h`` - remember the location of commands as they are looked up
   * ``i`` - interactive shell
   * ``m`` - enable job control
   * ``s`` - read commands from standard input

.. tip::

   Special parameters should be used without quotes unless it is necessary to
   use double quoutes for desired result:

   .. code-block:: console

      $ cat tesh.sh
      #!/bin/bash

      echo '"$*"'

      for arg in "$*"; do
        echo $arg
      done

      echo
      echo '$*'

      for arg in $*; do
        echo $arg
      done

      echo
      echo '"$@"'

      for arg in "$@"; do
        echo $arg
      done

      echo
      echo '$@'

      for arg in $@; do
        echo $arg
      done
      $ ./test.sh one 'two three'
      "$*"
      one two three

      $*
      one
      two
      three

      "$@"
      one
      two three

      $@
      one
      two
      three

----

References
==========

* `Bash Reference Manual - Special Parameters <https://www.gnu.org/software/bash/manual/bash.html#Special-Parameters>`_
* `Unix & Linux Stack Exchange - $BASHPID And $$ differ in some cases <https://unix.stackexchange.com/questions/62231/bashpid-and-differ-in-some-cases>`_
* `Unix & Linux Stack Exchange - What's the difference between $@ and $* <https://unix.stackexchange.com/questions/129072/whats-the-difference-between-and>`_
