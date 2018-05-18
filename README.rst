.. image:: https://travis-ci.org/awslabs/aws-detailed-billing-parser.svg?branch=master
    :target: https://travis-ci.org/awslabs/aws-detailed-billing-parser


AWS DBR parser
==============

    Author: Rafael M. Koike

    AWS ProServe

This script was created to support automatic parsing of Detailed Billing
Records (DBR) to JSON format and send these documents directly to
ElasticSearch or save it in a JSON file. It’s based on `AWS boto3`_,
`Elasticsearch`_ Python API and `click`_ CLI creation kit.

Installation Instructions
------------------------

This project isn’t on PyPI yet. For installation you will need to clone
this repository and use ``setup.py`` script to install it. For
requirements see the ``requirements/base.txt`` file. Clone this
repository and install using plain python and the ``setup.py`` script.
For example:

-  This option just install the dbrparser but maybe you can use the
   job.sh from the repository to schedule the process in your cronjob

::

    $ pip install git+https://github.com/awslabs/aws-detailed-billing-parser.git

-  This option clone the repository from git to your instance and
   install

.. code:: bash

    $ git clone https://github.com/awslabs/aws-detailed-billing-parser.git
    $ cd aws-detailed-billing-parser
    $ python setup.py install

Executing
---------

Once installed run ``dbrparser`` CLI with ``--help`` option:

.. code:: bash

    $ dbrparser --help

Running Tests
-------------

Tests still need to be written. But we have already introduced
`py.test`_, `tox`_ for test run automation and `flake8`_ to check
quality and style of the code. There are nice stubs for testing the CLI
command line. All you have to do is install **tox** and issue ``tox`` in
the command line.

TODO (Features to incorporate in the dbrparser)
-----------------------------------------------

-  Refactoring of analytics code.

Changes
-------
Version 0.5.4 - 2017-08-29
~~~~~~~~~~~~~~~~~~~~~~~~~~

- Bugfix: RI and Spot coverage was returning incorrect results with Python 2.7 due to the default integer result from /

