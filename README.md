# [Agent Watch](https://github.com/JJM8/Agent-Watch)

**A 3D-printed smartwatch that talks to [Uniagent](https://github.com/joshy/Uniagent) over WiFi.** Hold the button, speak, and your agent responds on the screen.

<div align="center">

| | |
|:---:|:---:|
| ![](images/watch_assembled.jpg) | ![](images/watch_enclosure.jpg) |
| ![](images/watch_display_module.jpg) | ![](images/watch_electronics.jpg) |
| ![](images/watch_running.jpg) | |

</div>

## Aim

A wearable interface for Uniagent. Capture audio through an onboard mic, send it to the agent, and display the response on a 2.4-inch TFT.

## Hardware

| Component | Detail |
|-----------|--------|
| **MCU** | ESP32-WROOM-32E, dual-core 240 MHz, 16 MB flash |
| **Display** | ILI9341 TFT, 320x240, resistive touch |
| **Mic** | I2S MEMS |
| **Connectivity** | WiFi 802.11 b/g/n, BLE |
| **Power** | LiPo battery |
| **Case** | 3D printed PLA/PETG (STL included) |

## Build

```bash
git clone https://github.com/JJM8/agent-watch.git
cd agent-watch
pio run
pio run -t upload
```


