Installation
============

.. include:: ../links.rst

Requirements
------------

* NodeJS_ - The main environment
* npm_ - Node Package Manager
* MongoDB_ - NoSQL Database


Requirements Install
--------------------

* For MongoDB_, please refer to `Install MongoDB`_ first. Most packages for Linux distros
  are a little bit old (in and older on old LTS versions), so we strongly suggest you to use
  the last stable version.

On Debian/Ubuntu
````````````````

.. code:: bash

    aptitude install nodejs npm

If you prefer, you can install MongoDB_ from the actual repository.

.. code:: bash

    aptitude install mongodb

On RedHat/CentOS
````````````````

.. code:: bash

    yum install nodejs npm

If you prefer, you can install MongoDB_ from the actual repository.

.. code:: bash

    yum install mongodb


graoJS Global Install
---------------------

Use:

.. code:: bash

    npm install -g graojs

or with ``sudo`` if your environment requires (e.g. Ubuntu way):

.. code:: bash

    sudo npm install -g graojs

And you're ready to play around with graoJS_ - see more on :doc:`quick-start`.
