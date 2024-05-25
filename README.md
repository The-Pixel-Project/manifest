# The Pixel Project #

## Sync

### Initialize local repository

```
repo init -u https://github.com/The-Pixel-Project/manifest -b fourteen --git-lfs
```

### Sync up 

```
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all) && repo forall -c git lfs pull
```

## Build

### Set up environment
```
. build/envsetup.sh
```
### Choose a target
```
lunch aosp_device-ap1a-userdebug
```
### Build the code
```
make bacon -j$(nproc --all)
```
