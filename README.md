# About
This script is a bash alternative of aarchup - an update checking daemon with notifications. It will write the database to RAM to save on HDD/SSD write cycles. The idea is because it resyncs the database so frequently, writing directly to the disk constantly could shorten its lifetime.

It doesn't require root priveleges, and will prompt to update with xterm and dialog if any are found. You can press <kbd>y</kbd>, <kbd>LeftArrow-Enter</kbd> or double click the "Yes" box to begin updating. If you don't want to update just press <kbd>Enter</kbd>, <kbd>n</kbd> or <kbd>Esc</kbd> twice.

# Install
```bash
wget https://raw.githubusercontent.com/644/check-updates/master/check-updates
sudo install -m 0755 check-updates /usr/local/bin/
```

Then add the script to a normal user's cronjob (cronie) with ```crontab -e```

Example cron script, runs check-updates every 15 minutes
```
PATH=/bin:/usr/bin:/usr/local/bin
*/15 * * * * check-updates
```

# Dependencies
- yay
- fakeroot
- notify-send
- cronie
- dialog (probably installed)
- xterm (probably installed)

# License
MIT
