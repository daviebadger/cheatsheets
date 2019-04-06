***************
Bash Invocation
***************

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright: `Creative Commons Attribution 4.0 International License`_

.. _Davie Badger: https://github.com/daviebadger
.. _Creative Commons Attribution 4.0 International License: https://creativecommons.org/licenses/by/4.0/

.. contents:: Table of Contents

Invocation
==========

* ``bash`` - Create a new instance of Bash (subshell)
* ``bash <script>`` - Run the Bash script in a subshell
* ``bash -c '<command>'`` - Run the command or commands separated by ``;`` in a subshell
* ``bash --help`` - Show Bash usage
* ``bash --version`` - Show version information of current Bash instance

.. note::

   Bash may be also run in two special modes:

   * Restricted (``-r, --restricted`` or ``rbash``) - Several shell features are not supported, e.g. redirecting output
   * POSIX (``--posix``) - Shell without Bash features in order to conform the POSIX standard

   The POSIX mode can be also run via ``sh`` command, if ``/bin/sh`` is
   symlinked to ``/bin/bash``. On Debian-based distributions, the ``sh`` is
   interpreted by Dash (``/bin/dash``), which is fully POSIX-compliant shell.

.. tip::

   Bash should be run with a minimum options. If some options are required
   for running a script, then ``set`` command should be used for modifying
   shell options instead of specifying options in a shebang or Bash command:

   .. code-block:: bash

      #!/bin/bash

      set -eux

      # ...

----

References
==========

* `Bash Reference Manual - Bash POSIX Mode <https://www.gnu.org/software/bash/manual/bash.html#Bash-POSIX-Mode>`_
* `Bash Reference Manual - Invoking Bash <https://www.gnu.org/software/bash/manual/bash.html#Invoking-Bash>`_
* `Bash Reference Manual - The Restricted Shell <https://www.gnu.org/software/bash/manual/bash.html#The-Restricted-Shell>`_
* `Google - Shell Style Guide <https://google.github.io/styleguide/shell.xml>`_
* `nixCraft - Linux: What is Dash ( /bin/dash ) Shell? <https://www.cyberciti.biz/faq/debian-ubuntu-linux-binbash-vs-bindash-vs-binshshell/>`_
