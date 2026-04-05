# Smart FDCAN Power Distribution Node

A high-performance Solid-State Power Controller (SSPC) designed for Industry 4.0 and defense applications, replacing traditional electromechanical relays with intelligent semiconductor switching.

## Hardware Specs
- **MCU:** STM32G474 (Arm® Cortex®-M4 @ 170MHz) with Cordic and Math Accelerators.
- **Switching:** Smart High-Side Switches (Infineon PROFET™ series) with integrated diagnostic feedback.
- **Communication:** Isolated FDCAN (Flexible Data-Rate CAN) interface.
- **Monitoring:** Multi-channel current/voltage sensing via internal 12-bit ADCs.
- **Protection:** I²t thermal modeling and ultra-fast hardware-based short-circuit shutdown.

## Architecture
- **Firmware:** Bare-metal C with STM32 HAL/LL drivers.
- **Sensing Logic:** DMA-driven ADC conversions synchronized with PWM cycles for noise-free current measurement.
- **Communication Layer:** Non-blocking FDCAN stack for real-time telemetry and remote configuration.
- **Safety:** Independent hardware watchdog and failsafe state machine.

## Disclaimer
This project is intended for educational and portfolio purposes. While designed following aerospace/industrial guidelines (IPC-2221), it is not a flight-certified or human-safety rated device.
