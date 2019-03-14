************
Tilix Themes
************

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright: `Creative Commons Attribution 4.0 International License`_

.. _Davie Badger: https://github.com/daviebadger
.. _Creative Commons Attribution 4.0 International License: https://creativecommons.org/licenses/by/4.0/

.. contents:: Table of Contents

Themes
======

Default
-------

.. code-block:: console

   $ ls -1 /usr/share/tilix/schemes
   base16-twilight-dark.json
   linux.json
   material.json
   monokai.json
   orchis.json
   solarized-dark.json
   solarized-light.json
   tango.json

External
--------

* https://github.com/storm119/Tilix-Themes
* https://github.com/isacikgoz/gogh-to-tilix

Custom
------

JSON file with hexadecimal colors stored in ``~/.config/tilix/schemes``:

.. code-block:: json

   {
     "name": "Name",
     "comment": "Comment",
     "use-theme-colors": false,
     "foreground-color": "#color",
     "background-color": "#color",
     "palette": [
       "#black",
       "#dark-red",
       "#dark-green",
       "#dark-yellow",
       "#dark-blue",
       "#dark-magenta",
       "#dark-cyan",
       "#light-grey",
       "#dark-grey",
       "#light-red",
       "#light-green",
       "#light-yellow",
       "#light-blue",
       "#light-magenta",
       "#light-cyan",
       "#white"
     ]
   }

.. note::

   If ``use-theme-colors`` is ``true``, then ``background-color`` with
   ``foreground-color`` are ignored and instead of them are used colors from
   system theme.

Testing themes
==============

.. code-block:: console

   $ cat preview.sh
   #!/usr/bin/env bash

   echo
   echo -e '  \e[0;30m████ \e[0;31m████ \e[0;32m████ \e[0;33m████ \e[0;34m████ \e[0;35m████ \e[0;36m████ \e[0;37m████\e[0m'
   echo -e '  \e[0;30m████ \e[0;31m████ \e[0;32m████ \e[0;33m████ \e[0;34m████ \e[0;35m████ \e[0;36m████ \e[0;37m████\e[0m'
   echo -e '  \e[0;90m████ \e[0;91m████ \e[0;92m████ \e[0;93m████ \e[0;94m████ \e[0;95m████ \e[0;96m████ \e[0;97m████\e[0m'
   echo -e '  \e[0;90m████ \e[0;91m████ \e[0;92m████ \e[0;93m████ \e[0;94m████ \e[0;95m████ \e[0;96m████ \e[0;97m████\e[0m'
   echo
   $ chmod +x preview.sh
   $ ./preview.sh

     ████ ████ ████ ████ ████ ████ ████ ████
     ████ ████ ████ ████ ████ ████ ████ ████
     ████ ████ ████ ████ ████ ████ ████ ████
     ████ ████ ████ ████ ████ ████ ████ ████

References
==========

* `Gogh.sh - Print colored Unicode Full Block characters <https://github.com/Mayccoll/Gogh/blob/f1f51de1d6f1e809135e8b1dde78ecc7787e75b4/gogh.sh#L218>`_
* `Tilix Documentation - Themes <https://gnunn1.github.io/tilix-web/manual/themes/>`_
