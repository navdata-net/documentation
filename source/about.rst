About navdata.net
=================

Purpose
-------

Develop a combination of easily accessible and cost efficient hard and software
to allow community based precision geolocation.
Compared to existing projects, we emphasize on creating a public networked
service rather than an individual setup.
We consider the project successful if we aggregate an equivalent or better service
than existing NTRIP providers.
While processing GNSS data, the related time information shall be made available
in the form of public NTP servers.


Users
-----

The project shall be valuable for the public at large serving diverse purposes.
Improving the location precision for mobile phones, vehicles, farmers machinery,
drone pilots or other location and navigation purposes.


Current goal
------------

To create a firmware image combining:

Hardware
''''''''

 - `Raspberry Pi`_ 3B
 - `ublox M8T`_ GPS / GLONASS / Galileo receiver

Software
''''''''

 - `Yocto Project Poky`_
 - `RTKLIB`_ (`edition by RTKEXPLORER`_)
 - `NTP server`_

into a ready to run RTK base station streaming correction data to a PylonGPS caster.


Resources
---------

Documentation
'''''''''''''

Accessible on `Read the Docs`_ and maintained at https://github.com/navdata-net/documentation


Installer
'''''''''

Maintained on github at https://github.com/navdata-net/installer

Used to develop the navdata.net configuration and for installations not using
the navdata.net images for reference hardware. The resources developed in the
installer repository are reused in the yocto layer repository.


Yocto workdir
'''''''''''''

Maintained on github at https://github.com/navdata-net/workdir

Used to simplify working with yocto, develop the navdata.net yocto image configuration
and make it easy to compile and develop the navdata.net image.


Yocto layer
'''''''''''

Maintained on github at https://github.com/navdata-net/meta-navdatanet

Used to develop the recipes for software navdata.net needs to add to yocto.



.. _Raspberry Pi: https://en.wikipedia.org/wiki/Raspberry_Pi#Specifications
.. _ublox M8T: https://www.u-blox.com/en/product/neolea-m8t-series
.. _Yocto Project Poky: https://www.yoctoproject.org/tools-resources/projects/poky
.. _RTKLIB: http://www.rtklib.com/
.. _edition by RTKEXPLORER: https://github.com/rtklibexplorer/RTKLIB
.. _NTP server: http://www.openntpd.org/
.. _Read the Docs: http://readthedocs.io/

