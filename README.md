<h1 align="center">Michał Matuszewski</h1>
<p align="center"><strong>Software · Embedded · Systems Developer</strong></p>
<p align="center"><code>C/C++</code> · <code>Python</code> · <code>TypeScript</code> · <code>Kotlin</code> · <code>Rust</code> · <code>ESP-IDF</code> · <code>Linux</code> · <code>Android</code></p>

I build practical systems across **embedded firmware, developer infrastructure, backend/web products, mobile applications, applied ML and hardware tooling**.

I am most interested in projects where software has to deal with real constraints: limited memory, hardware state, wireless protocols, process failures, unreliable networks, persistent data and long-running operation. I prefer explicit contracts, diagnostics and testable boundaries over hidden behavior.

## Engineering profile

| Area | What I work with |
| --- | --- |
| **Embedded & low-level** | ESP32-S3 / C6 / S2, ESP-IDF, PlatformIO, FreeRTOS, BLE, Zigbee, Wi-Fi, MQTT, USB, I²C, SPI, UART |
| **Systems & backend** | Python, process supervision, Git automation, SQLite, FastAPI, HTTP APIs, WebSocket, Linux/macOS services |
| **Frontend & mobile** | TypeScript, React, SvelteKit, Android, Kotlin, Jetpack Compose, Vite, Playwright |
| **Applied ML / vision** | TinyML, generated C inference, YOLO, OpenCV, MediaPipe, simulation and calibration tooling |
| **Hardware** | KiCad, SKiDL, PCB automation, sensors, displays, power-management circuits, 3D-printing workflows |
| **Quality & verification** | host tests, integration tests, static analysis, sanitizers, coverage, CI, memory/resource diagnostics, end-to-end checks |

---

## Featured engineering

### 1. [GrowClip — ESP32-S3 automation platform](https://github.com/MichalMatu/growclip)

Public showcase for my larger private ESP32-S3 firmware platform. The system combines a node-based automation runtime, sensor integrations, BLE/MQTT connectivity, microSD history/archive, an embedded web interface and a Clay-rendered device UI across multiple display targets.

The private firmware repository uses host-side Nodeflow tests, ASan/UBSan runs, coverage, static analysis, firmware architecture guardrails, memory-profile checks and load-testing tooling. The public repository exposes the product/architecture without publishing the full firmware source.

**Stack:** `ESP32-S3` · `C/C++` · `PlatformIO` · `FreeRTOS` · `BLE` · `MQTT` · `microSD` · `Clay` · `TypeScript/Svelte`

**Public showcase:** https://michalmatu.github.io/growclip/

### 2. [local-agent](https://github.com/MichalMatu/local-agent)

Deterministic local execution infrastructure for AI-assisted development. A planner defines the work; `local-agent` executes bounded tasks on the local machine and publishes machine-readable evidence of what actually happened.

The current implementation includes multi-repository scheduling, isolated workspaces, OS execution leases, process-group lifecycle management, command/no-output/RSS watchdogs, durable task claims and result spooling, crash recovery, bounded Git retry behavior, self-update safeguards and macOS `launchd` deployment.

**Engineering signals:** Linux/macOS process semantics · concurrency · durable state · failure recovery · resource limits · Git orchestration · unit/integration tests · macOS smoke tests

**Stack:** `Python` · `Git` · `subprocess/process groups` · `threads` · `file locking` · `launchd` · `GitHub Actions`

### 3. [Growbox ML Controller](https://github.com/MichalMatu/growbox-ml-controller)

ESP32-S3 controller research project combining a portable C++ control library, deterministic safety supervision, generated TinyML inference, Python model/simulation tooling and browser-based hardware/chamber configurators.

The portable controller is intentionally separated from ESP-IDF/Arduino concerns. CI verifies Python and ML tooling, portable C++ host tests, `clang-tidy`, an ESP-IDF firmware build plus `clang-check`, and the React/TypeScript frontend independently.

