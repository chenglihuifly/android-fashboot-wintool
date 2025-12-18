# Android Platform Tools for Windows

This repository contains the Android SDK Platform Tools for Windows, which are essential command-line utilities for Android development and device management.

## Contents

This package includes the following tools:

### Core Tools

- **adb.exe** - Android Debug Bridge: A versatile command-line tool for communicating with Android devices
- **fastboot.exe** - A tool for flashing firmware and other system images to Android devices
- **AdbWinApi.dll** & **AdbWinUsbApi.dll** - Windows API libraries required for ADB functionality

### Development Tools

- **aapt.exe** - Android Asset Packaging Tool: Compiles and packages Android app resources
- **aidl.exe** - Android Interface Definition Language: Generates Java interfaces from AIDL files
- **dexdump.exe** - DEX file parser and dumper for analyzing Android bytecode
- **dx.bat** - Converts Java bytecode to Dalvik bytecode
- **llvm-rs-cc.exe** - RenderScript compiler

### Additional Components

- **renderscript/** - RenderScript compiler headers and includes
- **api/** - API version definitions
- **lib/** - Required libraries (dx.jar)

## Usage

### ADB (Android Debug Bridge)

Connect to an Android device via USB or network:

```bash
# Check connected devices
adb devices

# Install an APK
adb install app.apk

# Access device shell
adb shell

# Push/pull files
adb push local.txt /sdcard/
adb pull /sdcard/file.txt
```

### Fastboot

Flash system images (requires bootloader mode):

```bash
# Check connected devices in fastboot mode
fastboot devices

# Flash system image
fastboot flash system system.img

# Reboot device
fastboot reboot
```

## Requirements

- Windows operating system
- USB drivers for your Android device (if connecting via USB)
- Developer options and USB debugging enabled on your Android device

## License

See [NOTICE.txt](NOTICE.txt) for licensing information.

## Notes

These tools are part of the Android SDK and are maintained by Google. This repository provides a convenient Windows distribution of these essential utilities.
