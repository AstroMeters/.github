---
layout: page
title: AMASC01 Circle Buffer Capture
subtitle: 'AMASC01: Circle Buffer Capture'
description: 'AMASC01 circle buffer capture – high-frame-rate event recording with CircularPiCam, RAM buffering, and multi-source triggers.'
keywords: 'AMASC01 circle buffer, CircularPiCam, high frame rate capture, pre-trigger recording, global shutter, IMX296, event capture'
menubar: docs_menu
show_sidebar: false
toc: false
nav_order: 5
hero_image: '/images/products/AMASC01/amasc01_hero.jpg'
---

# AMASC01 Circle Buffer Capture

The **Circle Buffer Capture** mode is intended for situations where the priority is not continuous all-night imaging, but capturing very fast transient events at the highest frame rate the camera can reliably deliver.

This software is based on **CircularPiCam**, a capture pipeline designed for high-speed event recording with RAM-based circular buffering and trigger-controlled clip saving.

## Purpose

This mode has the opposite design goal compared to the standard [Base Software Stack](/docs/AMASC01/base-software-stack/), which is built around continuous all-sky monitoring, long-term operation, and regular image generation.

Circle Buffer Capture focuses instead on:

- **maximum frame rate**
- **short-event recording**
- **pre-trigger and post-trigger history**
- **fast trigger response**

This makes it suitable for phenomena that happen too quickly for standard periodic all-sky imaging.

> **Note:** This software was originally developed specifically for the [**AMASC01** platform](/products/AMASC01/) and for monitoring the development of **bolides** and other very fast luminous events in the sky. At the same time, it is designed as a more universal capture system and can also be used with optics with a **narrower field of view**, with other camera configurations, or in application-specific trigger and recording setups. For more information about suitable configurations or possible adaptations, please do not hesitate to contact us for consultation.

## Sensor Options

On request, the AMASC01 can be equipped with a **Sony IMX296** sensor in either:

- **monochrome** variant
- **color** variant

The Sony IMX296 uses a **global shutter** and supports frame rates of up to **60 FPS**, which is important for capturing very fast events without rolling-shutter distortion.

## Circular Buffer Principle

The software continuously stores recent image data in a **RAM-based circular buffer**. This means the system always keeps the most recent seconds of recording in memory, even before any trigger occurs.

When a trigger is received, the software saves:

- several seconds **before** the trigger
- the trigger moment itself
- several seconds **after** the trigger

This allows the user to record not only the event, but also what happened immediately before it.

## Trigger Options

Several trigger methods can be used depending on the application:

- **WebSocket trigger**
- **light-change trigger**
- **keyboard trigger**
- **GPIO signal trigger**

These trigger modes allow the camera to react to external systems, sudden scene changes, or direct operator input.

## Typical Use Cases

Circle Buffer Capture is useful for events that are brief, unpredictable, or scientifically interesting only when the full pre-event context is preserved.

Example use cases include:

- **meteor and bolide events** where the trajectory onset is important
- **lightning and transient atmospheric discharges**
- **sudden optical flashes** or short luminous phenomena
- **laboratory or field experiments** synchronized by GPIO trigger
- **external instrument correlation**, where another detector triggers optical recording
- **diagnostics of fast mechanical or environmental events**, where the state before the trigger matters

In all of these scenarios, the ability to preserve frames from before the event is often more valuable than continuous low-rate imaging.

## Open-Source Availability

> **Note:** This software is also **open-source**. If you are interested in this capture mode or want to discuss a custom configuration, please use the contact information in the [About](/about/) section.
