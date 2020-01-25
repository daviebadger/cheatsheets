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



Syntax
======

Scalars
-------

* Boolean (false) - ``false``
* Boolean (true) - ``true``
* Floating point (negative) - ``-1.0``
* Floating point (negative infinity) - ``-.inf``
* Floating point (positive) - ``1.0``
* Floating point (positive infinity) - ``.inf``
* Integer (negative) - ``-1``
* Integer (positive) - ``1``
* Null - ``null``
* String - ``text``

Mappings
--------

* Block mapping - ``key: value``
* Flow mapping (inline) - ``{key1: value, key2: value}``
* Flow mapping (multiline)::

     {
       key1: value,
       key2: value,
     }

Sequences
---------

* Block sequence - ``- value``
* Flow sequence (inline) - ``[value, value]``
* Flow sequence (multiline)::

     [
       value,
       value,
     ]