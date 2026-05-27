[← Back to main page](/README.md)

# Rooting Guide

## Method 1: KernelSU-Next (Recommended)

This is the easiest method. No PC required.

1. Download the latest **KernelSU-Next Manager** APK from [here](https://github.com/KernelSU-Next/KernelSU-Next/releases).
2. Install and open the app.
3. Follow the on-screen instructions.

> [!NOTE]
> InfinityX ships with a KernelSU-Next compatible kernel. If the manager shows your device as supported, you are ready to go.

## Finished! ✅

---

## Method 2: Magisk

### Prerequisites

- [Recovery Image (TWRP for nabu)](https://github.com/ArKT-7/twrp_device_xiaomi_nabu/releases/tag/mod-win)
- [Android Platform Tools](https://developer.android.com/studio/releases/platform-tools)
- [Magisk APK](https://github.com/topjohnwu/Magisk/releases/latest)

---

### Step 1: Boot into fastboot

Power off the device and hold **Volume Down + Power**, or run:
```bash
adb -d reboot bootloader
```

Connect the device to your PC via USB.

---

### Step 2: Boot the recovery image

Replace the placeholder with the actual path to your downloaded recovery image:

```bash
# Windows:
fastboot boot path\to\recovery.img

# Linux / macOS:
fastboot boot path/to/recovery.img
```

---

### Step 3: Flash Magisk via recovery

Download `magisk.apk` to your PC and run:

```bash
# Windows:
adb push path\to\magisk.apk /tmp/magisk.zip && adb shell twrp install /tmp/magisk.zip

# Linux / macOS:
adb push path/to/magisk.apk /tmp/magisk.zip && adb shell twrp install /tmp/magisk.zip
```

---

### Step 4: Reboot into Android

```bash
adb reboot
```

> [!NOTE]
> If it doesn't boot automatically, hold the power button to reboot manually.

---

### Step 5: Complete Magisk setup

1. Install [Magisk APK](https://github.com/topjohnwu/Magisk/releases/latest) on the device if it isn't already there.
2. Open the **Magisk** app and follow the on-screen instructions.
3. The device will reboot to complete patching.

## Finished! ✅
