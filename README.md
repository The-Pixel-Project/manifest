<div align="center">

<img src="https://github.com/The-Pixel-Project/tpp_files/blob/main/TPPGithub.png?raw=true" >

</div>

A glimpse of the project
------------
The Pixel Project, an AOSP based custom rom lead by a passionate team aiming to provide a clean and smooth experience of stock android with Pixel Goodies.

Requirements
------------
- At least 250-300 GB free disk space.
- A computer/server with at least 16GB RAM running Linux and a fast & stable internet connection.
- Some basic knowledge of Linux commands, device tree management and git.

Instructions
------------
### Prerequisites
A properly configured build environment is required to build AOSP custom roms. A comprehensive guide for setting up the build environment can be found [here](https://source.android.com/setup/build/initializing).

Sync up the source
------------
```bash
repo init -u https://github.com/The-Pixel-Project/manifest -b fourteen --git-lfs

repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all) && repo forall -c git lfs pull
```

Build
------------
### Set up environment
```
. build/envsetup.sh
```
### Choose a target
```
lunch aosp_$device-ap1a-userdebug
```
### Build the code
```
make bacon -j$(nproc --all)
```
