# hue-wal
Setting Philips Hue lights to random pywal-colors
The idea and parts of the code are based on https://github.com/bisspector/openrazer_pywal a python script to set razer deives to random pywal-colors.

hue-wal can either be used with commandline arguments or by creating a config file.
This config file can be passed by a flag or has to be in ~/.config/hue-wal/config

usage: hue-wal.py [-h] [-i IP] [-c CONFIG] [-cl COLOR] [-ca COLORALL] [-ccl] [-rb] [-b BRIGHTNESS] [-bl BRIGHTNESSLIGHT] [-l LIGHTS]

optional arguments:<br /><br />
  -h, --help            show this help message and exit<br /><br />
  -i IP, --ip IP        provide bridge-ip (1.1.1.1)<br /><br />
  -c CONFIG, --config CONFIG<br />
                        provide config (/path/to/file)<br /><br />
  -cl COLOR, --color COLOR<br />
                        provide one single color for each lightin hex (ffffff)<br /><br />
  -ca COLORALL, --color-all COLORALL<br />
                        provide colors for each lights in hex ('ffffff,fffff')<br /><br />
  -ccl, --config-color  use colors from config<br />
  -rb, --random-brightness<br />
                        use random brightness for each light<br /><br />
  -b BRIGHTNESS, --brightness BRIGHTNESS<br />
                        provide one brightnessvalue for the lights 1-254 (1)<br /><br />
  -bl BRIGHTNESSLIGHT, --brightness-light BRIGHTNESSLIGHT<br />
                        provide brighnessvalues for each light 1-254 ('1,1')<br /><br />
  -l LIGHTS, --lights LIGHTS<br />
                        specify the light/lights to use ('light1,light2')<br /><br />

or just create a config like this:<br />
[bridge]<br />
#ip-adress of the bridge<br />
ip=ip.of.the.bridge<br />
<br />
[lights]<br />
#names of the lights you want to use<br />
name = ['light1', 'light1', 'light3']<br />
#brightness of the lights<br />
brightness = [254, 254, 254]<br />
#optinal color value in hex<br />
colors = ['111111', 'dd8452', '111111']<br />
<br />
This is my first time doing something in python if there is something that can be done better or you have some new ideas just let me know.
