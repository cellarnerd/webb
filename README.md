# James Webb telescope display
My James Webb telescope display.

There's a video showing how I built it: https://youtu.be/9QwxIP4gGE8

Currently, this is only an HTML file and these instructions. Oh, and the startup file for the Pi. In the future there will be an automation here, so if you decide to build your own – come back after the telescope has been adjusted and has started publishing proper images.

Add the webb.html file to your own chosen folder. Images are added to the img/ subfolder, and need to be added manually in the images array from line 32. 

You will have to install unclutter: 

```
sudo apt install unclutter
```

To add autostart:

```
sudo nano .config/lxsession/LXDE-pi/autostart
```

Add the following:

```
@lxpanel --profile LXDE-pi
@pcmanfm --desktop --profile LXDE-pi
@xscreensaver -no-splash
point-rpi
unclutter -idle 0
@chromium-browser --start-fullscreen --start-maximized --incognito --noerrdialogs file:///home/pi/webb/index.html
```

The Fusion 360-file:

https://a360.co/373ju2M
