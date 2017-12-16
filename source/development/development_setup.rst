Development environment setup
=============================

Clone / update workdir repository
---------------------------------

Switch to yocto user as prepared in `OS setup`_, clone your copy::

  cd /
  git clone https://github.com/navdata-net/workdir.git

Inside workdir, the navdata.net setup adds several additional git repositories.
When you are working with navdata.net, prefer to execute your git commands from
the /workdir or meta-navdatanet folder respectively to avoid any ambiguity
reagrding which repository your action is meant to execute on.

Clone the poky and poky layer repositories using navdata.net script::

  cd /workdir
  ./fetchrepos.sh

You can run the fetchrepos.sh script any time later to update / pull your copy
of the repositories.


Compile navdata.net basestation image
-------------------------------------

To compile the navdata.net basestation image, you need to start the yocto build
container and initiate bitbake inside it::

  cd /workdir
  ./rundocker.sh
  cd /workdir/dev
  ./bake.sh

.. OS setup: os_setup
