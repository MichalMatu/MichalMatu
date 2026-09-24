<h1 align="center">Michał Matuszewski</h1>
<p align="center"><strong>Software · Embedded · Systems Developer</strong></p>
<p align="center"><code>C/C++</code> · <code>Python</code> · <code>TypeScript</code> · <code>Kotlin</code> · <code>ESP-IDF</code> · <code>Android</code> · <code>Linux</code></p>

I build practical systems where software has to deal with real constraints: hardware state, limited resources, unreliable networks, long-running processes, local data, explicit authority and failure recovery.

My work spans **embedded firmware, Android, developer infrastructure, local-first products, applied ML and hardware tooling**. I prefer explicit contracts, observable state and testable boundaries over hidden behavior.

## Current flagship projects

### [AI Calls](https://github.com/MichalMatu/ai-calls)

Android research/product prototype for completing bounded real-world tasks over ordinary cellular calls on a stock Samsung phone. The system combines real call audio, local Polish STT/TTS, on-device Gemma 4 through LiteRT-LM, deterministic dialogue paths and an application-owned authorization layer for external effects.

**Engineering signal:** real-device telephony · local inference · safety/authority boundaries · Android services · STT/TTS · failure recovery

**Stack:** `Kotlin` · `Android` · `Gemma 4` · `LiteRT-LM` · `STT/TTS` · `Shizuku`

### [Local Agent](https://github.com/MichalMatu/local-agent)

Deterministic local execution infrastructure for AI-assisted development. A planner defines exact work; Local Agent executes it locally under explicit time, memory, repository and resource constraints and publishes machine-readable evidence of what actually happened.

It includes multi-repository scheduling, isolated workspaces, durable claims/results, process-group lifecycle control, watchdogs, crash recovery, repository/resource leases, Git-backed control state, emergency controls and macOS `launchd` deployment.

**Stack:** `Python` · `Git` · `process groups` · `threads` · `file locking` · `launchd` · `GitHub Actions`

### [Shelly Link](https://github.com/MichalMatu/shelly-link)

Local-first Android app for configuring a thermostat-style climate automation without a hub. The phone configures and diagnoses; a Shelly Plug S Gen3 executes the installed automation locally using BLE thermometer data, so the default path does not require Home Assistant, MQTT, cloud services or a 24/7 server.

The project has a verified real-hardware path, published Android beta builds and an accepted UX baseline.

**Stack:** `Kotlin` · `Android` · `Shelly RPC/Scripts` · `BLE/BTHome` · `local-first automation`

**Project page:** https://michalmatu.github.io/shelly-link/

### [BloomML](https://github.com/MichalMatu/bloomml)

Native ESP-IDF growbox controller for ESP32-S3 with deterministic climate control, real sensors, RF433 outputs, durable telemetry, e-ink operator UI and TinyML research tooling.

Production control remains deterministic and safety-owned; ML is deliberately kept in a shadow/research role. The firmware includes a native SSD1680 display path, Clay-rendered operator pages, host-side C++ tests and hardware-focused verification flows.

**Stack:** `ESP32-S3` · `ESP-IDF` · `C++17/20` · `FreeRTOS` · `SCD41` · `RF433` · `e-ink` · `TinyML`

### [GrowClip](https://github.com/MichalMatu/growclip-site)

Public showcase for my larger private ESP32-S3 automation platform. GrowClip combines a node-based automation runtime, sensor integrations, BLE/MQTT connectivity, persistent history/archive, an embedded web interface and device-side UI across constrained display targets.

The full firmware/runtime stays private; the public repository contains the marketing site, product mockups and a standalone LiteGraph demo.

**Stack:** `ESP32-S3` · `C/C++` · `FreeRTOS` · `BLE` · `MQTT` · `microSD` · `Clay` · `SvelteKit`

**Live:** https://michalmatu.github.io/growclip-site/

---

## Strong public projects

| Project | Focus | Main stack |
| --- | --- | --- |
| **[BlueEye Tracker](https://github.com/MichalMatu/tracker)** | Local-first Bluetooth/BLE situational-awareness app with explainable evidence, bounded ingest, Room persistence and field-tested Android scanning | Kotlin · Jetpack Compose · BLE/Bluetooth · Room · Hilt |
| **[MatrixHub](https://github.com/MichalMatu/MatrixHub)** | ESP32-S3 sensor/display platform with SCD41, BLE, Wi-Fi CSI motion sensing, USB HID, notifications, Shelly integration and embedded web UI | ESP32-S3 · C/C++ · PlatformIO · TinyUSB · SvelteKit |
| **[Miauudio](https://github.com/MichalMatu/miauudio)** | Android-first ambient audio mixer with native Media3 background playback, imported audio, procedural generators, PWA/web target and release tooling | TypeScript · React · Capacitor · Kotlin · Media3 |
| **[PhotoMap](https://github.com/MichalMatu/photomap)** | Place-centric visual map platform with editorial media pipeline, moderation, FastAPI backend and React/Leaflet frontend | Python · FastAPI · SQLModel · React · TypeScript · Leaflet |

---

## Hardware, experiments and maintained work

- **[Hardware Lab](https://github.com/MichalMatu/hardware-lab)** — consolidated firmware starters, board bring-up, ESP32-S2 USB networking, ESP32-C6/Zigbee experiments, Rust/ESP32, nRF52840, Raspberry Pi, e-paper, PCB/SKiDL/KiCad work and computer-vision experiments.
- **[IleStoi.pl](https://github.com/MichalMatu/ilestoi)** — maintained map application for documenting long-standing vehicles in public space; now intentionally a low-priority maintenance project. Live: https://ilestoi.pl
- **[Gesture Inspector](https://github.com/MichalMatu/gesture_inspektor)** — on-device MediaPipe gesture-recognition Android project.

---

## Engineering profile

| Area | What I work with |
| --- | --- |
| **Embedded & low-level** | ESP32-S3 / C6 / S2, ESP-IDF, PlatformIO, FreeRTOS, BLE, Zigbee, Wi-Fi, MQTT, USB, I²C, SPI, UART |
| **Systems & backend** | Python, process supervision, Git automation, SQLite, FastAPI, HTTP APIs, WebSocket, Linux/macOS services |
| **Android & frontend** | Kotlin, Jetpack Compose, TypeScript, React, SvelteKit, Vite, Playwright |
| **Applied ML / vision** | on-device LLM inference, TinyML, YOLO, OpenCV, MediaPipe, simulation and calibration tooling |
| **Hardware** | KiCad, SKiDL, PCB automation, sensors, displays, power-management circuits, 3D-printing workflows |
| **Verification** | host/integration tests, hardware smoke tests, static analysis, sanitizers, coverage, CI and resource diagnostics |

## Development workflow

I use AI coding agents extensively, but keep execution and verification explicit. I define constraints and architecture, review changes, debug integration failures and validate behavior with the strongest checks appropriate for each project.

Depending on the repository, that includes host/unit/integration tests, physical-device validation, compiler/static-analysis gates, ASan/UBSan, coverage, memory/resource diagnostics, schema/API validation, reproducible CI builds and end-to-end flows.

[`Local Agent`](https://github.com/MichalMatu/local-agent) is part of that workflow: it gives AI-planned work a deterministic, bounded and auditable execution layer across my local repositories.
