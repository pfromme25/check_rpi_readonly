# check_rpi_readonly

Icinga check command to monitor if a Raspberry Pi OS system is in read only mode.

## Requirements

* python3 (>=3.6)
* raspi-config

## Usage

### Behavior

This script checks if boot is mounted as read only and overlayfs is in use.

By default the check state will switch to critical only if both conditions (boot is writable and overlayfs is not in use) are met and warning, if one condition is met.

You can change this behavior by setting either one of the arguments to directly switch to critical, if either (boot read only or overlayfs check) fails.

### Arguments
```
optional arguments:
  -h, --help          show this help message and exit
  -b, --boot_crit     If boot is rw, set state to critical
  -o, --overlay_crit  If overlayfs is disabled, set state to critical
```

