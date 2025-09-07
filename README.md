# ESP32 Air Mouse - Web Flasher

This repository contains the web-based firmware flasher for the ESP32 Air Mouse project. It allows you to install the firmware directly to your ESP32 device from your web browser using the Web Serial API.

**[Live Flasher Link](https://your-username.github.io/your-repo-name/)** (Replace with your GitHub Pages URL after publishing)

## Features

- **Gyroscopic Air Mouse**: Control your cursor by moving the ESP32.
- **BLE Connectivity**: Connects to your computer wirelessly via Bluetooth Low Energy.
- **Button Support**: Left and Right click functionality.
- **Customizable Settings**: Adjust sensitivity, dead zone, and invert axes.
- **On-Device Calibration**: Calibrate the gyroscope for better accuracy.
- **Persistent Settings**: Saves your configuration to EEPROM.
- **Serial Command Interface**: Configure the device using serial commands.

## How to Use the Web Flasher

1.  **Connect Your Device**: Plug your ESP32 Air Mouse into your computer with a USB data cable.
2.  **Open the Flasher**: Navigate to the live flasher website.
3.  **Click Flash**: Click the "Flash Firmware" button.
4.  **Select COM Port**: A popup will appear. Choose the correct COM port for your ESP32 device and click "Connect".
5.  **Wait**: The flasher will automatically install the bootloader, partition table, and firmware. Do not disconnect the device.
6.  **Done**: Once the process is complete, the device will restart and be ready to use.

## Serial Commands

You can connect to the ESP32 with a serial monitor (at 115200 baud) to configure it using these commands:

| Command | Description |
|---|---|
| `SENS:<float>` | Set sensitivity multiplier (e.g., `SENS:1.2`) |
| `NAME:<text>` | Set the BLE device name |
| `DEADZONE:<float>`| Set the gyro dead zone in deg/s |
| `INVERTX` | Toggle the X-axis inversion |
| `INVERTY` | Toggle the Y-axis inversion |
| `CALIBRATE` | Start the gyro calibration sequence |
| `STATUS` | Print the current settings |
| `HELP` | Show all available commands |
| `SAVE` | Save the current settings to EEPROM |
| `LOAD` | Load settings from EEPROM |
| `RAW` | Toggle printing of raw gyro data |

## Author

Developed by **SK Raihan** at **SKR Electronics Lab**.
- [Website](https://www.skrelectronicslab.com/)
- [YouTube](https://youtube.com/@skr_electronics_lab)
- [Twitter](https://twitter.com/skrelectronics)

---
Powered by [ESP Web Tools](https://github.com/esphome/esp-web-tools).
