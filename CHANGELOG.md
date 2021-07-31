## Changelog (forked)

### v1.14 (binary updates)
* Updated rclone to 1.56.0 for all supported architectures.
* Updated README.md to point to Termux packages source.

### v1.14
* Used @Zackptg5's MMT-EX module template.
* Cleaned all install & wrapper scripts.
* Fixed bugs related to `rclone` command not working (proper wrapper script placement).
* All the webservers (SFTP/FTP/HTTP) work fine now.
* Bring back x86 and x86_64 support.
* Updated all binaries (extracted from Termux builds).
  - `libandroid-support` (28)
  - `rclone` (1.55.0)
  - `fusermount` (2.9.9)
  - `inotifywait` (3.20.11.0)

## Changelog (source)

### v1.13
* Add arm/arm64 1.53 binaries downloaded from https://beta.rclone.org/v1.53.0/testbuilds/rclone-android-16-arm.gz

### v1.12
* Fixed restart problems.

### v1.11
* Add arm/arm64 1.52 bins downloaded from https://beta.rclone.org/v1.52.0/testbuilds/rclone-android-16-arm.gz
* Fixed service.sh paths

### v1.10
* fixed fusermount wrapper

### v1.9
* Add arm/arm64 1.51 bins downloaded from https://beta.rclone.org/
* Commented fusermount wrapper

### v1.8
* Support for Work Profiles `PROFILE=`
* Isolate to Work Profiles `ISOLATE=1`
* Support syncing from SD to remote 

### v1.7
* Add ability to disable HTTP/FTP
* Link rest of default params to custom vars
* Exclude some custom params from globals
* Make some globals exclusive
* Change `BINDPOINT=` to `SDBINDPOINT=`
* Fix bug with custom params
* Set `PATH=` to change priority of used bins

### v1.6
* Simplify custom global parameters
* Fix & improve binding to SD
* Specify additional  rclone ops with `ADD_PARAMS=`
* Replace `rclone mount` ops via `REPLACE_PARAMS=`

### v1.5
* Replace arm/arm64  `rclone` 1.48 bins built with Termux
* Replace arm/arm64 `fusermount` built with Termux
* Add arm/arm64 `libandroid-support.so` from Termux
* Support for mounting to SD
* Squash missing rclone.conf install bug
* Tune default parameters
* Include a wrap for `rclone config`
* Include `fusermount-wrapper.sh`
* General Improvements

### v1.4
* Add ability to disable a remote 
* Add a wrapper script for rclone
* Access remotes via http & ftp
* Use without rebooting device
* Add wrapper cmds to `rclone help`
* Make remount possible via `su -M -c`

### v1.3
* Move user rclone.conf & related to `/sdcard/.rclone/`
* Control global `--vfs-cache-mode` via simple files placed in `/sdcard/.rclone/`
* Specify custom params for individual remotes via `/sdcard/.rclone/.REMOTENAME.params`

### v1.2
* Change install process
* Changes for full systemless
* Improve mount reliability
* Symlink mountpoint to `/storage/`

### v1.1
* Initial release
* rclone mount
