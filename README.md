# pi-py-restarter
Python script that starts a server to handle reboot requests via REST

Sometimes my Raspberry Pi SSH session will hang, and the only solution is a restart. I got tired of walking across the room to unplug it.

## Directions

1. Create the file in `/home/pi/rebootSrv.py`
2. Setup a cron schedule so the script is run on reboot. Run `sudo crontab -e` and then add the line `@reboot python /home/pi/rebootSrv.py`

That should do it! Now when you reboot your pi you should be able to trigger the script by navigating to `http://X.X.X.X:6502/rebootSrv.py`

References -
* https://forums.raspberrypi.com/viewtopic.php?t=98153
* https://www.instructables.com/Raspberry-Pi-Launch-Python-script-on-startup/
* https://www.reddit.com/r/linux4noobs/comments/5vbmq8/getting_errors_whenever_i_try_to_reboot_or/
