# Description
This short script is a replacement for aarchup - an update checking daemon with notifications. It will write the database to RAM to save on HDD/SSD write cycles. The idea is because it resyncs the database so frequently, writing directly to the disk could easily shorten its lifetime.

# Installation
Just download and add the script to a root cronjob (cronie), and change the username variable in the script. It requires yay, which provides AUR update checks as well.
