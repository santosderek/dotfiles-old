sudo vim /usr/share/X11/xorg.conf.d/40-libinput.conf





### Add `Option "ClickMethod" "clickfinger"` to the inputclass of "touchpad"
Section "InputClass"
        Identifier "libinput touchpad catchall"
        MatchIsTouchpad "on"
        MatchDevicePath "/dev/input/event*"
        Option "ClickMethod" "clickfinger"
        Driver "libinput"
EndSection


sudo service lightdm restart 
