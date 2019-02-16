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
     "background-color": "#color",
     "foreground-color": "#color",
     "palette": [
       "#dark-black",
       "#dark-red",
       "#dark-green",
       "#dark-yellow",
       "#dark-blue",
       "#dark-magenta",
       "#dark-cyan",
       "#dark-white",
       "#bright-black",
       "#bright-red",
       "#bright-green",
       "#bright-yellow",
       "#bright-blue",
       "#bright-magenta",
       "#bright-cyan",
       "#bright-white"
     ]
   }

.. note::

   If ``use-theme-colors`` is ``true``, then ``background-color`` and
   ``foreground-color`` are ignored. Instead of them are used colors from
   system theme.

References
==========

* `Tilix Documentation`_ - Tilix Themes

.. _Tilix Documentation: https://gnunn1.github.io/tilix-web/manual/themes/
