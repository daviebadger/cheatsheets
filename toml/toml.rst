============
 TOML 1.0.0
============
-----------------------------------
 Minimal Configuration File Format
-----------------------------------

:Author: `Davie Badger`_
:Contact: davie.badger@gmail.com
:Copyright:
   `Creative Commons Attribution-ShareAlike 4.0 International Public License`__

.. contents::

.. sectnum::
   :suffix: .

__ https://creativecommons.org/licenses/by-sa/4.0/

.. _Davie Badger: https://github.com/daviebadger



Keys
====



Values
======

* Array - ``[ 1, 2, 3 ]``
* Basic string (inline) - ``"text"``
* Basic string (multi-line)::

     """
     text"""

* Boolean (false) - ``false``
* Boolean (true) - ``true``
* Float (negative) - ``-1.0``
* Float (negative infinity) - ``-.inf``
* Float (negative scientific notation) - ``-1e+0``
* Float (negative with underscores) - ``-1.123_456_789``
* Float (positive) - ``1.0``
* Float (positive infinity) - ``.inf``
* Float (positive scientific notation) - ``1e+0``
* Float (positive with underscores) - ``1.123_456_789``
* Inline table - ``{ key1 = "value", key2 "value" }``
* Integer (negative) - ``-1``
* Integer (negative with underscores) - ``-1_000_000``
* Integer (positive) - ``1``
* Integer (positive with underscores) - ``1_000_000``
* Literal string (inline) - ``'text'``
* Literal string (multi-line)::

     '''
     text'''

* Local date - ``2020-01-31``
* Local date-time (with T delimiter) - ``2020-01-31T12:30:00``
* Local date-time (without T delimiter) - ``2020-01-31 12:30:00``
* Local time - ``12:30:00``
* Offset date-time (with T delimiter) - ``2020-01-31T12:30:00+01:30``
* Offset date-time (without T delimiter) - ``2020-01-31 12:30:00+01:30``
* Offset date-time UTC (with T delimiter) - ``2020-01-31T12:30:00Z``
* Offset date-time UTC (without T delimiter) - ``2020-01-31 12:30:00Z``



Other
=====

* Comment (full-line) - ``# comment``
* Comment (inline) - ``key = "value"  # comment``
