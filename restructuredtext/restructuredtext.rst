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


Markup
======

Block Elements
--------------

* Block quote:

  .. code:: rst

     ordinary-paragraph

        block-quote

* Comment - ``.. comment``
* Transition - ``----``
* Substitution definition - ``.. |substitution| directive-name:: substituted-text``

Inline Markup
-------------

* Citation reference - ``[label]_``
* Emphasis - ``*italic*``
* Footnote reference (auto-numbered) - ``[#]_``
* Footnote reference (manual) - ``[number]_``
* Hyperlink reference (anonymous phrase)- :literal:`\`phrase\`__`
* Hyperlink reference (anonymous word)- ``word__``
* Hyperlink reference (named phrase)- :literal:`\`phrase\`_`
* Hyperlink reference (named word)- ``word_``
* Inline literal - :literal:`\`\`code-snippet\`\``
* Standalone hyperlink (email) - ``davie.badger@gmail.com``
* Standalone hyperlink (URI) - ``http://github.com/daviebadger``
* Strong emphasis - ``**bold**``
* Substitution reference - ``|substitution|``


Directives
==========

* ``.. admonition:: title`` - Add a custom admonition with the given title
* ``.. attention::`` - Add attentive info
* ``.. caution::`` - Add cautious info
* ``.. class:: class-names`` - Add HTML classes to the following element
* ``.. code:: language`` - Add code with syntax highlighting
* ``.. contents::`` - Generate a table of contents
* ``.. csv-table:: optional-title`` - Add a CSV table
* ``.. danger::`` - Add dangerous info
* ``.. |substitution| date:: optional-format`` - Substitute for a date(time)
* ``.. default-role:: role-name`` - Set a new default role
* ``.. figure:: path/to/image`` - Add an image with a caption
* ``.. highlights`` - Add a summary
* ``.. hint::`` - Add a hint
* ``.. image:: path/to/image`` - Add an image
* ``.. important::`` - Add important info
* ``.. include:: path/to/file`` - Load text from a file
* ``.. list-table:: optional-title`` - Add a list-like table
* ``.. math::`` - Add a mathematical formula in LaTeX format
* ``.. meta::`` - Add HTML meta tags
* ``.. note::`` - Add a note
* ``.. raw:: output-formats`` - Bypass parsing text for the given output formats
* ``.. |substitution| replace:: text`` - Substitute for a text
* ``.. role:: role-name`` - Create a new role by aliasing or overloading
* ``.. rubric:: text`` - Add an informal heading
* ``.. sectnum::`` - Automatically number sections
* ``.. table:: optional-title`` - Add a wrapped table
* ``.. tip::`` - Add a tip
* ``.. title:: title`` - Set a different HTML title for a browser tab
* ``.. topic:: title`` - Add a topic container
* ``.. |substitution| unicode:: code`` - Substitute for a Unicode character
* ``.. warning::`` - Add a warning

Roles
=====

* ``:literal:`\```` - Inline code sample with escaped backslashes
* ``:math:`f(x) = x^2``` - Inline mathematical formula in LaTeX format
* ``:sub:`2``` - Subscript
* ``:sup:`2``` - Superscript
* ``:title:`How to Title My Book``` - Title of a work
* ``:PEP:`8``` - Link to a specific PEP
* ``:RFC:`3339``` - Link to a specific RFC
