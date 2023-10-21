=======================
Midnight Commander ulzx
=======================

Midnight Commander extfs plugin for handling lzx Amiga archives.

Description
===========

ULzx is an extfs plugin which can be used to browse and extract lzx archives,
which are known almost exclusively from Amiga.

Due to limitations of
`unlzx <ftp://us.aminet.net/pub/aminet/misc/unix/unlzx.c.gz.readme>`_ tools,
only reading is supported. Also be aware, that
`unlzx <ftp://us.aminet.net/pub/aminet/misc/unix/unlzx.c.gz.readme>`_ cannot
extract files individually, so copying entire archive content is not
recommended, since on every single file a full archive extract would be
done, which in the end would have impact on performance.

Requirements
------------

ULzx requires
`unlzx <ftp://us.aminet.net/pub/aminet/misc/unix/unlzx.c.gz.readme>`_ tool.

Installation
------------

* install `extfslib`_
* copy ``ulzx`` to ``~/.local/share/mc/extfs.d/``
* add or change entry for files handle in ``~/.config/mc/mc.ext``:

.. code:: ini

   [lzx]
   Regex=\.lzx$
   RegexIgnoreCase=true
   Open=%cd %p/ulzx://
   View=%view{ascii} unlzx -v %f

License
=======

This software is licensed under 3-clause BSD license. See LICENSE file for
details.


.. _extfslib: https://github.com/gryf/mc_extfslib
