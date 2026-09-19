# mylo-releases

Firmware binaries for [Mylo](https://github.com/BIOCOM-TECH-US/mylo-gateway).
Source lives in a private repository; only built artifacts are published here.

Devices fetch `manifest.json` from this branch and update themselves. The
manifest records the source commit each binary was built from, so any unit in
the field can be traced back to code.

**This repository is public so that devices can reach it anonymously.** An
access token embedded in firmware would be a shared secret in every unit,
extractable from flash, and revoking it would break updates fleet-wide.

## Layout

| file | purpose |
| --- | --- |
| `manifest.json` | version, filename, size, sha256, source commit |
| `firmware.bin` | the OTA image (a bare app image, **not** a factory image) |

Always the latest release; history holds the previous ones.
