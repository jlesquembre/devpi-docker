Devpi for Docker
================

Script to create and manage multiple docker_ containers serving devpi_ through
nginx with SSL support.


Quickstart
----------

Run the command `devpi-docker start`, first time it will take some time to
download the docker images. Once the command finish, try to open
https://localhost:3142/ to see if is working. You can find the ssl certificates
used by nginx at `~/devpi_certs`

Run `devpi-docker local_install` to avoid the ssl warning on chromium/chrome
and to generate a pip.conf file which will use devpi by default.

If your linux distro is using systemd, you can install `this service
<https://github.com/jlesquembre/consul-registrator>`_ to use the url
https://devpi:3142/ instead of localhost

If you have any problem, write me or open a `new issue on github
<https://github.com/jlesquembre/devpi-docker/issues>`_.
I'm more than happy about questions and discussions about the project.


Command reference
-----------------

- devpi-docker start
    Setup and run devpi using docker containers

- devpi-docker stop
    Stop the docker containers

- devpi-docker update
    Update devpi to the latest version

- devpi-docker rm
    Stop and remove the docker containers

    .. note:: You will lose all your devpi configuration and packages. Do a
              backup before!

- devpi-docker gen_cert
    Generate a new ssl certificate for nginx

- devpi-docker local_install
    Install the ssl certificate in chromium/chrome database and generate a
    basic pip.conf file



Devpi client quick start
------------------------

#. Create a user

    .. code-block:: bash

        devpi user -c $USER

#. Login as user
    .. code-block:: bash

        devpi login $USER

#. Create index
    .. code-block:: bash

        devpi index -c dev

#. Set new index as default
    .. code-block:: bash

        devpi use dev




.. _Docker: https://www.docker.com/

.. _Devpi: http://doc.devpi.net/
