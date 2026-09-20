# mylo-releases

Firmware binaries for [Mylo](https://github.com/BIOCOM-TECH-US/mylo-gateway).

Devices fetch `manifest.json` from this branch and update themselves.

**This repository is public so that devices can reach it anonymously.**

## Layout

| file | purpose |
| --- | --- |
| `manifest.json` | version, filename, size, sha256, source commit |
| `firmware.bin` | the OTA image (a bare app image, **not** a factory image) |
