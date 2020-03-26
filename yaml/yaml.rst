==========
 YAML 1.2
==========
------------------------------------------
 Human-Readable Data Serialization Format
------------------------------------------

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright:
   `Creative Commons Attribution-ShareAlike 4.0 International Public License`__

.. contents::

.. sectnum::
   :suffix: .

__ https://creativecommons.org/licenses/by-sa/4.0/

.. _Davie Badger: https://github.com/daviebadger



Scalars
=======

* Block string - folded style (clip)::

     >
       text

* Block string - folded style (strip)::

     >-
       text

* Block string - literal style (clip)::

     |
       text

* Block string - literal style (strip)::

     |-
       text

* Boolean (false) - ``false``
* Boolean (true) - ``true``
* Floating point (negative) - ``-1.0``
* Floating point (negative infinity) - ``-.inf``
* Floating point (negative scientific notation) - ``-1e+0``
* Floating point (positive) - ``1.0``
* Floating point (positive infinity) - ``.inf``
* Floating point (positive scientific notation) - ``1e+0``
* Flow string (double-quoted) - ``"text"``
* Flow string (plain)- ``text``
* Flow string (single-quoted) - ``'text'``
* Integer (negative) - ``-1``
* Integer (positive) - ``1``
* Null - ``null``
* Timestamp (date) - ``2020-02-20``
* Timestamp (datetime ISO) - ``2020-02-20T00:00:00``
* Timestamp (datetime spaced) - ``2020-02-20 00:00:00``



Collections
===========

Mappings
--------

* Block mapping - ``key: value``
* Flow mapping - ``{key1: value, key2: value}``

Sequences
---------

* Block sequence - ``- value``
* Flow sequence - ``[value, value]``



Other Indicators
================

* Alias - ``*name``
* Anchor - ``&name value``
* Comment (block) - ``# comment``
* Comment (inline) - ``value  # comment``
* Document directive - ``%YAML 1.2``
* Document end - ``...``
* Document start - ``---``
* Merge mapping keys (from multiple mappings) - ``<<: [*alias1, *alias2]``
* Merge mapping keys (from one mapping) - ``<<: *alias``
