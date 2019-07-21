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
   :depth: 3
   :suffix: .

.. _Creative Commons Attribution 4.0 International Public License: https://creativecommons.org/licenses/by/4.0/
.. _Davie Badger: https://github.com/daviebadger



Directives
==========

Directives are used as block elements defined on a separate line:

* ``.. admonition:: title`` - Add a custom admonition with the given title
* ``.. attention:: text`` - Add attentive info
* ``.. caution:: text`` - Add cautious info
* ``.. danger:: text`` - Add dangerous info
* ``.. default-role:: role-name`` - Set a new default role
* ``.. hint:: text`` - Add a hint
* ``.. important:: text`` - Add important info
* ``.. note:: text`` - Add a note
* ``.. role:: new-role-name`` - Create a new role by aliasing or overloading
* ``.. tip:: text`` - Add a tip
* ``.. warning:: text`` - Add a warning



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
