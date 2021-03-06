sphinx-mobi-builder
===================

A Sphinx builder for .mobi (Kindle) files.

This script is originally from GitHub Gist `#5866756`__, by Pedro Kroger.

.. __: https://gist.github.com/kroger/5866756

Requirements
------------

The .mobi builder requires:

* `kindlegen`__ - A command-line Kindle builder from Amazon.com. Just download the application and put it in your
  *PATH*.

.. __: http://www.amazon.com/gp/feature.html?docId=1000765211


Installation
------------

To install the script, download the source and run ``setup.py install``. It will be copied into your Python
``site-packages`` directory.

Using the Builder with Sphinx
-----------------------------

To use the builder with Sphinx, add ``sphinx.builders.mobi`` to the *extensions* list in ``conf.py``::

    extensions = [
       ... other extensions here ...
       sphinx.builders.mobi
       ]

The following configuration values can be used in ``conf.py``. At a minimum, you must set the *mobi_theme* option:

:mobi_add_visible_links: Whether or not to write out the full text of a hyperlink next to the link itself. If the
                         document will be read on paper (or printed), it is a good idea to set this to ``True``.

                         Default: ``True``

:mobi_author: The author of the book.

              Default: ``'unknown'``

:mobi_basename: The basename of the output file (the part of the filename that precedes ``.mobi``)

                Default: The project name, with spaces removed.

:mobi_copyright: The copyright holder of the book.

                 Default: The value of **copyright** in ``conf.py``

:mobi_cover: The cover image for the book. This should be in ``.jpg`` format.

             Default: No cover image is used.

:mobi_exclude_files: TBD

                     Default: no files are excluded.

:mobi_identifier: TBD

                  Default: ``'unknown'``

:mobi_language: TBD

                Default: The value of *language* in ``conf.py``, or ``'en'`` if *language* is not set.

:mobi_post_files: TBD

                  Default: no post files are used.

:mobi_pre_files: TBD

                 Default: no pre files are used.

:mobi_publisher: The publisher name for the book.

                 Default: ``'unknown'``

:mobi_scheme: TBD

              Default: ``'unknown'``

:mobi_theme: *Required*. The mobi theme-file to use. If you don't have a theme of your own, I suggest using the ``epub``
             theme::

              mobi_theme = 'epub'

:mobi_title: TBD

             Default: The value of *html_title* in ``conf.py``.

:mobi_tocdepth: TBD.

                Default: ``3``.

:mobi_tocdup: TBD

              Default: ``True``

:mobi_uid: TBD

           Default: ``'unknown'``


License
-------

As per the original script, this code is made available using the `BSD Open Source license`__.

.. __: http://opensource.org/licenses/BSD-3-Clause

