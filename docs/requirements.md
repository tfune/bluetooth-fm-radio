# Engineering Requirements

## Project Overview

The goal of this project is to design and build a tabletop Bluetooth/FM radio using an ESP32 microcontroller, custom PCB, and 3D-printed enclosure.

The radio will have a single speaker, physical controls, and a digital display. Firmware will be written in C using ESP-IDF and FreeRTOS.

## Engineering Requirements

| ID | Requirement | Verification |
|---|---|---|
| ER-01 | The system shall receive and play Bluetooth audio from a paired smartphone at a distance of at least 5 m indoors, support automatic reconnection, and provide basic playback controls. | Pair a smartphone, test playback at 5 m, disconnect and reconnect, and verify playback controls. |
| ER-02 | The system shall receive FM radio stations from 87.9 to 107.9 MHz and support manual tuning in 0.1 MHz increments. | Tune across the supported frequency range and verify the selected frequency. |
| ER-03 | The system shall reproduce Bluetooth and FM audio through a single speaker with a target output power of at least 2 W into 4 Ω and adjustable volume. | Measure amplifier output under defined test conditions and verify volume adjustment. |
| ER-04 | The system shall switch between Bluetooth and FM modes within 2 seconds without restarting the microcontroller. | Measure the time required to switch between modes. |
| ER-05 | The system shall display the operating mode, FM frequency, Bluetooth connection status, and volume changes, with a target input response time of 100 ms or less. | Operate the controls and verify displayed information and response times. |
| ER-06 | The system shall restore the last selected mode, FM frequency, and volume after a power cycle. | Change settings, power off the system, and verify settings after restarting. |
| ER-07 | The system shall operate from an external 5 V USB supply, provide a physical power switch, initialize its user interface within 5 seconds, and operate continuously for at least 4 hours. | Verify power operation, measure startup time, and perform a 4-hour continuous operation test. |
| ER-08 | The system shall integrate its main electronic components onto a custom two-layer PCB inside a 3D-printed enclosure. | Inspect the completed PCB and assembled enclosure. |
| ER-09 | The firmware shall use FreeRTOS for concurrent operations and include register-level programming for GPIO, interrupts, and hardware timers. | Review the firmware architecture and verify the implemented peripheral functionality. |

## User Controls

Two rotary encoders will be used for the main controls.

| Control | Bluetooth Mode | FM Mode |
|---|---|---|
| Volume encoder rotation | Adjust volume | Adjust volume |
| Volume encoder press | Play/pause | Mute/unmute |
| Tuning encoder rotation | Previous/next track | Tune frequency |
| Tuning encoder press | TBD | TBD |
| Mode button | Switch to FM | Switch to Bluetooth |
| Power switch | Turn system ON/OFF | Turn system ON/OFF |

Volume will be shared between both operating modes.

## Project Constraints

- Budget: $50–$100
- Development time: 6–8 weeks
- Mono audio output
- External 5 V USB power
- Custom two-layer PCB
- 3D-printed enclosure
- Firmware written in C

## Notes

These are the initial engineering requirements and may be adjusted during component selection and prototyping.

Audio power, timing, and communication targets will need to be verified under defined test conditions.