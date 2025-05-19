# LirOS — Customizable ESP32 Operating System

LirOS is a simple OS for your ESP32 + OLED setup. Everything is modular, so you can add or change apps fairly easy. Most features are placeholders right now—this thing is in early development. Requests, ideas, and code improvements are welcome.

## Features

- Home screen with simple navigation  
- Multiple pages and app selection  
- Built-in Settings, Clock, Calculator (more coming soon)  
- Easy to add your own apps (just make a new function and link it!)  
- Designed for a 128x64 OLED (SSD1306)  
- Button input system (up to 5 buttons supported)

## Hardware Requirements

- ESP32
- 128x64 OLED display (I2C, SSD1306)  
- 5 buttons (customizable pins in `buttonPins[]`)

## Getting Started

1. **Wire up your ESP32 + OLED + buttons** according to your pinout.
2. **Install libraries** in Arduino IDE:
   - `Adafruit_GFX`
   - `Adafruit_SSD1306`
   - `Wire`
3. **Upload the `LirOS.ino` script** to your ESP32.

## Adding Apps

Wanna make a custom app?  
- **1.** Write a new function for your app (see `settingsApp()` for an example).
- **2.** Add your app name to the `appNames[]` array.
- **3.** Add your icon to the `appIcons[]` array (or use the `comingSoonIcon` if you’re lazy).
- **4.** Increase `appsAmount` by 1.
- **5.** Call your app’s function in `appOpen()` (see how `settingsApp()` is called).

Then only program the apps function and done.
