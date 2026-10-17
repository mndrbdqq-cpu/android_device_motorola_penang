# AUR generation notes for motorola/penang

This tree was produced by `twrpdtgen` and post-processed by AUR. Review the items below before building — generators cannot detect everything from a boot image alone.

## Device summary

- Brand / model: **motorola / Holi for arm64**
- Platform: `holi` (arch: `arm64-v8a`)
- Android: 16 (SDK 36)
- A/B device: **yes**
- Dynamic partitions / super: **yes**
- Treble: yes
- Bootloader: `MBM-3.0-uefi-6a711df3e830-260723-U1TPS34.29-83-6-17-e33e7`
- Kernel: `Linux localhost 5.4.295-moto-17290-gb779c804ad8e #1 SMP PREEMPT Thu Jul 23 20:41:14 EDT 2026 aarch64 Toybox`

## Things to verify before building

- [ ] `BoardConfig.mk` flags match this device's SoC and partition scheme
- [ ] `recovery.fstab` mount points match `device.recovery.fstab` / `device.fstab` (this dir)
- [ ] Touch driver (init.recovery.<platform>.rc) loads for your panel
- [ ] Display resolution / pixel format in BoardConfig.mk matches device
- [ ] A/B build flags present: `AB_OTA_UPDATER`, `BOARD_USES_RECOVERY_AS_BOOT` if applicable
- [ ] Dynamic partition / super flags: `BOARD_USES_RECOVERY_AS_BOOT` may be required; consider `PRODUCT_USE_DYNAMIC_PARTITIONS := true`

## Partition map seen on device

| Logical name | Block device | Size |
|---|---|---|
| `boot_a` | `/dev/block/sdd18` | ? |
| `boot_b` | `/dev/block/sdf18` | ? |
| `dtbo_a` | `/dev/block/sdd20` | ? |
| `dtbo_b` | `/dev/block/sdf20` | ? |
| `logo_a` | `/dev/block/sdd17` | ? |
| `logo_b` | `/dev/block/sdf17` | ? |
| `metadata` | `/dev/block/sde9` | ? |
| `misc` | `/dev/block/sde4` | ? |
| `persist` | `/dev/block/sde2` | ? |
| `super` | `/dev/block/sde25` | ? |
| `userdata` | `/dev/block/sde26` | ? |
| `vbmeta_a` | `/dev/block/sdd11` | ? |
| `vbmeta_b` | `/dev/block/sdf11` | ? |
| `vendor_boot_a` | `/dev/block/sdd19` | ? |
| `vendor_boot_b` | `/dev/block/sdf19` | ? |
| `abl_a` | `/dev/block/sdd8` | ? |
| `abl_b` | `/dev/block/sdf8` | ? |
| `apdp` | `/dev/block/sde18` | ? |
| `bluetooth_a` | `/dev/block/sdd15` | ? |
| `bluetooth_b` | `/dev/block/sdf15` | ? |
| `carrier` | `/dev/block/sde11` | ? |
| `cid` | `/dev/block/sde8` | ? |
| `ddr` | `/dev/block/sda2` | ? |
| `devcfg_a` | `/dev/block/sdd5` | ? |
| `devcfg_b` | `/dev/block/sdf5` | ? |
| `devinfo` | `/dev/block/sde16` | ? |
| `dhob` | `/dev/block/sde15` | ? |
| `dsp_a` | `/dev/block/sdd16` | ? |
| `dsp_b` | `/dev/block/sdf16` | ? |
| `frp` | `/dev/block/sde5` | ? |
| `fsc` | `/dev/block/sde14` | ? |
| `fsg_a` | `/dev/block/sdd13` | ? |
| `fsg_b` | `/dev/block/sdf13` | ? |
| `hw` | `/dev/block/sda1` | ? |
| `hyp_a` | `/dev/block/sdd3` | ? |
| `hyp_b` | `/dev/block/sdf3` | ? |
| `keymaster_a` | `/dev/block/sdd6` | ? |
| `keymaster_b` | `/dev/block/sdf6` | ? |
| `kpan` | `/dev/block/sde10` | ? |
| `logfs` | `/dev/block/sde17` | ? |
| `modem_a` | `/dev/block/sdd14` | ? |
| `modem_b` | `/dev/block/sdf14` | ? |
| `modemst1` | `/dev/block/sde12` | ? |
| `modemst2` | `/dev/block/sde13` | ? |
| `padA` | `/dev/block/sde24` | ? |
| `prodpersist` | `/dev/block/sde3` | ? |
| `prov_a` | `/dev/block/sdd7` | ? |
| `prov_b` | `/dev/block/sdf7` | ? |
| `qupfw_a` | `/dev/block/sdd9` | ? |
| `qupfw_b` | `/dev/block/sdf9` | ? |
| `rpm_a` | `/dev/block/sdd1` | ? |
| `rpm_b` | `/dev/block/sdf1` | ? |
| `sda` | `/dev/block/sda` | ? |
| `sdb` | `/dev/block/sdb` | ? |
| `sdc` | `/dev/block/sdc` | ? |
| `sdd` | `/dev/block/sdd` | ? |
| `sde` | `/dev/block/sde` | ? |
| `sdf` | `/dev/block/sdf` | ? |
| `secdata` | `/dev/block/sde19` | ? |
| `secdataBackup` | `/dev/block/sde20` | ? |
| `ssd` | `/dev/block/sde1` | ? |
| `storsec_a` | `/dev/block/sdd4` | ? |
| `storsec_b` | `/dev/block/sdf4` | ? |
| `tz_a` | `/dev/block/sdd2` | ? |
| `tz_b` | `/dev/block/sdf2` | ? |
| `uefisecapp_a` | `/dev/block/sdd10` | ? |
| `uefisecapp_b` | `/dev/block/sdf10` | ? |
| `uefivarstore` | `/dev/block/sde21` | ? |
| `utags` | `/dev/block/sde6` | ? |
| `utagsBackup` | `/dev/block/sde7` | ? |
| `vbmeta_system_a` | `/dev/block/sdd12` | ? |
| `vbmeta_system_b` | `/dev/block/sdf12` | ? |
| `vm-data` | `/dev/block/sde23` | ? |
| `vm-keystore` | `/dev/block/sde22` | ? |
| `xbl_a` | `/dev/block/sdb1` | ? |
| `xbl_b` | `/dev/block/sdc1` | ? |
| `xbl_config_a` | `/dev/block/sdb2` | ? |
| `xbl_config_b` | `/dev/block/sdc2` | ? |


## OrangeFox overlay applied
- Added OF_* block to `BoardConfig.mk` — review screen height / quick-backup list
- Wrote `vendorsetup.sh` exporting `FOX_BUILD_DEVICE`
- Placeholder `recovery/recovery.fstab` written (may need hand-edit)
- Build with the OrangeFox manifest: https://gitlab.com/OrangeFox/sync
