============
Contributing
============

Contributions are welcome, and they are greatly appreciated! Every little bit
helps, and credit will always be given.

You can contribute in many ways:

Types of Contributions
----------------------

Report Bugs
~~~~~~~~~~~

Report bugs using the `issue tracker <https://github.com/matthiaskoenig/libsbgn-python/issues>`__

If you are reporting a bug, please include:

* Your operating system name and version.
* Your python and libsbgn-python version.
* Any details about your local setup that might be helpful in troubleshooting.
* Detailed steps to reproduce the bug.

Fix Bugs
~~~~~~~~

Look through the GitHub `issues <https://github.com/matthiaskoenig/libsbgn-python/issues>`__
for bugs. Anything tagged with "bug" and "help wanted" is open to whoever wants
to implement it.

Implement Features
~~~~~~~~~~~~~~~~~~

Look through the GitHub `issues <https://github.com/matthiaskoenig/libsbgn-python/issues>`__
for features. Anything tagged with "enhancement" and "help wanted" is open to whoever wants to
implement it.

Write Documentation
~~~~~~~~~~~~~~~~~~~

libsbgn-python could always use more documentation, whether as part of the official
libsbgn-python docs, in docstrings, or even on the web in blog posts, articles, and
such - all contributions are welcome!

Submit Feedback
~~~~~~~~~~~~~~~

The best way to send feedback is to file an
`issue <https://github.com/matthiaskoenig/libsbgn-python/issues>`__.

If you are proposing a feature:

* Explain in detail how it would work.
* Keep the scope as narrow as possible, to make it easier to implement.
* Remember that this is a volunteer-driven project, and that contributions
  are welcome :)

If you like libsbgn-python please remember to 'star' our github page (click on the star
at top right corner), that way we also have an idea of who is using libsbgn-python!

Get Started!
------------

Want to contribute a new feature or improvement? Consider starting by raising an
issue and assign it to yourself to describe what you want to achieve. This way,
we reduce the risk of duplicated efforts and you may also get suggestions on how
to best proceed, e.g. there may be half-finished work in some branch that you
could start with.

Here's how to set up `libsbgn-python` for local development to contribute smaller
features or changes that you can implement yourself.

1. Fork the `libsbgn-python` repository on GitHub.
2. Clone your fork locally::

    $ git clone git@github.com:<your Github name>/libsbgn-python.git

3. If virtualenvwrapper is not installed,
   `follow the directions <https://virtualenvwrapper.readthedocs.io/en/latest/>`__
   to install virtualenvwrapper.

4. Install your local copy of libsbgn-python into a virtualenv with virtualenvwrapper::

    $ cd libsbgn-python
    $ mkvirtualenv libsbgn-python

   Use the ``--python`` option to select a specific version of Python for the
   virtualenv.

5. Install the required packages for development in the virtualenv using pip install::

    (libsbgn-python)$ pip install --upgrade pip setuptools wheel
    (libsbgn-python)$ pip install -r requirements.txt

6. Check out the branch that you want to contribute to. Most likely that will be
   ``develop``::

    (libsbgn-python)$ git checkout develop

7. Create a branch for local development based on the previously checked out
   branch (see below for details on the branching model)::

    (libsbgn-python)$ git checkout -b name-of-your-bugfix-or-feature

   Now you can make your changes locally.

8. Setup libsbgn-python for development::

    (libsbgn-python)$ pip install -e .

9. When you are done making changes, check that your changes pass pep8
   and the tests with tox for your local Python version::

     (libsbgn-python)$ tox -e pep8

    and one of the py2 and py3 tests via::

     (libsbgn-python)$ tox -e py35
     (libsbgn-python)$ tox -e py36
     (libsbgn-python)$ tox -e py37
     (libsbgn-python)$ tox -e py38

10. Commit your changes and push your branch to GitHub::

    (libsbgn-python)$ git add .
    (libsbgn-python)$ git commit -m "Your detailed description of your changes."
    (libsbgn-python)$ git push origin name-of-your-bugfix-or-feature

11. Submit a pull request through the GitHub website. Once you submit a pull
    request your changes will be tested automatically against multiple python
    versions and operating systems. Further errors might appear during those
    tests.

For larger features that you want to work on collaboratively with other libsbgn-python team members,
you may consider to first request to join the libsbgn-python developers team to get write access to the
repository so that you can create a branch in the main repository
(or simply ask the maintainer to create a branch for you).
Once you have a new branch you can push your changes directly to the main
repository and when finished, submit a pull request from that branch to ``develop``.

Pull Request Guidelines
-----------------------

Before you submit a pull request, check that it meets these guidelines:

1. The pull request should include tests in the ``libsbgn-python/test``
   directory. Except in rare circumstances, code coverage must
   not decrease (as reported by codecov which runs automatically when
   you submit your pull request)
2. If the pull request adds functionality, the docs should be
   updated. Put your new functionality into a function with a
   docstring and consider creating a notebook that demonstrates the
   usage in ``documentation_builder`` (documentation is written as
   jupyter notebooks in the ``documentation_builder`` directory, which
   are then converted to rst by the ``autodoc.sh`` script.)
3. The pull request should work for Python 2.7, 3.5 and 3.6.
4. Assign a reviewer to your pull request. If in doubt, assign matthiaskoenig.
   Your pull request must be approved by at least one
   reviewer before it can be merged.

Unit tests and benchmarks
-------------------------

libsbgn-python uses `pytest <http://docs.pytest.org/en/latest/>`_ for its
unit-tests and new features should in general always come with new
tests that make sure that the code runs as intended::

    (libsbgn-python)$ pytest


Branching model
---------------

``develop``
    Is the branch all pull-requests should be based on.
``master``
    Is only touched by maintainers and is the branch with only tested, reviewed
    code that is released or ready for the next release.
``{fix, bugfix, doc, feature}/descriptive-name``
    Is the recommended naming scheme for smaller improvements, bugfixes,
    documentation improvement and new features respectively.

Please use concise descriptive commit messages and consider using
``git pull --rebase`` when you update your own fork to avoid merge commits.

1. Tests are in the ``libsbgn-python/test`` directory. They are automatically run
   through continuous integration services on both python 2 and python 3
   when pull requests are made.
2. Please write tests for new functions. Writing documentation as well
   would also be very helpful.
3. Ensure code will work with both python 2 and python 3. For example,
   instead of ``my_dict.iteritems()`` use ``six.iteritems(my_dict)``

Thank you very much for contributing to libsbgn-python!