**Stack:** `ESP32-S3` · `ESP-IDF` · `C++17` · `CMake/CTest` · `TinyML` · `Python` · `React` · `Three.js`

**3D chamber configurator:** https://michalmatu.github.io/growbox-ml-controller/chamber-3d

### 4. [MatrixHub](https://github.com/MichalMatu/MatrixHub)

ESP32-S3 sensor/display platform that combines environmental sensing, BLE scanning, Wi-Fi CSI motion sensing, USB HID, local logging, HTTPS/JWT security, notifications and a SvelteKit control interface.

The project includes native host-test environments and coverage support, API/architecture documentation, flash coredumps and explicit PSRAM/TLS memory tuning for a resource-constrained device.

**Stack:** `ESP32-S3` · `C/C++` · `PlatformIO` · `BLE` · `Wi-Fi CSI` · `TinyUSB` · `SCD41` · `LittleFS` · `SvelteKit`

---

## Real-world products

### [IleStoi.pl / WreckScanner](https://github.com/MichalMatu/WreckScanner)

A map-based application for documenting long-standing vehicles in public space. It combines field-photo ingestion and review, SQLite-backed state, privacy-safe image derivatives, historical WMS imagery, cadastral data, PDF report generation, administration and backup/restore tooling.

The repository has separated HTTP/core layers, a broad Python test suite, frontend checks, architecture/data diagnostics, CI, smoke tests and an end-to-end `upload → review → map → PDF` flow.

**Stack:** `Python` · `SQLite` · `Leaflet` · `WMS/GIS` · `Pillow/OpenCV` · `ReportLab` · `Cloudflare Tunnel` · `Restic`

**Live:** https://ilestoi.pl

### [PhotoMap.pl](https://github.com/MichalMatu/PhotoMaps)

Visual place-discovery and editorial map platform built around a place-centric data model. The project includes a FastAPI/SQLModel backend, Alembic migrations, media/content pipelines, moderation-oriented services and a React/Leaflet frontend.

The codebase is split into API, core, database, models, schemas, serializers, services and tests. CI runs a common quality gate with backend/frontend validation and Playwright-based browser checks.

**Stack:** `Python` · `FastAPI` · `SQLModel` · `Alembic` · `React` · `TypeScript` · `Leaflet` · `Vite` · `Playwright`

**Live:** https://photomap.pl

---

## Embedded, hardware & protocol work

