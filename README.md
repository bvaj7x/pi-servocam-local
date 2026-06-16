# pi-servocam-local

![status: planning](https://img.shields.io/badge/status-planning-blue)
![hardware: Raspberry Pi 5](https://img.shields.io/badge/hardware-Raspberry%20Pi%205-c51a4a)
![camera: Module 2/3](https://img.shields.io/badge/camera-Module%202%2F3-2f7d32)
![network: local LAN](https://img.shields.io/badge/network-local%20LAN-455a64)

`pi-servocam-local` is a documentation-first Raspberry Pi camera project: a local LAN camera built around a Raspberry Pi 5, Raspberry Pi Camera Module 2 or 3, and a two-servo pan/tilt mount.

The goal is a small, understandable, self-hosted device that can be opened from a phone or browser on the same network. No cloud service, no public internet dependency, and no promise of production-ready camera control yet.

## Quick Links

- [Project map](docs/PROJECT_MAP.md)
- [Hardware plan](docs/HARDWARE_PLAN.md)
- [Roadmap](docs/ROADMAP.md)

## Project Map

```mermaid
flowchart LR
    User["User browser / phone"]
    UI["Local web UI"]
    Service["Raspberry Pi service"]
    Stream["Camera stream"]
    ServoController["Servo controller"]
    Pan["Pan servo"]
    Tilt["Tilt servo"]
    Mount["Camera mount"]

    User --> UI
    UI --> Service
    Service --> Stream
    Service --> ServoController
    ServoController --> Pan
    ServoController --> Tilt
    Pan --> Mount
    Tilt --> Mount
```

## Hardware Target

Initial hardware target:

- Raspberry Pi 5
- Raspberry Pi Camera Module 2 or Raspberry Pi Camera Module 3
- Two servos for pan/tilt movement
- Standard wall power supply for the first stage
- Local network access only

Planned later:

- Confirmed mounting design
- Optional enclosure
- Optional battery or power pack

## Current Status

Status: **planning / documentation-first**.

This repository is currently defining the project shape before implementation. It does not yet provide:

- A working backend service
- A working camera stream
- Servo movement
- Wiring diagrams
- Installation or startup commands

That is intentional. The first milestone is to make the project understandable before adding moving parts.

## Planned Architecture

The planned system is intentionally small:

- A Raspberry Pi 5 runs a local service.
- A browser-based UI is available only on the local network.
- The service will eventually expose a camera stream.
- The same service will eventually control pan and tilt servos.
- Servo limits and calibration will be added before any polished control experience.

The project should stay readable, local-first, and hardware-conscious as it grows.

## Local Network Model

The intended access model is:

- Device runs on a home or lab LAN.
- User opens the local web UI from a phone, tablet, or desktop browser.
- No cloud account is required.
- No public internet exposure is assumed.
- Remote access, tunneling, and WAN deployment are out of scope for the first stage.

## Safety / Hardware Notes

- Do not assume servo power can safely come directly from the Raspberry Pi 5V pin.
- Larger or stalled servos can draw more current than the Raspberry Pi should provide.
- A separate servo power supply with a shared ground is usually the safer design.
- Exact wiring will be documented only after the hardware choices are confirmed.
- Servo travel limits and calibration matter; the mount should not be driven blindly into mechanical stops.

## Roadmap

- [x] repo documentation
- [ ] hardware wiring plan
- [ ] camera bring-up
- [ ] local web UI
- [ ] pan/tilt servo control
- [ ] limits/calibration
- [ ] systemd service
- [ ] optional enclosure
- [ ] optional battery/power pack

See the full [roadmap](docs/ROADMAP.md) for phase-level planning.

## Repository Layout

```text
.
+-- README.md
`-- docs/
    +-- HARDWARE_PLAN.md
    +-- PROJECT_MAP.md
    `-- ROADMAP.md
```

## Project Note

This project starts with the README on purpose. Hardware projects are easier to build, debug, and share when the goal, constraints, and system map are visible early.

The next step is not to add a large framework. The next step is to confirm the hardware path, then bring up the camera and servos in small, testable increments.
