===========================================================
A virtualenv-ized bootstrap script for Buildout's bootstrap
===========================================================

Or a meta-bootstrap...


What is this?
=============

This is a script which automates the creation of a `virtualenv`_ from which
`Buildout`_ is going to be installed and initialized.


Why would I need this?
======================

If you want a completely repeatable `Buildout`_ environment, you should probably
rely on using `virtualenv`_ first, to have a empty, basic, Python environment,
isolated from the rest of your system, from which you can run `Buildout`_'s own
bootstrap and then finally `Buildout`_ itself.

As it can be a bit daunting to set up everything each times, this script simply
tries to automate the whole process.


How do I use it?
================
Simply download it, and run::

    python bootstrap-venv.py

It will creates the `virtualenv`_ (in `parts/venv/`), download a `Buildout`_'s
`bootstrap`_ file, and execute it, using the Python installed in the
`virtualenv`_ created above. You can also specify another directory to bootstrap
the whole thing in::

    python bootstrap-venv.py some-directory

It does the same, only in the `some-directory` directory.

As an additional feature, if `virtualenv`_ itself is not available, it will also
**bootstrap** `virtualenv`_ itself, before doing anything else. So basically, as
soon as you only have a bare Python installation, you can use this script to
have a customizable, isolated, working environment.


Why do I need to use this?
==========================

Really, you just need a plain `Python 2.x Python 3.x
<https://www.python.org/downloads/>`_. It's supposed to
download the rest automatically.


It's just awesome, can I really rely on this?
=============================================

It started as a proof-of-concept, so it *works for me* ® but your mileage may
vary. Feel free to open issue or better yet, send me patches or pull requests!

The code is available under the Simplified BSD License. See the :file:`LICENSE`
file for more information.

.. _virtualenv: http://virtualenv.readthedocs.org/
.. _buildout: http://www.buildout.org
.. _bootstrap: https://bootstrap.pypa.io/bootstrap-buildout.py
