## General info

This firmware is for use on the SI4732 (ESP32-S3) Mini/Pocket Receiver. Based on the following sources:

- Ralph Xavier:    <https://github.com/ralphxavier/SI4735>
- PU2CLR, Ricardo: <https://github.com/pu2clr/SI4735>
- Goshante:        <https://github.com/goshante/ats20_ats_ex>
- G8PTN, Dave:     <https://github.com/G8PTN/ATS_MINI>

I also strongly recommend to take a look at this repository: <https://github.com/esp32-si4732>. It contains a lot of information about beforementioned pocket receiver and also an actively developed firmware with a lot of useful changes (which I may or may not port to my version).

This version mostly contains interface changes according to my taste.

- Frequency scale from Volos interface is back! I like it so much.
- S-meter is smaller and moved to the top.
- Battery indicator was changed.
- Brightness now is a number from 1 to 15. It maps to PWM fill values from 255/17 to 255.
- Sleep timeout can only be now up to 90 seconds. I just wanted to make it two-digit number, so it would nicely fit into menu rectangle.

## How to build

I'm using Arduino IDE.

- Add board "esp32 2.0.14" in Board Manager (there are fresh versions, but I got problems when I was trying to make them work with [TFT_eSPI](https://github.com/Xinyuan-LilyGO/T-Display-S3) library).
- TFT_eSPI should be [manually added](https://github.com/Xinyuan-LilyGO/T-Display-S3?tab=readme-ov-file#4%EF%B8%8F%E2%83%A3--arduino-ide-manual-installation) to Arduino libraries.
- Board settings I use:
    - Board: ESP32S3 Dev Module
    - CPU Frequency: 80MHz
    - Flash size: 8MB
    - Partition scheme: Default 4MB with spiffs (1.2MB APP/1.5MB SPIFFS)
    - PSRAM: Disabled

## Interface view

![interface](assets/interface.jpg?raw=true)
