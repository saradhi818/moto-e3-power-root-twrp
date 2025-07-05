# Moto E3 Power Root and TWRP Setup

This repository contains essential tools and files to root and install TWRP on the **Motorola Moto E3 Power (XT1706)**.

## 📱 Device Details

- **Model:** Motorola Moto E3 Power XT1706
- **Android Version:** 6.0 (Marshmallow)
- **CPU Architecture:** ARMv7

---

## ⚠️ Disclaimer

> Rooting your device voids warranty and may brick your phone if steps are not followed correctly. Proceed at your own risk.

---

## 🛠️ Files Included

- **ADB & Fastboot tools:** `adb.exe`, `fastboot.exe`, `adb-setup-1.4.3.exe`, DLLs
- **TWRP Recovery Image:** `decker.img`
- **Rooting Zip:** `SuperSU-v2.79-201612051815.zip`
- **Command Guide:** `Commands.txt`

---

## 🔓 Step-by-Step Rooting Guide

### 1. **Preparation**

- Install Motorola USB drivers on PC.
- Enable **Developer Options**, **OEM Unlock**, and **USB Debugging** on the phone.

### 2. **Unlock Bootloader**

1. Reboot to bootloader:
    ```bash
    adb reboot bootloader
    ```

2. Get unlock data:
    ```bash
    fastboot oem get_unlock_data
    ```

3. Paste it on [Motorola Unlock Site](https://motorola-global-portal.custhelp.com/app/standalone/bootloader/unlock-your-device-b) to receive unlock key.

4. Unlock:
    ```bash
    fastboot oem unlock UNIQUE_UNLOCK_KEY
    ```

---

### 3. **Flash TWRP Recovery**

```bash
fastboot flash recovery decker.img
fastboot reboot
