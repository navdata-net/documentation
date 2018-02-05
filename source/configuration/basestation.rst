Basestation
===========

Overview
--------

The reference basestation is based on a Raspberry Pi 3 and a u-blox M8T receiver.
The basestation is configured as an NTP server, RTKlib rtkrcv for location and a
combination of RTKlib str2str and PylonGPS transceiver for data streaming.


Hardware
--------

The Raspberry Pi 3 is connected to the M8T receiver via USB for data and GPIO
pin 4 for the 1 Hz PPS signal.


NTP server
----------

The NTP server is configured as a client to 4 pool.ntp.org servers of the country
of the basestations public IP. The M8T PPS signal is provided via the kernel based
PPS driver and used by NTPD for precision timekeeping. NTPD is configured as an
NTP server for public reuse.


rtkrcv
------

RTKlibs rtkrcv is the direct user of the M8T receiver via its USB based serial
tty. rtkrcv continuously computes the basestations location from the satellite
data. It is configured to provide several network ports on the local IP::

  :3130 - telnet console (-p option)
  :3134 - monitoring port (-m option)


str2str
-------

str2str is used to shield rtkrcv from user acces and convert the u-blox receiver
data format into standardised RTCMv3 format. ::

  :3131 - passthrough receiver data / raw (u-blox format)
  :3132 - passthrough receiver data / RTCM3
  :3133 - TCM3 antenna location message 1006
  :3141 - integrated RTCM 3 location and raw data


transceiver
-----------

It is intended to run multiple transceiver instances for broadcasting different
data. Each instance has a distinct name.


transceiver naming convention
"""""""""""""""""""""""""""""

The transceiver name is made up of 5 components of fixed length, the digits
representing the field number and the number of digits the field length::

  1_22_33333333333333


field 1
'''''''

1 character indicating the basestation designation as::

  D : development (may intentionally send wrong data)
  M : mobile / location not static
  T : test (unreliable)
  C : community (essential reliabililty and quality)
  U : university / education (high reliability and quality)
  B : business (high reliability and quality)
  G : government (official, professional basestation)


field 2
'''''''

2 characcters indicating data format::

  R3 : RTCM v3 (RTCM_V3)
  UB : u-blox (RAW)


field 3
'''''''

14 characters custom personalized station name string


example
'''''''

D_UB_MyBase



standard transceiver instances
""""""""""""""""""""""""""""""

RAW
'''

transceiver connects to the local rtkrcv process on logging port :3141 and
forwards the raw receiver module data to pylon.navdata.net
