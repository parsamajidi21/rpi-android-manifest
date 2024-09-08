# Rpi Android BSP Repo Manifest README

This repo is used to download manifests for Raspberry pi Android BSP releases.

The rpi-android-14 branch will include all release manifests for Android 14 rpi releases.

### To use this manifest repo, the 'repo' tool must be installed first.
```
$: mkdir ~/bin
$: curl http://commondatastorage.googleapis.com/git-repo-downloads/repo  > ~/bin/repo
$: chmod a+x ~/bin/repo
$: PATH=${PATH}:~/bin
```
### Setup build environment:
-------------------------
- Set up the environment for building. This only configures the current terminal.
$ source build/envsetup.sh

### Execute the Android lunch command.

lunch command can be issued with an argument <Build name>-<Build type> or can be issued without the argument presenting a menu of selection.
```
$ lunch <Build name>-<Build type>
# (Example: Build name :rpi_4b Build type: userdebug)
```
### Execute the "imx-make.sh" script to generate the image.
```
$ ./rpi-make.sh -j4 2>&1 | tee build-log.txt
```
When the make command is complete, the build-log.txt file contains the execution output. Check for any errors.
