# Installation:
Install latest termux-x11 official:

https://github.com/termux/termux-x11

or install one of the most stable versions from here:

[termux-x11](https://github.com/ar37-rs/xfce4-termux/releases/download/Backup/termux-x11-arm64-v8a-debug.zip)

and then
```
cd && pkg install wget && rm -rf ~/xfce4 && wget https://github.com/ar37-rs/xfce4-termux/releases/download/latest/xfce4 && chmod +x ~/xfce4
```
# Usage from termux terminal:
Install xfce4 dependecies
```
~/xfce4 install
```
Using virglrenderer

[(Read more for virgl additional usage)](https://github.com/ar37-rs/virgl-angle-termux)
```
~/xfce4 use-virgl
```
and then simply start xfce
```
~/xfce4
```
# Additional usage:
Quite or terminate all xfce4 and 3d party process
```
~/xfce4 q
```
Switch back using default renderer instead of virgl
```
~/xfce4 default
```
# Note
Solution for android 12+ with [Process completed (signal 9) - press Enter] issue:

[Read more from here](https://github.com/termux/termux-app/issues/2366)
