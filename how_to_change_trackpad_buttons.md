1. `sudo vim /usr/share/X11/xorg.conf.d/40-libinput.conf`





2. ***Add `Option "ClickMethod" "clickfinger"` to the inputclass of "touchpad"***
```
Section "InputClass"
        Identifier "libinput touchpad catchall"
        MatchIsTouchpad "on"
        MatchDevicePath "/dev/input/event*"
        Option "ClickMethod" "clickfinger"
        Driver "libinput"
EndSection
```

3. `sudo service lightdm restart`
