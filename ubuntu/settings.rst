***************
Ubuntu Settings
***************

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

   $ # Budgie panel
   $ dconf dump /com/solus-project/ > panel.dconf

Import
------

.. code-block:: console

   $ # Budgie panel
   $ dconf load /com/solus-project/ < panel.dconf

.. note::

   Reboot is needed after loading settings in order to see changes.

----

References
==========

* `AddictiveTips`_ - How To Back Up The Budgie Desktop Settings On Linux

.. _AddictiveTips: https://www.addictivetips.com/ubuntu-linux-tips/back-up-the-budgie-desktop-linux/
