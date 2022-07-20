## Magisk v25.1-delta-3 by HuskyDG

> Synchronized with Magisk 8c17f54d-delta

### Diff from official

- [General] MagiskHide is restored and enabled by default
- [General] The package name is `io.github.huskydg.magisk`
- [MagiskHide] Hide Google SafetyNet process by default
- [General] Implement Core-only mode
- [General] Support installing Magisk into system partition
- [General] Add button to temporarily disable Magisk
- [General] Add button to download and install Riru core
- [General] Fix Magisk survival script `addon.d` when FBE cannot be decrypted: Change modules directory from `/data/adb/magisk` to `/data/unencrypted/MAGISKBIN` and symlink back
- [MagiskHide] Only reset sensitive props after boot completed
- [General] Change magisk directory from `/data/adb/modules` to `/data/unencrypted/magisk_modules` and symlink back on FBE so you can manage module from Recovery.
- [MagiskInit] Inject Magisk services through `exec` option
- [MagiskHide] Introduce MagiskHide Dualspace mode to hide Magisk from all apps on dual space
- [MagiskHide] Introduce MagiskHide WhiteList mode to hide Magisk from all apps except apps that have been previously granted root access from Magisk
- [Manager] Show all supported languages in Language settings for Chinese ROM
- [Modules] Support systemless deleting files or folders for modules. [Learn more about it...](https://huskydg.github.io/blog/delete-file-and-folder-by-magisk-module)
- [General] Introduce Anti Zygote loop feature to automatically boot into Core-only mode if zygote fails to start for many times (aka. bootloop)

### About MagiskHide WhiteList

After WhiteList is enabled, Magisk will be hidden from all apps by default and only previously apps have been granted root access from Magisk can continue to access Magisk.

Temporarily turn off MagiskHide WhiteList if you want to grant root access to new apps

MagiskHide WhiteList has significant performance and memory consumption issue and might break some modules that require app to read (overlay module, systemize app, ...). Only use WhiteList if necessary

### About Zygisk 💀

Zygisk is detectable and does not have hiding itself method like RiruHide. In additional, there are no hiding module that actually work, please don't enable Zygisk if unnecessary. [Read here to learn more about Zygisk...](https://huskydg.github.io/blog/zygisk-can-be-detected-very-easily)

## Magisk v25.1 Official changes

- [MagiskBoot] Fix ramdisk backup being incorrectly skipped
- [MagiskBoot] Add new feature to detect unsupported dtb and abort during installation
- [Zygisk] Change binary hijack paths
- [App] Fix incorrect recovery mode detection and installation
- [MagiskInit] Fix config not properly exported in legacy SAR devices
- [General] Enforce the Magisk app to always match or be newer than magiskd
