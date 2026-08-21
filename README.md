# Michał Matuszewski

Embedded / IoT developer focused on practical firmware, connected devices and hardware-oriented systems.

I build projects around **ESP32-S3 / ESP32-C6, ESP-IDF, C/C++, PlatformIO, BLE, Wi-Fi, Zigbee, MQTT, sensors, PCB design and 3D printing**. I also work on supporting web interfaces and device-side tooling where it helps make embedded systems easier to configure, test and use.

## Selected projects

### [MatrixHub](https://github.com/MichalMatu/MatrixHub)
ESP32-S3 firmware and web dashboard for a connected sensor/display platform. Includes BLE scanning, Wi-Fi CSI motion sensing, USB HID, SCD41 environmental sensing, LittleFS logging, HTTPS/JWT security, notifications and a SvelteKit UI.

**Tech:** ESP32-S3 · C/C++ · PlatformIO · BLE · Wi-Fi · I²C · RMT · TinyUSB · LittleFS · SvelteKit

### [ESP32-C6 Zigbee Gateway](https://github.com/MichalMatu/esp32_c6_zigbee)
Native ESP-IDF Zigbee coordinator/gateway using the Espressif Zigbee SDK. Handles network formation and persistence, join/rejoin flows, device discovery, reporting configuration, sleepy end devices, bounded queues and normalized gateway events.

**Tech:** ESP32-C6 · ESP-IDF · C/C++ · Zigbee · ZCL/ZDO · NVS · FreeRTOS

### [ESP32-S2 USB Wi-Fi Bridge](https://github.com/MichalMatu/esp32_s2_wifi)
ESP-IDF firmware that exposes USB NCM to macOS and bridges it to Wi-Fi STA. Includes provisioning, runtime diagnostics, UART recovery console, flash coredumps, memory/stack monitoring and a TypeScript configuration UI with regression checks.

**Tech:** ESP32-S2 · ESP-IDF · C/C++ · USB NCM · TinyUSB · Wi-Fi · networking · NVS · TypeScript · CI

### [Growbox ML Controller](https://github.com/MichalMatu/growbox-ml-controller)
Production-oriented ESP32-S3/TinyML controller demo with a portable C++ control library, deterministic safety supervisor, generated C inference model, host tests, static analysis and CI-oriented build gates.

**Tech:** ESP32-S3 · ESP-IDF · C++17 · CMake/CTest · TinyML · Python · clang-tidy

### [Local Climate Link](https://github.com/MichalMatu/local-climate-link-starter)
Local climate automation without a hub: BLE thermometers feed a Shelly Plug Gen3 script that controls heating/cooling locally. Includes diagnostics, device discovery and Android release builds.

**Tech:** BLE · BTHome v2 · Shelly Script · IoT · Android

## Hardware and lower-level work

- [PCB workspace](https://github.com/MichalMatu/pcb) — code-generated schematics with SKiDL/KiCad automation, reusable hardware blocks and an ESP32 DevKitC HAT built around the AXP2101 PMIC.
- [nRF52840](https://github.com/MichalMatu/nrf52840) — PlatformIO firmware starter with a local board definition, OLED/buttons and quality tooling.
- [ESP32 Rust](https://github.com/MichalMatu/esp_rs) — `no_std` ESP32-C3 project using `esp-hal`, RISC-V, I²C sensors and quality/dependency checks.

## Private flagship project

I am also developing a larger private **ESP32-S3 automation platform** with a node-based automation engine, sensor integrations, SD-card history/archive, embedded web UI and host-side tests. The source is private, but I can discuss the architecture and implementation during a technical interview.

## Background

My background is strongly hands-on: automotive mechanics/body repair, production assembly and industrial maintenance. I have worked in environments including **Volvo, Toyota, Honda and 3M**, and I now combine that practical engineering background with embedded software and electronics.

## Currently developing

- advanced C and embedded software design
- ESP-IDF and FreeRTOS patterns
- networking fundamentals and Linux tooling
- Zigbee / BLE / IoT systems
- firmware testing, debugging and reliability

I am currently interested in **Junior Embedded Software / Firmware / IoT / Embedded Test / R&D Technician** opportunities in Wrocław, hybrid or remote.
