Navdata.net development environment components
==============================================

navdata.net workdir provides you with the following content.


Folder structure
----------------

folder dev & prod
'''''''''''''''''

For simplicity in the initial phases, we keep two copies of poky in separate
folders instead of using git branches. This simplifies working with the build
directory of bitbake inside those trees.
Inside each of these copies we add additional meta layer repositories at the
dev and prod directory level (poky root).
Therefore the navdata.net tools are in the `workdir repository`_ and the
`meta-navdatanet repository`_ is located inside the poky root folders /dev and
/prod.


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

.. workdir repository: https://github.com/navdata-net/workdir
.. meta-navdatanet repository: https://github.com/navdata-net/meta-navdatanet
