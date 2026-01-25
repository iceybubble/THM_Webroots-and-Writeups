Room Name: Dumping Router Firmware
Room Link: https://tryhackme.com/room/rfirmware

```
What does the first clear text line say when running strings on the file?
Linksys WRT1900ACS Router
```

```
Also, using strings, what operating system is the device running?
Linux
```

```
What option within Binwalk will allow us to extract files from the firmware image?
-e
```

```
Now that we know how to extract the contents of the firmware image, what was the first item extracted?
uImage header
```

```
What was the creation date?
2020-04-22 11:07:26
```

```
The Cyclical Redundancy Check is used similarly to file hashing to ensure that the file contents were not corrupted and/or modified in transit.



What is the CRC of the image?
0xABEBC439
```

```
What is the image size?
4229755 bytes
```

```
What architecture does the device run?
ARM
```

```
Researching the results to question 10, is that true?
Yes
```

```
Running strings on 6870, we notice a large chunk of clear text. We can actually rerun binwalk on this file to receive even more files to investigate. Interestingly enough, a copy of the Linux kernel is included. What version is it for?
3.10.39
```

```
Where does linuxrc link to?
/bin/busybox
```

```
What parent folder do mnt, opt, and var link to?
/tmp/
```

```
What folder would store the router's HTTP server?
/www/
```

```
The first of the folders that aren't empty is /bin/; where do a majority of the files link to?

Why is that? Well, busybox is more or less a tool suite of common executable commands within the Unix environment.
busybox
```

```
Interestingly, what database would be running within the bin folder if the router was online?
sqlite3
```

```
The following notable folder of interest is /etc/. This folder contains many configuration files for the router, such as Access Point power levels regulated by certain countries. One you might recognize is the FCC (Federal Communications Commission).

We can even see the build date of the device. What is the build date? 
2020-04-22 11:44
```

```
There are even files related to the SSH server on the device. What SSH server does the machine run?
dropbear
```

```
We can even see the file for the media server, which company developed it?

This company use to own Linksys at one point in time, which is likely why it is still being used.
Cisco
```

```
Which file within /etc/ contains a list of standard Network services and their associated port numbers?
services
```

```
Which file contains the default system settings?
system_defaults
```

```
What is the specific firmware version within the /etc/ folder?
2.0.3.201002
```

```
What three networks have a folder within /JNAP/modules?
guest_lan, lan, wan
```

