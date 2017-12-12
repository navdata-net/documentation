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

 - Raspberry Pi 3B
 - U-Blox M8T GPS / GLONASS / Galileo receiver

Software
''''''''

 - Yocto Project
 - RTKLIB
 - PylonGPS
 - NTP server

into a ready to run RTK base station streaming correction data to a PylonGPS caster.
