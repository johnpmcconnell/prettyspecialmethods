==================================
sphinxcontrib-prettyspecialmethods
==================================

|badge-pypi| |badge-travis|

.. |badge-pypi| image:: https://badgen.net/pypi/v/sphinxcontrib-prettyspecialmethods
    :target: https://pypi.org/project/sphinxcontrib-prettyspecialmethods

.. |badge-travis| image:: https://travis-ci.org/sphinx-contrib/prettyspecialmethods.svg?branch=master
    :target: https://travis-ci.org/sphinx-contrib/prettyspecialmethods

Shows special methods as the python syntax that invokes them

Overview
--------

This module renders docs like

.. code-block:: rst

    .. method:: __add__(other)
        Docstring


as

self + other
    Docstring

It also works when using autodoc on a class that implements these methods.

After installing this module, add the following to your `conf.py` to enable it

.. code-block:: python

    extensions = [
        ...  # your other extensions
        'sphinxcontrib.prettyspecialmethods',
    ]

Changing "self"
---------------

The directive `renameself` is included in the docstring, its argument will be used
in place of "self" in the output:

.. code-block:: rst

    .. method:: __add__(other)
        Docstring
        .. renameself:: obj

renders to

obj + other
    Docstring


Links
-----

- Source: https://github.com/sphinx-contrib/prettyspecialmethods
- Bugs: https://github.com/sphinx-contrib/prettyspecialmethods/issues
