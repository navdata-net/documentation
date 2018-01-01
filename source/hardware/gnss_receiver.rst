Configuring and using GNSS receivers for navadata.net
=====================================================

u-blox
------

By using rtklibexplorers edition of RTKLIB we get enhanced support for`u-blox receivers`_.
On rtklibexplorers website we can find an article about`Configuring the GPS receiver`_ for use with RTKLIB.

In summary::

  set UBX:CFG:PRT:Baudrate to 115200
  disable all NMEA messages
  save configuration in UBX:CFG:CFG:Save configuration



.. u-blox receivers: https://www.u-blox.com/en/position-time
.. Configuring the GPS receiver: https://rtklibexplorer.wordpress.com/2016/01/30/configuring-the-gps-receiver-ublox-eval-software/
