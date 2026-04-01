<div align="center">

<img src="Assets/OrganizationLogo/creativ3lab-logo.png" width="88" alt="Creativ3 Lab">

```
██╗     ██╗██████╗ ██╗███╗   ███╗ ██████╗ ██████╗ ██╗██╗     ███████╗
██║     ██║██╔══██╗██║████╗ ████║██╔═══██╗██╔══██╗██║██║     ██╔════╝
██║     ██║██████╔╝██║██╔████╔██║██║   ██║██████╔╝██║██║     █████╗
██║     ██║██╔══██╗██║██║╚██╔╝██║██║   ██║██╔══██╗██║██║     ██╔══╝
███████╗██║██████╔╝██║██║ ╚═╝ ██║╚██████╔╝██████╔╝██║███████╗███████╗
╚══════╝╚═╝╚═════╝ ╚═╝╚═╝     ╚═╝ ╚═════╝ ╚═════╝ ╚═╝╚══════╝╚══════╝
```

**A ground-up C++23 reimplementation of the iOS device tooling ecosystem.**

![Status](https://img.shields.io/badge/status-pre--alpha%20v0.1.0-orange)
![Modules](https://img.shields.io/badge/modules-111%20%2F%20235%20implemented-blue)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux-lightgrey)
![Language](https://img.shields.io/badge/language-C%2B%2B23-blueviolet)
![License](https://img.shields.io/badge/license-private-red)

</div>

---

## What is LibIMobile?

LibIMobile replaces 30+ scattered legacy iOS tools with a single, modular C++23 library — **235 modules across 8 tiers**. It covers everything from low-level USB transport and lockdown authentication through backup/restore, jailbreak, hardware repair, and forensics, all under one unified API.

The source code is private. This repository is a public preview showing what's being built.

---

## Progress

| Layer | Tier | Modules | Status |
|-------|------|---------|--------|
| Primitives | 0 | 9 / 9 | ✅ Complete |
| Transport | 1 | 9 / 9 | ✅ Complete |
| Cross-Cut | — | 18 / 18 | ✅ Complete |
| Protocol | 2 | 5 / 5 | ✅ Complete |
| Services | 3 | 26 / 26 | ✅ Complete |
| High Level | 4 | 37 / 39 | ✅ Nearly complete |
| Exploit | 5 | 18 / 22 | 🟡 In progress |
| Vertical | 6 | 0 / 61 | 🔲 Scaffolded |
| Repair | 7 | 0 / 5 | 🔲 Scaffolded |
| Overlays (CLI, GUI, Bindings) | — | — | ✅ CLI + GUI active |

**111 of 235 modules fully implemented** — all core tiers (0–5) functionally complete.

---

## Highlights

- **USB + Wi-Fi device detection** — WinUSB / libusb, usbmuxd multiplexer, USB-NCM, mDNS discovery
- **Full lockdown stack** — TLS pairing, trust dialog, service start, get/set values
- **iOS 17+ CoreDevice** — QUIC tunnel, XPC binary framing, RemoteServiceDiscovery
- **Backup & Restore** — full encrypted backup pipeline, TSS/APTicket, NOR flash, IPSW
- **Instruments / DTX** — CPU, memory, energy, GPU, network profilers via DTX wire protocol
- **XCTest / XCUITest** — gesture injection, element query, screenshot comparison
- **Jailbreak (checkm8)** — DFU/iBoot chain, kernel patch finder, ramdisk injection, keychain dump
- **Forensics** — artifact extraction, SQLite carving, chain-of-custody, write-block
- **Hardware Repair** — PCB boardview (ODB++/GenCAD), netlist graph, 2D canvas, 3D teardown
- **Windows GUI** — Qt6 device panel with 3D model viewer (Qt Quick 3D / glTF), screen mirror, instruments, MDM, filesystem browser

---

## GUI Preview

The Windows GUI frontend is active and growing alongside the library.

<div align="center">
<img src="Assets/Gui-Preview/Screenshot 2026-03-21 114918.png" width="720" alt="LibIMobile GUI">
</div>

→ **[Full GUI Preview](Docs/hyperlink-pages/Gui-Preview.md)**

---

## Module Checklist

A full breakdown of all 235 modules organized by tier, with implementation status.

→ **[Module Checklist](Docs/hyperlink-pages/Module-Checklist.md)**

---

## Architecture

System architecture overview — tiers, dependency graph, overlay design.

→ **[Architecture](Docs/hyperlink-pages/Architecture.md)** *(coming soon)*

---

<div align="center">

Built by **Creativ3 Lab** · Source is private · Preview only

</div>
