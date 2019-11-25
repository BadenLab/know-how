---
layout: page
title: NAS Ocennus connection
#parent: prototyping-tools
permalink: /docs/backup_systems/oceannus_connection
---


DANIO (also known (erroneously) as Oceannus (Oceannus is the computing cluster. Danio is the data server)).

To connect to it using windows:
open windows explorer → my computer → map a network drive (see that this is different from map a network location).

If your computer does not have an IT image installed, type the following address:

//alt-danio.uscs.susx.ac.uk/baden

check “log with different credentials” and “connect at startup”

then username: ad_us\USERNAME (here this should be your Uni. Sussex username – the short form of your email before “@”)
password is your email password.

If your computer has an IT image the same as above applies, but using the following address:

//danio.uscs.susx.ac.uk/baden


A note on permissions and file visibility

For security reasons, accounts are split into two types (roughly speaking), regular and admin accounts.
Regular accounts (phds, post docs, technicians, masters, rotation, etc) only have access to the folder “shared” and their own user folder. Whatever they create on the shared folder can be seen/modified by everyone. What is in their own folders can only be seen by the user who created it and by admin accounts

Admin accounts can see and change everything in all folders, but what they create on folders that belong to regular users can only be seen by the admin! (from IT implementation point of view there is no easy way around this).

The above fact bumps into how we’ve been recording data (up to July 2019) on setups 1 and 2:
There we logged in an Admin account permanently which prevents each user having to log in to Danio every time, but creates the problem that all files created/stored there cannot be seen by the user when they log in on their office machines. This is going to be phased out until the end of July 2019, so that users use a new storing pipeline: Setup computers → NAS → office/analysis computer. (all backup to Danio will be done automatically on a daily basis(non overwrite), and weekly basis (overwritting)).
