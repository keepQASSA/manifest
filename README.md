# Android Open Source `QASSA` Project #

## Building AOSQP
### Create a directory

```bash

 mkdir -p ~/rom/aosqp
 cd ~/rom/aosqp
```

### Sync ###

```bash

# Initialize local repository
repo init -u ssh://git@github.com/AOSQP/manifest -b Q

# Sync
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
```

### Build ###

```bash

# Set up environment
$ . build/envsetup.sh

# Choose a target
$ lunch aosqp_$device-userdebug

# Build the code
$ mka qassa -j$(nproc --all)
```
