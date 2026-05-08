# ImDuino
ImGui on Arduino example

Use the 

#  M5Stack

By default, the full screen is used with 8bpp (RGB332) color.

## Requirements

1. An M5Stack device wih configured display, such as
    - Core
    - Core2
    - CoreS3
    - Cardputer (Requires additional Cardputer library)
2. Installed M5Unified and M5GFX libraries
3. Uncomment `#define IMDUINO_M5GFX` at the top of `ImDuino.ino`


## Options
 - Change `SCREEN_COLOR` to other lgfx-defined colors. *Note: attempting to use more than 8bpp may result in a frame buffer larger than the maximum heap allocation size.*
 - Adjust `screen.createSprite( M5.Display.width(),  M5.Display.height())` to a smaller portion of the screen.
 - Enable alphablending during rasterization by changing `using ColorRaster_t = ColorDisplay_t` to a color with an alpha channel *e.g.* `color16_alpha8_t` or `color32_t`. This will more than double the frame raster time.
 - Uncomment `screen.setPsram( true )` to enable larger frame buffers. *Note: this is untested and will be slower if it works.*


# TFT_22_ILI9225 220x176 16bpp TFT

## Requirements

1. The TFT_22_ILI9225 screen and Nkawu's TFT_22_ILI9225 library
2. An Arduino with SPI (this example was designed for an
ESP32-WROOM-32 "WeMos WiFi & Bluetooth Battery")
3. Uncomment `#define IMDUINO_TFT_22_ILI9225` at the top of `ImDuino.ino`

![pinout](wifi-bluetooth/pinout.png)

## Setting up hardware

ImDuino is configured by default to use:

* Pin 32 for LED
* Pin 33 for reset
* Pin 27 for RS
* Pin 15 for CS
* Pin 14 for clock
* Pin 13 for SDI

These can be changed by modifying the following constants in `ImDuino.ino`:

```cpp
const uint8_t TFTLED = 32;
const uint8_t TFTRST = 33;
const uint8_t TFTRS  = 27;
const uint8_t TFTCS  = 15;
const uint8_t TFTCLK = 14;
const uint8_t TFTSDI = 13;
```

# SSD1306 128x64 1bpp OLED

## Requirements

1. The SSD1306 screen and Adafruit's SSD1306 library
2. An Arduino with I2C (this example was designed for an
ESP32-WROOM-32 "WiFi & Bluetooth Battery OLED")
3. Uncomment `#define IMDUINO_SSD1306` at the top of `ImDuino.ino`

![pinout](wifi-bluetooth-oled/pinout.png)

## Setting up hardware

ImDuino is configured by default to use:

* Pin 4 for SCL (Serial Clock Line)
* Pin 5 for SDA (Serial Data Line)
* No reset pin
* Address 0x3C

These can be changed by modifying the following constants in `ImDuino.ino`:

```cpp
const uint8_t OLEDSDA  = 5;
const uint8_t OLEDSCL  = 4;
const int8_t OLEDRST   = -1;
const uint8_t OLEDADDR = 0x3C;
```
