![alt_test](image/xfce4.png)

# Installation:
Install latest termux-x11 official:

https://github.com/termux/termux-x11

or install one of the most stable versions and slightly modified for smoother experience from here:

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
Using virglrenderer driver (Universal GPUs)

[(Read more for virgl additional usage)](https://github.com/ar37-rs/virgl-angle-termux)
```
~/xfce4 driver=virpipe
```

Using llvmpipe driver (Universal CPUs)
```
~/xfce4 driver=llvmpipe
```

Using llvmpipe driver + zink (Universal CPUs)
```
~/xfce4 driver=llvmpipe-zink
```

Using default driver can be combined with zink, kgsl for Adreno, amd for Xclipse or any supported other gpu drivers (if any)
```
~/xfce4 driver=default
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

# Note
Solution for android 12+ with [Process completed (signal 9) - press Enter] issue:

[Read more from here](https://github.com/termux/termux-app/issues/2366)
