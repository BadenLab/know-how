---
layout: page
title: Backup System
permalink: /docs/backup_systems/backup-system-information/
---

### BADEN LAB backup system (20190811):

Currently we are storing data in the following way: Users record data on setups computers, which are connected to NAS (12TB space at the moment). An automated system backs up data from NAS to Oceannus:

Setup PC (2p, MEA, etc) user add data manually→ NAS → data enters automatically Oceannus.

The NAS content was divided into two backups:
- one for non-data files (presentations, protocols, forms, etc). This is about 60GB of content and the backup is updated once a week (see below)

- one for data files, actual data from experiments and analysis (ie everything which is in the “data” folder in NAS). This is the rest of the NAS, and today is about 5TB. The backup content is updated everyday (so that every each experiment, new data is backed up, also this should decrease overhead when new data is entering the backup system).

One of the advantages of this system is that it is robust to people entering/leaving the lab (as opposed to create one backup system for each user).

The backup system being used is based on Duplicati, an open source tool for data backup.

Details:
- Duplicati compresses the data and stores it as a collection of files of compressed files. When restoring the data, you need to run the software, so that the data is decompressed and “mounted back” the advantage here is that we can update the NAS size without worrying about Oceannus being the exact same size (I think compression gives us 40% space ie 10GB of raw data are stored as a 6GB backup).

- every time a scheduled backup runs, Duplicati checks which files were altered and only changes those, overwritting them. So if a new analysis is run, and new figures are made with the same name the system should be able to change those files only.

In order to keep track of the backups, a setting file is generated for each backup, so even if working from a different machine, if the user has the setting file and the original backup files, the user can restore the data. In our current setting there are two settings files (data and non-data backups).

On Oceannus the backups are being saved in folders, that only accounts with admin rights can access.
