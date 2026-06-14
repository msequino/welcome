---
title: Remote Controller Car Server
subtitle: Lightweight Bluetooth RFCOMM server for remote-controlled car control
tech:
  - Python
  - Bluetooth
  - Raspberry Pi
link: https://github.com/msequino/RemoteControllerCarServer
---

## Overview

A compact, modular Python service that listens for Bluetooth RFCOMM connections and translates simple semicolon-delimited command strings into GPIO actions for a remote-controlled car. The project is intentionally minimal so it can be extended with real hardware drivers and security features.

## Key Features

- **Bluetooth RFCOMM server** — advertises a service UUID and accepts a single RFCOMM connection on port 1.
- **Simple message protocol** — semicolon-delimited UTF-8 strings for commands: `throttle`, `reverse`, `steer`, `slowdown`.
- **Command parsing & dispatch** — `MessagePayload` builder maps messages to action classes which invoke the GPIO interface.
- **GPIO abstraction** — `Gpio` methods (`throttle`, `reverse`, `steer`, `slowdown`) keep hardware control isolated and replaceable.
- **Convenience startup script** — `start-server.sh` ensures the Bluetooth adapter is discoverable and launches the server.

## Technical Highlights

- Minimal, synchronous server loop using Python and the `pybluez`-style Bluetooth API.
- Clean separation of concerns: networking (`main.py`), message/model (`model.py`), hardware interface (`gpio.py`).
- Lightweight protocol with predictable parsing: `command;param1;param2;timestamp`.
- Easy to replace stubbed GPIO calls with `RPi.GPIO`, `gpiozero`, or a hardware-specific driver.

## Lessons & Notes

- Keep network parsing defensive — validate message length and formats before acting on hardware.
- For production use on a Raspberry Pi, run hardware control as a non-root service with restricted capabilities and add authentication.
- Single-connection design is simple but limited; consider using threading/asyncio for multiple clients or a command queue with rate-limiting.
