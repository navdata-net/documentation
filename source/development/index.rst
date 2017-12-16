Developing with navdata.net
===========================

Poky
-----

We base our image on the Poky distribution developed by the Yocto project.
To avoid issues between the developers working environment and the requirements
of cross compiling, we make use of Yoctos docker based build tool `crops/poky`_.


source code location
--------------------

This docker image uses a directory of its host computer as the storage for its build process.
This folder is accessed at '/workdir' inside the build container.
For ease of use and validity of the same paths from host and container, we
store our code at that same location at '/workdir'.


Preparing your development environment
======================================

.. toctree::
   :maxdepth: 2

   os_setup
   development_setup



.. _crops/poky: https://github.com/crops/poky-container
