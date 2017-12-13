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
drone pilots or other navigation purposes.


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
 - `PylonGPS`_
 - `NTP server`_

into a ready to run RTK base station streaming correction data to a PylonGPS caster.


.. _Raspberry Pi: https://en.wikipedia.org/wiki/Raspberry_Pi#Specifications
.. _ublox M8T: https://www.u-blox.com/en/product/neolea-m8t-series
.. _Yocto Project Poky: https://www.yoctoproject.org/tools-resources/projects/poky
.. _RTKLIB: http://www.rtklib.com/
.. _edition by RTKEXPLORER: https://github.com/rtklibexplorer/RTKLIB
.. _PylonGPS: https://github.com/charlesrwest/pylonGPS
.. _NTP server: http://www.openntpd.org/
