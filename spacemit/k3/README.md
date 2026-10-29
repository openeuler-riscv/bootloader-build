# Usage

Boot into BROM fastboot mode then:

```shell
fastboot stage FSBL.bin
fastboot continue
sleep 10
fastboot stage u-boot.itb
fastboot continue
sleep 1
fastboot flash mtd partition_4M.json
fastboot flash bootinfo bootinfo_spinor.bin
fastboot flash fsbl FSBL.bin
fastboot flash env u-boot-env-default.bin
fastboot flash esos esos_rt24.itb
fastboot flash opensbi fw_dynamic.itb
fastboot flash uboot u-boot.itb
```

Optional EC firmware upgrading:

```shell
fastboot stage ec.bin
fastboot oem ec:flash
```

Optional system image deploying:

```shell
# For UFS
fastboot flash scsi xxx.img
# For NVMe
fastboot flash nvme xxx.img
```
