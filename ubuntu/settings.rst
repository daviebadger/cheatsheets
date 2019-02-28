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
   $ dconf dump /com/solus-project/budgie-panel/ > panel.dconf
   $ # GNOME desktop
   $ dconf dump /org/gnome/desktop/ > desktop.dconf
   $ # Keyboard shortcuts and other GNOME plugins
   $ dconf dump /org/gnome/settings-daemon/plugins/ > plugins.dconf
   $ # Mutter (window manager)
   $ dconf dump /org/gnome/mutter/ > mutter.dconf

Import
------

.. code-block:: console

   $ dconf load /com/solus-project/budgie-panel/ < panel.dconf
   $ dconf load /org/gnome/desktop/ < desktop.dconf
   $ dconf load /org/gnome/settings-daemon/plugins/ < plugins.dconf
   $ dconf load /org/gnome/mutter/ < mutter.dconf

.. note::

   Some settings (e.g. Budgie panel) require reboot in order to see changes
   while others not (e.g. GNOME desktop).

----

References
==========

* `AddictiveTips`_ - How To Back Up The Budgie Desktop Settings On Linux

.. _AddictiveTips: https://www.addictivetips.com/ubuntu-linux-tips/back-up-the-budgie-desktop-linux/
