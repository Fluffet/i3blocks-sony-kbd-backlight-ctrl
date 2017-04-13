# i3blocks-sony-kbd-backlight-ctrl

Simple script to control the backlight of your Sony Vaio Pro keyboard directly from i3bar/blocks. Handy if you like to code by night or watch movies :)

Also be aware of:
/sys/devices/platform/sony-laptop/kbd_backlight_timeout where: 0(default)=10secs, 1=30secs, 2=60secs and 3=unlimited.

You need write access for /sys/devices/platform/sony-laptop/kbd_backlight, so you need to do this once:

'''sh
sudo chmod o+w /sys/devices/platform/sony-laptop/kbd_backlight
'''

i3blocks config:
'''
[sony-kbd-ctrl]
label= 
command=location_of_git_repo/i3blocks-sony-kdb-backlight-ctrl/sony-kbd-ctrl
interval=once
'''
