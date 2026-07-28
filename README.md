# NoiseGuardian — Case Study

> **iOS app** · Source remains **private** · This page is a public product / engineering summary only.

## Problem

Phone users want a lightweight way to **watch environmental loudness trends** — live levels, short history, and alerts when things get too loud — without claiming to be a certified sound level meter.

## Product

**NoiseGuardian** is a SwiftUI + AVFoundation app for **real-time approximate noise monitoring**:

- Live **dB (approx.)** readout from microphone RMS (+ optional calibration offset)
- Scrolling ~30s trend graph (~10 Hz samples)
- Short-window stats (~1s / ~3s means, max/min)
- **Peak** and **sustained** alerts with cooldown (User Defaults thresholds)
- Save sessions to **Core Data** history with optional names
- Calibration offset / presets; background audio capability for continued analysis when OS allows

**Disclaimer:** Values are approximate loudness trends for awareness — **not** A-weighted SPL, LAeq, or legal/occupational compliance measurements.

## Stack

`Swift` · `SwiftUI` · `AVFoundation` · `Core Data` · iOS 18.5+

## Engineering highlights

- RMS tap on mono PCM → UI buffer capped for stable memory
- Main-actor UI updates; privacy manifest for App Store disclosure
- Alert model: peak threshold, sustained hold duration, inter-alert cooldown

## Source

Implementation stays in a **private** repository. This showcase contains **no source code** — portfolio narrative only.
