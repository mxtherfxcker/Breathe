# Breathe Engine

A fork of [Dreivy Engine](https://github.com/WhatIsDreivy/Dreivy_engine) with additional improvements and refinements.

## Contents
- [What is this?](#what-is-this)
- [Architecture overview](#architecture-overview)
- [Project status](#project-status)
- [Who is this for?](#who-is-this-for)
- [Build & Run](#build--run)

## What is this?

This repository is a fork of **Dreivy Engine**, a small experimental game engine written in C++.

The original project aimed to create a real game engine that is **easy to read, understand, and modify** for developers with junior or early middle C++ experience. This fork builds on that foundation, adding various enhancements and quality-of-life improvements while keeping the same core philosophy: no hidden magic, no heavy abstractions, everything explicit.

> [!NOTE]
> Some internal APIs may change as the codebase evolves.
> The focus is on clarity, learning, and experimentation rather than strict backward compatibility.

## Architecture overview

The engine is split into clearly separated layers:

ECS
→ RenderQueueBuilder
→ RenderQueue
→ Renderer

- **ECS** knows nothing about rendering
- **RenderQueueBuilder** adapts ECS data for rendering
- **RenderQueue** is a pure data contract
- **Renderer** only consumes prepared render data

> [!NOTE]
> Each layer has a single responsibility and does not depend on higher-level systems.

## Project status

This is a **learning and experimental engine** fork.

The focus remains on:
- clarity
- architecture
- correctness

Not on feature completeness or production readiness.

## Who is this for?

- Developers learning how game engines work internally
- Junior C++ programmers who want a real, readable codebase
- Engine developers who appreciate simple, explicit architecture

> [!IMPORTANT]
> If you want a huge feature set - this is not the project.
> If you want to understand how things work - it probably is.

## Build & Run

1. Clone the repository
2. Open the `.sln` file in Visual Studio 2019+
3. Build and run

No additional libraries or setup required.
