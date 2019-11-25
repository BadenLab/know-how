---
layout: page
title: NAS
#parent: prototyping-tools
permalink: /docs/backup_systems/nas
---


# Baden Lab backup / file storage backup_system

## NOTE: Other than this automated storage system, all lab members are responsible for keeping backups of their own data! Preference is given for a complete copy in an external drive (extra points if this is kept outside the lab!)

### Currently (20191126) the lab uses a NAS system from Synology.

Computers attached to setups and other measurement devices are connected to this
system. So users have the task of copying their data after the end of an Experiment
to the appropriate folder in the NAS -> normally a subfolder inside the "data folder"
in the file tree.
  - Copying your data there ensures that the automatic backing up system saves your
  data to Oceannus (a data server maintained by Sussex IT department).

  - If you copy your data elsewhere within NAS, this won't be automatically backed up!!!

- New users should contact [Andre](https://andre.github.io) for a new login and password (which will be different from
   your Sussex credentials).

- accessing the NAS from the office should be done connecting to badenstation.biochem.susx.ac.uk/root
  - this can be done by typing the above address on your web browser
  - or more conveniently by mapping a network drive, if you are using a Windows computer.

  ---

###  More detailed info about NAS installation:

Following IT instructions the system has to be setup as DHCP.

In case a new systems needs to be installed (a complete new NAS and not just HD updates), here are the necessary steps to get it up and running:

- Find out the MAC address of the ethernet port on the NAS you will use to connect it to the network (the NAS has more then one ethernet port, and each has a different MAC address, so make sure you always connect the selected port).

- contact IT and tell them the device has been changed, sending them the MAC address. This will allow them to set a fixed IP to the NAS and all users will be able to connect to it:

 1 –(IT’s PREFERRED METHOD – stable even if NAS IP changes) using the name registered on the network (DNS name) badenstation.biochem.susx.ac.uk

or

 2 – using FTP protocol and setting the IP address given by IT

Windows users:
open windows explorer → my computer → connect to a network location.
Then type on the location address: ftp://USERNAME@IPADDRESS/Root (considering Root is the base folder setup on NAS).

Check “connect at log in” and “use different credentials”. Type your NAS password (not necessarily the same as sussex pasword).
