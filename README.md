# [Agent Watch](https://github.com/JJM8/Agent-Watch)

A 3D-printed smartwatch that talks to [Uniagent](https://github.com/joshy/Uniagent) over WiFi. Hold the button, speak, and your agent responds on the screen.

![Assembled watch](images/watch_assembled.jpg)

## Aim

A wearable interface for your local AI agent. Voice in, response out, no cloud, no bullshit. The watch captures audio through an onboard microphone, sends it to Uniagent running on your machine, and displays the reply on a 2.4-inch TFT screen. Everything stays local.

## Hardware

| Component | Detail |
|-----------|--------|
| MCU | ESP32-WROOM-32E, dual-core 240 MHz, 16 MB flash |
| Display | ILI9341 TFT, 320x240, resistive touch |
| Mic | I2S MEMS (INMP441) |
| Connectivity | WiFi 802.11 b/g/n, BLE 4.2 |
| Power | LiPo battery, deep sleep support |
| Case | 3D printed PLA/PETG (STL included) |

## Pinout

| Peripheral | GPIO |
|------------|------|
| TFT CS | 14 |
| TFT DC | 12 |
| TFT MOSI | 27 |
| TFT SCK | 13 |
| TFT MISO | 25 |
| TFT Backlight | 10 |
| Touch CS | 3 |
| Buzzer | 7 |
| Battery ADC | 1 |
| Wake button | 2 |

## Apps

- **Home** -- 24h clock, school timetable, wifi status, battery voltage
- **Drawing** -- touch paint with 5 colours
- **Weather** -- temperature and sunset from OpenWeatherMap
- **Snooker** -- 2D physics sim with collisions

The watch connects to Uniagent for voice commands. Audio goes in, the agent processes it, and the response comes back to the screen.

## Build

```bash
git clone https://github.com/JJM8/agent-watch.git
cd agent-watch
pio run
pio run -t upload
```

Add your WiFi credentials to `src/secret.h` before flashing.

## Repo

```
agent-watch/
├── images/          # Photos of the build
├── src/main.cpp     # Firmware
├── WatchBaseMk3.stl # 3D printable case
├── platformio.ini   # Build config
└── README.md
```
