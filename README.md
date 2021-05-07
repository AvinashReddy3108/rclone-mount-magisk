<h1 align="center">Cloud Storage Mounter for Magisk (prev: rclone-mount)</h1>

<div align="center">
  <!-- Version -->
    <img src="https://img.shields.io/badge/Version-v1.14-blue.svg?longCache=true&style=for-the-badge"
      alt="Version" />
  <!-- Last Updated -->
    <img src="https://img.shields.io/badge/Updated-April 22, 2021-green.svg?longCache=true&style=for-the-badge"
      alt="_time_stamp_" />
  <!-- Min Magisk -->
    <img src="https://img.shields.io/badge/Magisk-20.0%2B-red.svg?longCache=true&style=for-the-badge"
      alt="_time_stamp_" /></div>

<div align="center">
  <strong>This is the spiritual successor of <a href="https://github.com/Magisk-Modules-Repo/com.piyushgarg.rclone">rclone-mount</a> with bug fixes and newer binaries included. More details in the
    <a href="https://github.com/AvinashReddy3108/rclone-mount-magisk/wiki">wiki</a>.
</div>

<div align="center">
  <h3>
    <a href="https://github.com/AvinashReddy3108/rclone-mount-magisk">
      Source Code
    </a>
    <span> | </span>
    <a href="https://github.com/Magisk-Modules-Repo/com.piyushgarg.rclone">
      Original Module Repository
    </a>
    <span> | </span>
    <a href="https://github.com/AvinashReddy3108/rclone-mount-magisk/issues">
      Issues
    </a>
  </h3>
</div>

### Features
- Support for arm, arm64, ~~& x86~~ (will be back soon)
- Huge list of [supported cloud storage providers](https://rclone.org/#providers)
- Apps with ability to specify paths can access the remotes at `/mnt/cloud/`.
- Most file explorers work just fine ([read more on this](https://github.com/Magisk-Modules-Repo/com.piyushgarg.rclone/issues/9)).
- Mount points use names of remote(s) in rclone.conf
- Specify custom rclone params for each remote via `/sdcard/.rclone/.REMOTE.param`
- Access remotes via HTTP or (S)FTP clients, or bind the remotes to `/sdcard/Cloud/REMOTE` (recommended to [read this](https://github.com/Magisk-Modules-Repo/com.piyushgarg.rclone/issues/5)).
- Support for Work Profiles.

### Configuration
1. Copy your `rclone.conf` file (if you have one already) to `/sdcard/.rclone/rclone.conf` (can always be generated later.)
2. Add custom params at `/sdcard/.rclone/.[global/REMOTE].param` (if needed)
3. Install the module via Magisk Manager
4. Run `rclone config` via term if additional setup required
4. All your rclone mount points will show up under `/mnt/cloud/` & `/storage/cloud/` or `/sdcard/cloud/`

For more detailed configuration of rclone please refer to [official documentation](https://rclone.org)

### Known Issues
- VLC  takes a long time to load media as it opens file in write mode when using it's internal browser.

   a. Create remote type alias for media dirs in rclone.conf and
specify `CACHEMODE=off` in `/sdcard/.rclone/.ALIASNAME.param`

- Encrypted devices can not mount until unlock
- Encrypted `rclone.conf` causes reboots
- High cpu/mem in some apps with storage perms ([issue #9](https://github.com/Magisk-Modules-Repo/com.piyushgarg.rclone/issues/9))
- The `fusermount` bin may not be compatible on all devices (see [thread](https://www.google.com/amp/s/forum.xda-developers.com/android/development/fusermount-android-rclone-mount-t3866652/amp/))

## Disclaimer
- Neither the author nor devs will be held responsible for any damage/data loss that may occur during use of this module.
- While we have done our best to make sure no harm will come about, no guarantees can be made.
- Keep in mind the binaries included in this project are BETA quality (at best), which may cause unforseen issues.

Always check this document before updating to new releases as significant changes may occur.

## Credits
- rclone devs
- pmj_pedro[@xda](https://forum.xda-developers.com/showpost.php?p=78147335&postcount=1)
- agnostic-apollo[@xda](https://forum.xda-developers.com/showpost.php?p=79929083&postcount=12)
- Termux for building and hosting binaries for [rclone](https://10.via0.com/ipns/k51qzi5uqu5dg9vawh923wejqffxiu9bhqlze5f508msk0h7ylpac27fdgaskx/pool/main/r/rclone), [fusermount](https://grimler.se/termux-root-packages-24/pool/stable/libf/libfuse2/), [inotifywait](https://10.via0.com/ipns/k51qzi5uqu5dg9vawh923wejqffxiu9bhqlze5f508msk0h7ylpac27fdgaskx/pool/main/i/inotify-tools), [libandroid-support.so](https://10.via0.com/ipns/k51qzi5uqu5dg9vawh923wejqffxiu9bhqlze5f508msk0h7ylpac27fdgaskx/pool/main/liba/libandroid-support).
- improvements by geofferey@github
- @Zackptg5 for MMT-EX Module template.
