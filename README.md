# The Pixel Project

## Build Process

### Initialize local repository
```
repo init -u https://github.com/The-Pixel-Project/manifest -b 15 --git-lfs
```
### Sync
```
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

### Build ###

```
. build/envsetup.sh
```
```
lunch aosp_$device-bp1a-$build_type
```
```
make bacon -j$(nproc --all)
```
