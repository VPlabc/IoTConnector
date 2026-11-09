# IoTConnector firmware releases

Firmware images for IoTConnecter boards, fetched by the on-device OTA pull
(HTTPS via raw.githubusercontent.com).

```
iotconn-esp32/manifest.json      # V1 board (ESP32, 4 MB)
iotconn-esp32s3/manifest.json    # V2 board (ESP32-S3)
iotconn-<target>/iotconnecter-<version>.bin
```

Boards check the manifest periodically, download a newer image into the
inactive slot, and wait for the user to confirm the install. Nothing is
installed automatically.

Images are published with `tools/release-fw.ps1` from the main project.
Firmware signing is not enabled yet: only trusted maintainers may push here.
