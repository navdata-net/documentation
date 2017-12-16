OS setup for navdata.net development
====================================

As the underlying OS any recent linux distribution with support for docker should do.
Expect up to 50GB storage space to be utilized in folder /workdir.


Ubuntu Desktop
--------------

Below commands are execute by user root.
Based on default Desktop installation, add required packages::

  apt install docker

We will run all development, compilation and image creation as user yocto::

  adduser yocto

Development files will be on directory /workdir, this makes paths aligned with the yocto build container::

  mkdir /workdir
  chown yocto:yocto /workdir
