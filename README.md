# #keepQASSA #

### Create a directory ###
```bash
 mkdir -p ~/rom/qassa
 cd ~/rom/qassa
```

### Sync ###
#### Initialize local repository ####
```bash
repo init -u ssh://git@github.com/keepQASSA/manifest -b Q
```

#### Sync ####
```bash
repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags
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
