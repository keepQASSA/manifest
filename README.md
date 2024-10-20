# #keepQASSA #

### Create a directory ###
```bash
 mkdir -p ~/rom/qassa
 cd ~/rom/qassa

```

### Sync ###
#### Initialize local repository ####
```bash
repo init -u ssh://git@github.com/keepQASSA/manifest -b Q-rzy --depth=1 --git-lfs
```

#### Sync ####
```bash
repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

### Build ###
#### Set up environment ####
```bash
$ . build/envsetup.sh
```

#### Choose a target ####
```bash
$ lunch qassa_$device-userdebug
```

#### Build the code ####
```bash
$ mka qassa -j$(nproc --all)
```
