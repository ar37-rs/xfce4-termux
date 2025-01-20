![alt_test](image/xfce4.png)

# Installation:
Install latest termux-x11 official:

https://github.com/termux/termux-x11

or install one of the most stable versions and slightly modified for smoother experience from here:

[termux-x11](https://github.com/ar37-rs/xfce4-termux/releases/download/Backup/termux-x11-arm64-v8a-debug.zip)

and then
```
cd && pkg install wget openssl && rm -rf ~/xfce4 && wget https://github.com/ar37-rs/xfce4-termux/raw/refs/heads/main/xfce4 && chmod +x ~/xfce4
```
# Usage from termux terminal:
Install xfce4 dependecies
```
~/xfce4 install
```

Using virglrenderer driver (for such Mali, Adreno many other modern supported GPUs)

[(Read more for virgl additional usage)](https://github.com/ar37-rs/virgl-angle-termux)
```
~/xfce4 driver=virpipe
```

Using llvmpipe driver (software renderer Universal CPUs)
```
~/xfce4 driver=lvp
```

Using llvmpipe driver + zink
```
~/xfce4 driver=lvp-zink
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

# Note:

* If there's problem when installing, make sure the latest correct termux app version is installed from here:
   https://github.com/termux/termux-app/releases

* Tested using termux app v0.119.0-beta.1

* Fix for android 12+ with [Process completed (signal 9) - press Enter] issue (using adb):
   For Android 12L & Android 13+
   ```
   adb shell "settings put global settings_enable_monitor_phantom_procs false"
   ```

   For Android 12：
   ```
   adb shell "/system/bin/device_config set_sync_disabled_for_tests persistent; /system/bin/device_config put activity_manager max_phantom_processes 2147483647"
   ```

   [Read more from here](https://ivonblog.com/en-us/posts/fix-termux-signal9-error/) or [here](https://github.com/termux/termux-app/issues/2366)
