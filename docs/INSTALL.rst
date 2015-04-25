c2.splitter.janome Installation
================================

* Create a file called ``c2.splitter.janome-configure.zcml`` in the
   ``/path/to/instance/etc/package-includes`` directory.  The file
   should only contain this::

       <include package="c2.splitter.janome" />

.. _pythonproducts: http://plone.org/products/pythonproducts

Alternatively, if you are using zc.buildout and the plone.recipe.zope2instance
recipe to manage your project, you can do this:

* Add ``c2.splitter.janome`` to the list of eggs to install, e.g.::

   [buildout]
   ...
   eggs =
       ...
       c2.splitter.janome

* Tell the plone.recipe.zope2instance recipe to install a ZCML slug::

   [instance]
   recipe = plone.recipe.zope2instance
   ...
   zcml =
        c2.splitter.janome

* Re-run buildout, e.g. with::

   $ ./bin/buildout

You can skip the ZCML slug if you are going to explicitly include the package
from another package's configure.zcml file.
