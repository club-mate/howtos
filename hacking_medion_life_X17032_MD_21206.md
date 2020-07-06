# Hacking the Medion Life X17032 (MD 21206) Smart-TV

## Board
it's a 17MB120 board from the turkish manufacturer Vestel, but it should work also with other vestel boards

## service codes
got to menu and hit:
* 4725 for hidden service menu (be careful, you can brick it there)
* 1595 for starting FW update from USB Stick
* 7935 for Hotel Mode

## open ports
beside the crappy smart-tv functions (i've bought a firestick to make it a smart-tv with less pain) u can do funny things with this cheap UHD LED TV
* 7681 | listening to websockets
* 4660 | telnet remote control

## telnet remote shell (not tested yet)
### first
```bash
telnet 192.168.1.123 1986
telnetd -l /bin/sh #you get no response here, which is ok
```
### second
```bash
telnet 192.168.1.123 23
ls -la
# in /mnt/hd0a your usb stick is mounted
# in /vendor/vk_keymapping_db.xml you can find the remote control codes
```
## remote controll codes (not tested all)
* BUTTON_HOME 1046
* BUTTON_POWER    1012
* BUTTON_POWER_NAV    1012
* BUTTON_POWER_PLAYER 1012
* BUTTON_POWER_PVM    1012
* BUTTON_POWER_GES_NAV    1012
* BUTTON_POWER_GES_PLAYER 1012
* BUTTON_POWER_GES_PVM    1012
* BUTTON_RECORD   1051
* BUTTON_PLAY 1025
* BUTTON_PAUSE    1049
* BUTTON_STOP 1024
* BUTTON_PREVIOUS 1034
* BUTTON_REWIND   1027
* BUTTON_FORWARD  1028
* BUTTON_NEXT 1255
* BUTTON_SCREEN   1011
* BUTTON_LANG 1015
* BUTTON_SUBTITLE 1031
* BUTTON_PRESETS  1014
* BUTTON_EPG  1047
* BUTTON_TEXT 1255
* BUTTON_FAV  1040
* BUTTON_3D   1040
* BUTTON_SLEEP    1042
* BUTTON_0    1000
* BUTTON_1    1001
* BUTTON_2    1002
* BUTTON_3    1003
* BUTTON_4    1004
* BUTTON_5    1005
* BUTTON_6    1006
* BUTTON_7    1007
* BUTTON_8    1008
* BUTTON_9    1009
* BUTTON_MENU 1048
* BUTTON_MUTE 1013
* BUTTON_UP   1020
* BUTTON_LEFT 1021
* BUTTON_OK   1053
* BUTTON_RIGHT    1022
* BUTTON_DOWN 1019
* BUTTON_VOL_UP   1016
* BUTTON_VOL_DOWN 1017
* BUTTON_VOL_UP_2 1016
* BUTTON_VOL_DOWN_2   1017
* BUTTON_PROG_UP  1032
* BUTTON_PROG_DOWN    1033
* BUTTON_BACK 1010
* BUTTON_EXIT 1037
* BUTTON_RED  1055
* BUTTON_GREEN    1054
* BUTTON_YELLOW   1050
* BUTTON_BLUE 1052
* BUTTON_INFO 1018
* BUTTON_MMEDIA   1057
* BUTTON_SOURCE   1056
* BUTTON_SWAP 1034
* BUTTON_CHAN 1045
* BUTTON_QMENU    1043

## contributing
if you like to share your expierience / thoughts, feel free to pull a request

## sauce
* [https://community.medion.com/t5/Video/Probleme-nach-Firmware-Update-MEDION-LIFE-MB-120-LED-Backlight/td-p/62850/page/3](https://community.medion.com/t5/Video/Probleme-nach-Firmware-Update-MEDION-LIFE-MB-120-LED-Backlight/td-p/62850/page/3)
* [https://shkspr.mobi/blog/2018/11/telnet-control-of-toshiba-smart-tvs/](https://shkspr.mobi/blog/2018/11/telnet-control-of-toshiba-smart-tvs/)

## more coming soon ...
