===========================
Rule Based Bangla Stemmer
===========================

**contents**
    - `Installation`_
    - `Usage`_
    - `Rules Documentation (Only for Development)`_

Installation
-------------

.. code-block:: bash

    $ pip install py_bangla_stemmer

`Usage`_
----------

.. code-block:: python

    >>> from py_bangla_stemmer import BanglaStemmer
    >>> 
    >>> stemmer = BanglaStemmer()
    >>> stemmer.stem('জনপ্রিয়তা')  # 'জনপ্রি'
    >>> stemmer.stem(' সেটাই')    # 'সে'

`Rules Documentation (Only for Development)`_
----------------------------------------------

Following documentations are for the further development of the stemmer. There is a file in ``py_bangla_stemmer/resources`` folder named ``common.rules``. Bellow are the information required to know to change the rules.

.. code-block:: math

    X + n :

When X appears at the end of a word and word length is at least n, remove it

.. code-block:: math

    Y -> Z + n :

When Y appears at the end of a word and word length is at least n, replace it with Z

.. code-block:: math

    Y.Z -> A.B + n :`

When Y, followed by some character a, followed by Z appears at the end of a word 
and word length is at least n, replace it with AaB.