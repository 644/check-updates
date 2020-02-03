# Description
This script is a bash replacement for aarchup - an update checking daemon with notifications. It will write the database to RAM to save on HDD/SSD write cycles. The idea is because it resyncs the database so frequently, writing directly to the disk constantly could easily shorten its lifetime.

It doesn't require root priveleges, can replace notifications, and even offers a way to upgrade the system by clicking a button on the notification itself.

# Installation
Just download and add the script to a normal user's cronjob (cronie), and configure the settings in the script (mainly the TERMINAL=xfce4-terminal) as everything else is *probably* the defaults.

An example cronjob would look like
```
PATH= # do echo "$PATH" in your terminal and add it here
*/5 * * * * /home/user/bin/check-updates
```

# Dependencies
yay, fakeroot, notify-send.sh (https://github.com/vlevit/notify-send.sh)

# License
MIT
