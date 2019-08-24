==================
 reStructuredText
==================
---------------------------------------------------------
 Lightweight Markup Language for Technical Documentation
---------------------------------------------------------

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright: `Creative Commons Attribution 4.0 International Public License`_

.. contents::

.. sectnum::
   :suffix: .

.. _Creative Commons Attribution 4.0 International Public License: https://creativecommons.org/licenses/by/4.0/
.. _Davie Badger: https://github.com/daviebadger



Directives
==========

Directives are used as block markup defined on a separate line:

* ``.. admonition:: title`` - Add a custom admonition with the given title
* ``.. attention::`` - Add attentive info
* ``.. caution::`` - Add cautious info
* ``.. class:: class-names`` - Add HTML classes to the following element
* ``.. contents::`` - Generate a table of contents
* ``.. danger::`` - Add dangerous info
* ``.. default-role:: role-name`` - Set a new default role
* ``.. hint::`` - Add a hint
* ``.. important::`` - Add important info
* ``.. include:: path/to/file`` - Load text from a file
* ``.. meta::`` - Add HTML meta tags
* ``.. note::`` - Add a note
* ``.. raw:: output-formats`` - Bypass parsing text for the given output formats
* ``.. role:: new-role-name`` - Create a new role by aliasing or overloading
* ``.. sectnum::`` - Automatically number sections
* ``.. tip::`` - Add a tip
* ``.. title:: title`` - Set a different HTML title for a browser tab
* ``.. warning::`` - Add a warning



Roles
=====

Interpreted text roles are used as inline markup in text with spaces around,
either hard-typed or escaped, except for punctuation marks:

* ``:literal:`\```` - Inline code sample with escaped backslashes
* ``:math:`f(x) = x^2``` - Inline mathematical formula in LaTeX format
* ``:sub:`2``` - Subscript
* ``:sup:`2``` - Superscript
* ``:title:`How to Title My Book``` - Title of a work
* ``:PEP:`8``` - Link to a specific PEP
* ``:RFC:`3339``` - Link to a specific RFC
