Developing with navdata.net
===========================

Poky
-----

We base our image on the Poky distribution developed by the Yocto project.
To avoid issues between the developers working environment and the requirements
of cross compiling, we make use of Yoctos docker based build tool "CROPS".


source code location
--------------------

This docker image uses a directory of its host computer as the storage for its build process.
This folder is accessed at '/workdir' inside the build container.
For ease of use and validity of the same paths from host and container, we
store our code at that same location at '/workdir'.

To clone your copy::

  cd /
  git clone https://github.com/navdata-net/workdir.git

Inside workdir, the navdata.net setup adds several additional git repositories.
When you are working with navdata.net, prefer to execut your git commands from
the /workdir folder to avoid any ambiguity reagrding which repository your action
is meant to execute on.

navdata.net workdir provides you with:


folder dev & prod
'''''''''''''''''

For simplicity in the initial phases, we keep two copies in separate folders
instead of using git branches. This simplifies working with the build directory
of bitbake inside those trees.


fetchrepos.sh
''''''''''''''

Retrieve and/or update all external source code, namely poky and additional poky
layers into the /workdir folder::

  cd /workdir
  ./fetchrepos.sh


rundocker.sh
''''''''''''

Start Yocto provided build environment::

  cd /workdir
  ./rundocker.sh


bake.sh
'''''''

Execute a build of the navdata.net base station image from within docker console
started above::

  cd /workdir/dev
  ./bake.sh

Expect up to 50GB storage space to be utilized.
