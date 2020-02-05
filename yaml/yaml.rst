======
 YAML
======
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

* Boolean (false) - ``false``
* Boolean (true) - ``true``
* Floating point (negative) - ``-1.0``
* Floating point (negative infinity) - ``-.inf``
* Floating point (positive) - ``1.0``
* Floating point (positive infinity) - ``.inf``
* Integer (negative) - ``-1``
* Integer (positive) - ``1``
* Multi-line string - folded style (clip)::

     >
       word1
       word2

* Multi-line string - folded style (keep)::

     >+
       word1
       word2

* Multi-line string - folded style (strip)::

     >-
       word1
       word2

* Multi-line string - literal style (clip)::

     |
       line1
       line2

* Multi-line string - literal style (keep)::

     |+
       line1
       line2

* Multi-line string - literal style (strip)::

     |-
       line1
       line2
* Null - ``null``
* String - ``text``
* String (double-quoted) - ``"text"``
* String (single-quoted) - ``'text'``

Collections
===========

Mappings
--------

* Block mapping - ``key: value``
* Flow mapping (inline) - ``{key1: value, key2: value}``
* Flow mapping (multi-line)::

     {
       key1: value,
       key2: value,
     }

Sequences
---------

* Block sequence - ``- value``
* Flow sequence (inline) - ``[value, value]``
* Flow sequence (multi-line)::

     [
       value,
       value,
     ]

.. rename "Other" to something else?

Other
=====

* Alias - ``*name``
* Anchor - ``&name``
* Comment (block) - ``# comment``
* Comment (inline) - ``value  # comment``
* Document end - ``...``
* Document start - ``---``
* Merge mapping keys (from multiple mappings) - ``<<: [*alias1, *alias2]``
* Merge mapping keys (from one mapping) - ``<<: *alias``
* YAML directive - ``%YAML 1.2``
