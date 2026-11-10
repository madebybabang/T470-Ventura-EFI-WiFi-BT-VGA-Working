![macOS](https://img.shields.io/badge/macOS-Ventura%2013.7.8-blue)
![OpenCore](https://img.shields.io/badge/OpenCore-0.8.8-green)
![Status](https://img.shields.io/badge/Status-Working-brightgreen)

# T470-Ventura-EFI-WiFi-BT-VGA-Working
The ultimate OpenCore EFI for ThinkPad T470 running Ventura. Fixes the infamous NULL Bluetooth, VGA monitor detection, and Trackpad scroll issues.

<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/2dd24c5b-dc83-48ae-8582-8b7bffbfb6f1" />



<img width="1402" height="732" alt="image" src="https://github.com/user-attachments/assets/4e45513f-557f-4fe5-a653-4321b7ce0966" />



<img width="918" height="606" alt="image" src="https://github.com/user-attachments/assets/03635bf2-922d-4f03-ab7e-625c01575c6b" />



<img width="912" height="606" alt="image" src="https://github.com/user-attachments/assets/3a03bb89-2324-449c-a1af-ccf7a2cc2dfe" />



<img width="915" height="604" alt="image" src="https://github.com/user-attachments/assets/9525a15d-db71-46b5-a622-51b0efe225b5" />


<img width="1107" height="521" alt="image" src="https://github.com/user-attachments/assets/3c8619e4-a9be-408a-aaad-183d74ef3e4b" />





# T470-Ventura-EFI-WiFi-BT-VGA-Working

**The ultimate OpenCore EFI for ThinkPad T470 running macOS Ventura.** 
This configuration was heavily tested and modified to fix the most common (and frustrating) Hackintosh issues on this specific laptop.

## 🔥 What's Fixed in this EFI:
*   **Bluetooth**: Fixed the infamous `NULL` state and crash loops. Bluetooth works perfectly out of the box.
*   **External Display (VGA)**: Fixed HDMI-to-VGA monitor detection using a custom `framebuffer` patch.
*   **Trackpad**: Fixed two-finger scroll and gestures (switched to `VoodooPS2Trackpad` for better compatibility).
*   **Wi-Fi**: Working flawlessly using `AirportItlwm` v2.2.0 (Native UI, no HeliPort needed).

## 💻 Hardware Specifications
*   **Laptop**: Lenovo ThinkPad T470
*   **CPU**: Intel Core i5-7300U (Kaby Lake)
*   **iGPU**: Intel HD Graphics 620
*   **Wi-Fi/BT**: Intel Dual Band Wireless-AC 8265 *(Adjust if your chip is different)*
*   **macOS**: Ventura 13.7.8 (Tested on External SSD via USB Enclosure)

## ✅ What's Working
*   **Graphics**: Intel HD 620 with full QE/CI (Hardware Acceleration).
*   **Audio**: Working (AppleALC, layout-id 29).
*   **Battery**: Working (SMCBatteryManager).
*   **USB Ports**: Mapped using USBToolBox & UTBMap.
*   **Keyboard & Fn Keys**: Working.

## ⚠️ IMPORTANT NOTES
*   **SMBIOS**: This repo is **SANITIZED**. You MUST generate your own SMBIOS (`MacBookPro14,1`) using GenSMBIOS and insert your Serial Number, MLB, UUID, and ROM into `PlatformInfo` in your `config.plist`.
*   **VGA Display**: The external display works but might be slightly darker. It is recommended to use the **BetterDisplay** app to adjust the brightness.
*   **Scroll Direction**: Use the **Mos** app to fix the reversed scroll direction between a physical mouse and the trackpad.

## 🙏 Credits
*   Acidanthera (OpenCore, Lilu, WhateverGreen, etc.)
*   OpenIntelWireless (AirportItlwm)
*   zxystd (IntelBluetoothFirmware)
*   KawaiiGirl2001 (Base ACPI inspiration)