| Project | Focus | Main stack |
| --- | --- | --- |
| **[ESP32-C6 Zigbee Gateway](https://github.com/MichalMatu/esp32_c6_zigbee)** | Coordinator/gateway with formation, persistence, join/rejoin, discovery, reporting, sleepy-device handling and bounded runtime state | ESP32-C6 · ESP-IDF · C · Zigbee/ZCL/ZDO · FreeRTOS |
| **[ESP32-S2 USB Wi-Fi Bridge](https://github.com/MichalMatu/esp32_s2_wifi)** | USB NCM ↔ Wi-Fi bridge for macOS with provisioning, diagnostics, UART recovery and coredumps | ESP32-S2 · ESP-IDF · C · TinyUSB · networking · TypeScript |
| **[PCB workspace](https://github.com/MichalMatu/pcb)** | Code-generated schematics and KiCad automation, reusable hardware blocks and an ESP32 DevKitC HAT around the AXP2101 PMIC | Python · SKiDL · KiCad · pcbnew API |
| **[ESP32 Rust](https://github.com/MichalMatu/esp_rs)** | `no_std` RISC-V firmware with I²C sensors and Rust quality/dependency tooling | Rust · ESP32-C3 · `esp-hal` · RISC-V |
| **[nRF52840](https://github.com/MichalMatu/nrf52840)** | Nordic/PlatformIO firmware starter with a local board definition, OLED/buttons and development tooling | nRF52840 · C/C++ · PlatformIO |
| **[Raspberry Pi Zero appliance](https://github.com/MichalMatu/rp_pi2_zero)** | Headless Linux device setup, systemd hardening/boot optimization and e-paper status integration | Linux · systemd · shell · C/Python |

---

## Applied ML, computer vision & mobile

### [IPCam](https://github.com/MichalMatu/IPCam)

Real-time IP-camera monitoring and evidence recording with YOLO-based `dog` / `person` detection. The pipeline supports ROI-aware inference, configurable runtime detection profiles, adaptive idle/active detection cadence, full-frame recording and automatic MPS → CPU fallback.

**Stack:** `Python` · `OpenCV` · `YOLO/Ultralytics` · `Flask` · `MPS` · `OpenVINO` · `JavaScript`

### [BlueEye Tracker](https://github.com/MichalMatu/tracker)

Modular Android application for observing Bluetooth/BLE devices, maintaining a watchlist and presenting evidence/confidence around detections. It includes foreground scanning, Room-backed data, BLE decoder modules, Compose features and instrumented tests.

**Stack:** `Kotlin` · `Jetpack Compose` · `BLE/Bluetooth` · `Room` · `Hilt` · `Android services`

### [Gesture Inspector](https://github.com/MichalMatu/gesture_inspektor)

MediaPipe-based Android project for on-device gesture recognition and gesture-to-action mapping, with explicit lifecycle handling, bounded inference behavior, privacy-oriented offline operation and an Android quality gate in CI.

**Stack:** `Kotlin` · `Android` · `MediaPipe` · `CameraX` · `Gradle`

---

## More selected work

- **[Local Climate Link](https://github.com/MichalMatu/local-climate-link-starter)** — local BLE/BTHome thermometer → Shelly automation without a cloud service or central hub.
- **[Miauudio](https://github.com/MichalMatu/miauudio)** — Android-first ambient audio mixer built on a web/Capacitor stack with native Android media integration.
- **[Arduino MQ](https://github.com/MichalMatu/Arduino_MQ)** — ATmega328P environmental/gas-sensor project with explicit safety limitations and local display/UI.
- **[LilyGo 4.7](https://github.com/MichalMatu/LilyGo_4.7)** — ESP32-S3 e-paper/touch integration with LVGL and a separated hardware/UI structure.

---

## Development workflow

I use **AI coding agents extensively** as part of my normal development workflow. I treat them as engineering tools rather than as a substitute for verification: I define constraints and architecture, review changes, debug integration failures and validate behavior with the strongest checks that make sense for the project.

Depending on the repository, that includes:

- host/unit/integration tests and hardware smoke tests,
- compiler and static-analysis gates,
- ASan/UBSan, coverage and memory/resource diagnostics,
- schema/API/data-contract validation,
- reproducible CI builds and end-to-end flows,
- physical-device validation for firmware and hardware-facing work.

The [`local-agent`](https://github.com/MichalMatu/local-agent) project is also part of this workflow: it provides deterministic, bounded execution of agent-planned tasks across my local repositories.

## Technology map

**Languages:** `C` · `C++` · `Python` · `TypeScript/JavaScript` · `Kotlin` · `Rust`

**Embedded:** `ESP-IDF` · `PlatformIO` · `FreeRTOS` · `BLE` · `Zigbee` · `Wi-Fi` · `MQTT` · `USB/TinyUSB` · `I²C/SPI/UART`

**Software:** `FastAPI` · `SQLite/SQLModel` · `React` · `SvelteKit` · `Android/Compose` · `Linux/systemd` · `Git automation`

**ML / vision:** `TinyML` · `YOLO` · `OpenCV` · `MediaPipe` · simulation/calibration tooling

**Hardware:** `KiCad` · `SKiDL` · PCB automation · sensors · displays · power management

**Quality:** `GitHub Actions` · host tests · integration/e2e tests · `clang-tidy` · `cppcheck` · `Ruff` · sanitizers · coverage · static analysis
