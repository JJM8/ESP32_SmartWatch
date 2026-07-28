# [Agent Watch](https://github.com/JJM8/Agent-Watch)

A 3D-printed smartwatch that talks to [Uniagent](https://github.com/joshy/Uniagent) over WiFi. Hold the button, speak, and your agent responds on the screen.

## Aim

A wearable interface for Uniagent. Capture audio through an onboard mic, send it to the agent, and display the response on a 2.4-inch TFT. That's it.

## Hardware

| Component | Detail |
|-----------|--------|
| MCU | ESP32-WROOM-32E, dual-core 240 MHz, 16 MB flash |
| Display | ILI9341 TFT, 320x240 |
| Mic | I2S MEMS |
| Connectivity | WiFi 802.11 b/g/n |
| Power | LiPo battery |
| Case | 3D printed (STL included) |

## Build

```bash
git clone https://github.com/JJM8/agent-watch.git
cd agent-watch
pio run
pio run -t upload
```

## Repo

```
agent-watch/
├── images/          # Photos
├── src/main.cpp     # Firmware
├── WatchBaseMk3.stl # 3D printable case
├── platformio.ini
└── README.md
```
