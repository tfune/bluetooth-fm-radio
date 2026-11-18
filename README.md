# Custom Bluetooth & FM Radio

This project is a custom tabletop radio that
combines Bluetooth audio streaming and FM radio
reception. The goal is to design and build the
radio from scratch, including the electronics,
firmware, PCB, and enclosure.

I also want to use this project to gain more
experience with embedded systems development,
particularly FreeRTOS, register-level programming,
PCB design, and audio electronics.

## Planned Features

- Bluetooth audio streaming from a smartphone
- FM radio with manual frequency tuning
- Single speaker with adjustable volume
- Rotary encoders for volume, tuning, and playback
controls
- Digital display for frequency, operating mode,
and Bluetooth status
- Physical power switch
- Saved settings after power cycling
- USB-C power input

## Hardware

Components have not been selected yet. The current plan is
to use an ESP32-based microcontroller, a dedicated FM
receiver, and a mono audio amplifier.

The electronics will be integrated onto a custom two-layer
PCB.

## Firmware

Firmware will be developed in C using ESP-IDF and
FreeRTOS.

I plan to use register-level programming for GPIO,
interrupts, and hardware timers while using ESP-IDF drivers
for more complex peripherals such as Bluetooth and I2S
audio.

## Enclosure

The radio will have a compact, modern design with a dark
enclosure, speaker grille, digital display, and two
physical knobs.

The enclosure will be designed in CAD and 3D-printed.

## Project Constraints

- Budget: $50–$100
- Timeline: 6–8 weeks
- Audio: Mono
- Power: External 5 V USB
- PCB: Custom two-layer design

## Project Status

Currently in the planning and requirements phase. The next
steps are to develop the system architecture and select
components.