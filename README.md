# Reading Streak
A reading streak app for the [Pala One](https://github.com/Chris24680/pala-one-firmware) e-ink reader.

## Controls

| Gesture | Action |
|---|---|
| Single click | Log the day |
| Hold | Exit to launcher |

## Building

Requires the ESP32-S3 toolchain installed by Arduino IDE (`~/.arduino15/packages/esp32/tools/esp-x32/`) and the [pala-one-firmware](https://github.com/Chris24680/pala-one-firmware) repo checked out alongside this one:

```
Work/
├── pala-one-firmware/
└── reading_streak/          ← this repo
```

Then:

```sh
make
```

This produces `reading_streak.bin`.


## Uploading

1. On the device, triple-click from the library screen to enter Upload mode.
2. Connect to the device's WiFi AP (`PALA-xxxxxx`, password `palaread`).
3. Open `http://192.168.4.1` and upload `reading_streak.bin` to `/apps/reading_streak.bin`.

The app will appear in the launcher on next boot.