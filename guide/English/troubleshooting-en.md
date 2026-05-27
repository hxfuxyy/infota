[← Back to main page](/README.md)

# Troubleshooting

<details>
<summary>Device not detected in fastboot / ADB</summary>

- Try a different USB cable — many cables are charge-only and do not support data transfer
- Try a different USB port (prefer USB 2.0 over USB 3.0)
- On Windows: install or reinstall [Google USB Driver](https://developer.android.com/studio/run/win-usb) or use [Universal ADB Driver](https://adb.clockworkmod.com/)
- Make sure **USB Debugging** is enabled in Developer Options
- Run `adb devices` or `fastboot devices` to confirm the device is listed

</details>

<details>
<summary>Boot loop after flashing</summary>

- Boot into recovery and perform **Factory Reset > Format data**
- Re-flash the ROM via ADB sideload or Auto Installer
- Make sure you flashed the correct ROM version for your device (nabu)

</details>

<details>
<summary>Stuck on first boot / boot animation</summary>

- First boot can take **5–10 minutes** — wait before assuming something is wrong
- If it exceeds 15 minutes, reboot into recovery, perform a Factory Reset, and re-flash

</details>

<details>
<summary>ADB sideload fails or shows an error</summary>

- Make sure the device is in sideload mode: **Apply Update > Apply from ADB**
- Verify the ZIP is not corrupted — re-download if needed
- Use the `-d` flag: `adb -d sideload InfinityX.zip`
- On Windows: run as Administrator; on Linux/macOS: use `sudo`

</details>

<details>
<summary>Auto Installer script fails or exits early</summary>

- Make sure the extracted folder path has **no spaces or special characters**
- On Windows: right-click the `.bat` file and **Run as Administrator**
- On Linux/macOS: grant execute permission — `chmod +x install_..._linux.sh`
- Check that `fastboot devices` detects your tablet before running the script
- Do not close the terminal or disconnect the device during execution

</details>

<details>
<summary>No sound / Wi-Fi not working after first boot</summary>

- Reboot the device once — some HALs initialize on second boot
- If still not working after a reboot, perform a clean re-flash with Factory Reset

</details>

<details>
<summary>OTA update fails / updater not showing new version</summary>

- Check your internet connection and retry
- Make sure you are on the latest stable release — beta/unofficial builds may not receive OTA
- Update manually via Recovery (Option A) using the latest ZIP from [Releases](https://github.com/hxfuxyy/InfinityX-XiaomiPad5/releases/latest)

</details>

---

> Still not solved? Join [t.me/InfinityXnabu](https://t.me/InfinityXnabu) and describe your issue with logs if possible.
