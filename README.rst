PRAW: The Python Reddit API Wrapper
===================================

|travis-ci| |coveralls|

.. |travis-ci| image:: https://travis-ci.org/michael-lazar/praw3.svg?branch=master
  :target: https://travis-ci.org/michael-lazar/praw3
.. |coveralls| image:: https://coveralls.io/repos/github/michael-lazar/praw3/badge.svg?branch=master
  :target: (https://coveralls.io/github/michael-lazar/praw3?branch=master

This repository contains a fork of the `PRAW <https://github.com/praw-dev/praw>`_ library, with intent of continuing support for the (deprecated) version 3 branch. If you are looking for information about the official PRAW library, please visit their `documentation <http://praw.readthedocs.io/en/latest/>`_. This fork was created to support the `RTV <https://github.com/michael-lazar/rtv>`_ reddit command line application. RTV relies heavily on the structure of the legacy PRAW API and would require a major overhaul to support the new version. The maintainer of PRAW has expressed that he does not intend to provide any support for older versions going forward. It is important to note that the Reddit API itself has not released any breaking changes. Both versions of PRAW can interact with the core Reddit functions, although the newer version contains support for some of the more cutting-edge features such as live threads.

The goal of this repository is to provide security updates and bug fixes to the stable PRAW 3 branch. This is not intended to compete against the official PRAW library in any way. Anyone who is capable of doing so to should be using the latest official version of PRAW.

Changes
-------

This repository was forked on March 6, 2017 from PRAW v3.6.1. Since then, the following changes have been made:

- Disabled and removed the ``update_checker`` project dependency
- Switched from absolute imports to relative imports, in order to make it possible to bundle the *praw/* directory inside of another project
- Upped the ``requests`` version requirement to v2.4.0 (`link <https://github.com/praw-dev/praw/issues/737>`_)
- Fix for new user profiles ``TypeError: subreddit_name must be a non-empty string`` (`link <https://github.com/michael-lazar/rtv/issues/375>`_)
- Patch to remove the ``permalink`` field from the Comment JSON object (`link <https://github.com/michael-lazar/praw3/pull/3>`_)
- Fixed several Multireddit functions when using OAuth (`link <https://github.com/michael-lazar/praw3/pull/4>`_)

Installation
------------

You can use pip to install directly from the repository:

``pip install git+git://github.com/michael-lazar/praw3@master``

Documentation
-------------

For now, the PRAW v3 documentation is still being hosted at http://praw.readthedocs.io/en/v3.6.1/

License
-------

All of the code contained here is licensed by
`the GNU GPLv3 <https://github.com/praw-dev/praw/blob/master/COPYING>`_.
