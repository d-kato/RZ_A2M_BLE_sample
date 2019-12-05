# RZ_A2M_BLE_sample
This is a sample program that works on RZ/A2M boards and RZ/A1 boards.  
- [RZ/A2M](https://www.renesas.com/us/en/products/microcontrollers-microprocessors/rz/rza/rza2m.html)
- [RZ/A1H](https://www.renesas.com/us/en/products/microcontrollers-microprocessors/rz/rza/rza1h.html)
- [RZ/A1LU](https://www.renesas.com/us/en/products/microcontrollers-microprocessors/rz/rza/rza1lu.html)


## Overview
It is equivalent to the following sample. Please refer to the following description.  
[BLE_LED](https://github.com/ARMmbed/mbed-os-example-ble/blob/master/BLE_LED)

The following samples that operate in the peripheral role also work. Replace the source folder and build.  
- [BLE_Button](https://github.com/ARMmbed/mbed-os-example-ble/blob/master/BLE_Button)  
- [BLE_BatteryLevel](https://github.com/ARMmbed/mbed-os-example-ble/blob/master/BLE_BatteryLevel)  
- [BLE_HeartRate](https://github.com/ARMmbed/mbed-os-example-ble/blob/master/BLE_HeartRate)  
- [BLE_Thermometer](https://github.com/ARMmbed/mbed-os-example-ble/blob/master/BLE_Thermometer)  


## Requirements
The following targets have been tested and work with these examples:

- [RZ/A2M Evaluation Board Kit](https://www.renesas.com/jp/en/products/software-tools/boards-and-kits/eval-kits/rz-a2m-evaluation-board-kit.html) (RZ/A2M)  
  - [Pmod ESP32](https://store.digilentinc.com/pmod-esp32-wireless-communication-module/)  
    Please update ESP32 FW ``AT version:1.1.3.0`` or later.  
    ![](docs/img/Pmod_ESP32_img.jpg)  
    ![](docs/img/Pmod_ESP32_connection.png)  


- [SBEV-RZ/A2M](http://www.shimafuji.co.jp/products/1486) (RZ/A2M)  
  - IoT-Engine WIFI ESP32 (SEMB1401-1)  


- [SEMB1402](http://www.shimafuji.co.jp/products/1505) (RZ/A2M)  
  - IoT-Engine WIFI ESP32 (SEMB1401-1)  


- [GR-LYCHEE](https://os.mbed.com/platforms/Renesas-GR-LYCHEE/) (RZ/A1LU)  
  - It is equipped with ESP32.  
    Please update ESP32 FW ``AT version:1.1.3.0`` or later.  


- [GR-PEACH](https://os.mbed.com/platforms/Renesas-GR-PEACH/)  (RZ/A1H)
  - [GR-PEACH Wireless CAMERA Shield](https://www.core.co.jp/product/m2m/gr-peach/audio-camera.html)  
    Please update ESP32 FW ``AT version:1.1.3.0`` or later.  


The sample application can be seen on any BLE scanner on a smartphone. If you don't have a scanner on your phone, please install:

- [nRF Master Control Panel](https://play.google.com/store/apps/details?id=no.nordicsemi.android.mcp) for Android.

- [LightBlue](https://itunes.apple.com/gb/app/lightblue-bluetooth-low-energy/id557428110?mt=8) for iPhone.


## About custom boot loaders
This sample uses a custom boot loader, and you can drag & drop the "xxxx_application.bin" file to write the program.  

1. Hold down ``SW3 (UB0)`` and press the reset button. (Or turn on the power.)  
2. Connect the USB cable to the PC, you can find the ``MBED`` directory.  
3. Drag & drop ``xxxx_application.bin`` to the ``MBED`` directory.  
4. When writing is completed, press the reset button.  

**Attention!**  
This sample program uses custom boot loaders ``revision 4`` .  
For the first time only, you need to write a custom bootloader as following.  
[How to write a custom boot loader](https://github.com/d-kato/bootloader_d_n_d)  


## Development environment
Please refer to the following.  
https://github.com/d-kato/RZ_A2M_Mbed_samples


## How to update ESP32 firmware to "AT version:1.1.3.0"
Please refer to the following.  
https://github.com/d-kato/esp32-at-ble-stack


## Known issues
It works properly only in the peripheral role. The center role does not work properly with the ESP32 FW problem.  
