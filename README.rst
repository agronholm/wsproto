Pure Python, pure state-machine WebSocket implementation
========================================================

.. image:: https://travis-ci.org/python-hyper/wsproto.svg?branch=master
    :target: https://travis-ci.org/python-hyper/wsproto
    :alt: Build status
.. image:: https://readthedocs.org/projects/wsproto/badge/?version=latest
    :target: http://wsproto.readthedocs.io/en/latest/?badge=latest
    :alt: Documentation Status
.. image:: https://codecov.io/gh/python-hyper/wsproto/branch/master/graph/badge.svg
    :target: https://codecov.io/gh/python-hyper/wsproto
    :alt: Code coverage

This needs a pile of cleaning up.

It passes the autobahn test suite completely and strictly in both client and
server modes and using permessage-deflate.

If `wsaccel <https://pypi.python.org/pypi/wsaccel>`_ is installed
(optional), then it will be used to speed things up.

If you want to run the compliance tests, go into the compliance directory and
then to test client mode, in one shell run the Autobahn test server:

.. code-block:: console

    $ wstest -m fuzzingserver -s ws-fuzzingserver.json

And in another shell run the test client:

.. code-block:: console

    $ python test_client.py

And to test server mode, run the test server:

.. code-block:: console

    $ python test_server.py

And in another shell run the Autobahn test client:

.. code-block:: console

    $ wstest -m fuzzingclient -s ws-fuzzingclient.json

This was written using Python 3.5. Python 3.4, 3.5 and 3.6 are being
actively tested. PyPy3 will be tested once TravisCI gets it working
again. Python 2.x is not supported.
