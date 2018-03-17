navdata.net system
==================

Overview
--------

navdata.net combines several open source software components into an easy to use
satellite navigation network that offers improved location precision to the
general public as a community based service.

navdata.net provides ready to run system images for specific low cost hardware
and general configuration information to allow supporters to contribute data by
operating community basestations at low cost.


High level components
---------------------

User
""""

A user of navdata.net uses a local device, equipped with or connected to a
satellite navigation receiver (eg. GPS device). The users intention is to use
data from navdata.net to improve their location precision and reliability.

The navdata.net data is retrieved through a navdata.net client and handed over
to evaluation by RTKlib. RTKlib combines it with the local receivers data to
compute improved precision location information which is provided to client
software (differential GPS).


Broadcaster and catalog
"""""""""""""""""""""""

The users navdata.net client connects to navdata.net broadcasters to identify
and subscribe to the basestation closest to the user (best precision).
The broadcaster sends subscribed navigation data to the client.


Basestation
"""""""""""

A Basestation is directly connected to a -fixed location- satellite navigation
antenna via a receiver that supports delivery of raw signal data. The basestation
evaluates the data and sends it to a navdata.net Broadcaster.
