---
title: Interactive Game Engine (Rust)
subtitle: A 2D game engine written in Rust exploring both game dev and systems programming
tech:
  - Python
  - Raspberry
link: https://github.com/msequino/RemoteControllerCarServer
---

## Overview

An experimental game engine built in Rust to explore low-level graphics programming, efficient event handling, and memory safety in performance-critical code. The engine supports 2D rendering, physics simulation, and extensible game logic.

## Key Features

- **ECS Architecture** - Entity Component System for flexible game object composition
- **Physics Simulation** - Rigid body dynamics with collision detection
- **WebGL Rendering** - Cross-platform graphics via web technologies
- **Event-Driven Architecture** - Decoupled systems communicate via message passing
- **Scripting Support** - Lua integration for game logic

## Technical Highlights

- Memory-safe concurrent systems using Rust's ownership model
- Zero-copy rendering with custom allocators
- Profiling-driven optimization achieving 60 FPS on target hardware
- Comprehensive benchmarking suite

## Lessons from Rust

- Ownership rules prevent entire classes of bugs
- The borrow checker feels restrictive initially but guides good design
- Performance can be exceptional when you have control over memory layout
