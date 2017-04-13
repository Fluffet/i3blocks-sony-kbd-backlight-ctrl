# i3blocks-sony-kbd-backlight-ctrl

Simple script to control the backlight and timeout time of your Sony Vaio Pro keyboard directly from i3bar/blocks. Handy if you like to code by night or watch movies :)

You need write access for /sys/devices/platform/sony-laptop/kbd_backlight and /sys/devices/platform/sony-laptop/kbd_backlight_timeout so you need to do this once:

```sh
sudo chmod o+w /sys/devices/platform/sony-laptop/kbd_backlight /sys/devices/platform/sony-laptop/kbd_backlight_timeout
```

i3blocks config:
```
[sony-kbd-ctrl]
label= 
command=location_of_git_repo/i3blocks-sony-kdb-backlight-ctrl/sony-kbd-ctrl
interval=once
```

As a little good to know, note the file
```
/sys/devices/platform/sony-laptop/kbd_backlight_timeout
```
It has 3 modes:
  * 0(default)=inf
  * 1=10secs
  * 2=30secs 
  * 3=60s