**************
Tilix Settings
**************

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright: `Creative Commons Attribution 4.0 International License`_

.. _Davie Badger: https://github.com/daviebadger
.. _Creative Commons Attribution 4.0 International License: https://creativecommons.org/licenses/by/4.0/

.. contents:: Table of Contents

Settings
========

Export
------

.. code-block:: console

   $ dconf dump /com/gexperts/Tilix/ > tilix.dconf

Import
------

.. code-block:: console

   $ dconf load /com/gexperts/Tilix/ < tilix.dconf

.. note::

   Imported settings immediately update all running Tilix instances.

----

References
==========

* `Tilix News - 1.5.4 release <https://gnunn1.github.io/tilix-web/2017/03/18/release-1-5-4>`_
