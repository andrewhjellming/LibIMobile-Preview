# Module Checklist

**235 modules · 8 tiers + overlays · 111 implemented**

> ✅ Implemented — real logic written and tested
> 🟡 Partial — core compiles, some subsystems pending
> 🔲 Scaffolded — headers + CMakeLists exist, source stubs only

---

## Tier 0 — Primitives

| # | Module | Description | Status |
|---|--------|-------------|--------|
| 1 | `imobile-types` | Core types, `std::expected` error handling, `Error` enum | ✅ Done |
| 2 | `imobile-log` | spdlog wrapper, ANSI/rich module-colored output | ✅ Done |
| 3 | `imobile-async` | Boost.Asio C++20 coroutine runtime | ✅ Done |
| 4 | `imobile-plist` | Apple plist parser/writer (binary + XML) | ✅ Done |
| 5 | `imobile-crypto` | AES, RSA, ECDH, PBKDF2, SHA, HMAC via OpenSSL | ✅ Done |
| 6 | `imobile-macho` | Mach-O parser — load commands, symbols, segments | ✅ Done |
| 7 | `imobile-arm64` | ARM64 disassembler via Capstone | ✅ Done |
| 8 | `imobile-sqlite` | SQLite wrapper with async query support | ✅ Done |
| 9 | `imobile-dmg` | DMG/HFS+ parser; APFS layer partially scaffolded | 🟡 Partial |

---

## Tier 1 — Transport

| # | Module | Description | Status |
|---|--------|-------------|--------|
| 10 | `imobile-usb` | WinUSB / libusb device enumeration and I/O | ✅ Done |
| 11 | `imobile-usbmux` | usbmuxd multiplexer protocol | ✅ Done |
| 12 | `imobile-usbncm` | USB-NCM network interface | ✅ Done |
| 13 | `imobile-tcp` | Async TCP client (Boost.Asio) | ✅ Done |
| 14 | `imobile-wifi` | Wi-Fi / mDNS device discovery | ✅ Done |
| 15 | `imobile-hid` | HID device bridge (JC.id programmers) | ✅ Done |
| 16 | `imobile-i2c-bridge` | I2C bridge over USB | ✅ Done |
| 17 | `imobile-serial` | Serial port I/O | ✅ Done |
| 18 | `imobile-serial-dcsd` | DCSD diagnostic cable (Apple serial) | ✅ Done |

---

## Cross-Cutting Infrastructure

| # | Module | Description | Status |
|---|--------|-------------|--------|
| 19 | `imobile-session-pool` | One auth session per device, shared across callers | ✅ Done |
| 20 | `imobile-event-bus` | Pub/sub event system across modules | ✅ Done |
| 21 | `imobile-device-registry` | Connected device state registry | ✅ Done |
| 22 | `imobile-capability-registry` | Per-device feature capability cache | ✅ Done |
| 23 | `imobile-manifest-validator` | Module manifest schema validator | ✅ Done |
| 24 | `imobile-config` | Runtime configuration store | ✅ Done |
| 25 | `imobile-metrics` | Counters, gauges, histograms | ✅ Done |
| 26 | `imobile-tracing` | Distributed trace spans | ✅ Done |
| 27 | `imobile-auth-context` | Authentication context propagation | ✅ Done |
| 28 | `imobile-error-registry` | Centralized error code registry | ✅ Done |
| 29 | `imobile-anomaly-detection` | Anomaly detection over metric streams | ✅ Done |
| 30 | `imobile-serdes` | Serialization / deserialization helpers | ✅ Done |
| 31 | `imobile-secrets` | Secrets store (Windows DPAPI / macOS Keychain) | ✅ Done |
| 32 | `imobile-profiler` | CPU profiler integration | ✅ Done |
| 33 | `imobile-protocol-policy` | Protocol policy and version negotiation | ✅ Done |
| 34 | `imobile-jailbreak-context` | Jailbreak state context propagation | ✅ Done |
| 35 | `imobile-device-db` | SQLite-backed device history database | ✅ Done |
| 36 | `imobile-simulator` | Device simulator for offline testing | ✅ Done |

---

## Tier 2 — Protocol

| # | Module | Description | Status |
|---|--------|-------------|--------|
| 37 | `imobile-pairing` | Pairing record I/O, escrow bag, cross-platform keychain | ✅ Done |
| 38 | `imobile-lockdown` | Lockdown TLS auth, service start, get/set values | ✅ Done |
| 39 | `imobile-recovery` | DFU / Recovery mode, iBoot commands, file sender | ✅ Done |
| 40 | `imobile-rsd` | RemoteServiceDiscovery (iOS 17+) XPC manifest parse | ✅ Done |
| 41 | `imobile-tunnel` | iOS 17+ CoreDevice QUIC tunnel, XPC binary framing | ✅ Done |

---

## Tier 3 — Services

| # | Module | Description | Status |
|---|--------|-------------|--------|
| 42 | `imobile-heartbeat` | Keepalive service | ✅ Done |
| 43 | `imobile-gestalt` | MobileGestalt key queries | ✅ Done |
| 44 | `imobile-diagnostics` | Gas gauge, power source info, relay | ✅ Done |
| 45 | `imobile-notification` | NotificationProxy — subscribe/observe/post | ✅ Done |
| 46 | `imobile-syslog` | os_trace_relay (iOS 10+) + syslog relay fallback | ✅ Done |
| 47 | `imobile-afc` | AFC filesystem — read/write/mkdir/rm | ✅ Done |
| 48 | `imobile-housearrest` | House arrest service for app sandboxes | ✅ Done |
| 49 | `imobile-screenshot` | Screenshot capture (screenshotr) | ✅ Done |
| 50 | `imobile-springboard` | SpringBoard state, icons, orientation | ✅ Done |
| 51 | `imobile-apps` | App install, uninstall, enumerate, lookup | ✅ Done |
| 52 | `imobile-misagent` | Profile install / remove via misagent | ✅ Done |
| 53 | `imobile-amfi` | AMFI entitlement checks | ✅ Done |
| 54 | `imobile-companion` | Watch companion link XPC session | ✅ Done |
| 55 | `imobile-power` | Power assertions, sleep/wake | ✅ Done |
| 56 | `imobile-sync` | Media sync, playlist, contacts | ✅ Done |
| 57 | `imobile-filerelay` | FileRelay crash/log extraction (iOS ≤ 8) | ✅ Done |
| 58 | `imobile-softwareupdate` | OTA software update trigger | ✅ Done |
| 59 | `imobile-pasteboard` | Pasteboard read/write | ✅ Done |
| 60 | `imobile-axaudit` | Accessibility audit | ✅ Done |
| 61 | `imobile-nfc` | NFC tag reader / writer | ✅ Done |
| 62 | `imobile-dbi` | Developer Bridge Interface | ✅ Done |
| 63 | `imobile-kdebug` | Kernel debug trace (kdebug) stream | ✅ Done |
| 64 | `imobile-dep` | DEP enrollment check | ✅ Done |
| 65 | `imobile-bfu-afu` | BFU / AFU state detection | ✅ Done |
| 66 | `imobile-uvc` | USB Video Class mirror bridge | ✅ Done |
| 67 | `imobile-os-trace-relay` | os_trace stream relay (Unified Logging) | ✅ Done |

---

## Tier 4 — High Level

| # | Module | Description | Status |
|---|--------|-------------|--------|
| 68 | `imobile-imagemounter` | Developer disk image mount | ✅ Done |
| 69 | `imobile-devmode` | Developer mode toggle (iOS 16+) | ✅ Done |
| 70 | `imobile-symbols` | Crash symbolication, DWARF lookup | ✅ Done |
| 71 | `imobile-crash` | Crash log harvest and symbolication | ✅ Done |
| 72 | `imobile-backup` | Encrypted backup pipeline (iTunes format) | ✅ Done |
| 73 | `imobile-ipsw` | IPSW parser, component extractor | ✅ Done |
| 74 | `imobile-activation` | Device activation via Albert | ✅ Done |
| 75 | `imobile-screenmirror` | Screen mirror — screenshotr 5fps bridge | ✅ Done |
| 76 | `imobile-webinspector` | WebInspector WIR protocol | ✅ Done |
| 77 | `imobile-debug` | GDB RSP debug server proxy | ✅ Done |
| 78 | `imobile-xctest` | DTX/XCTest runner | ✅ Done |
| 79 | `imobile-dvt` | DTX wire protocol, DvtServiceHub | ✅ Done |
| 80 | `imobile-instruments` | CPU / memory / energy / GPU / network profilers | ✅ Done |
| 81 | `imobile-xcuiauto` | XCUITest gesture injection, element query | ✅ Done |
| 82 | `imobile-pcap` | Plist-framed packet capture | ✅ Done |
| 83 | `imobile-location` | GPS simulation, GPX playback, NMEA stream | ✅ Done |
| 84 | `imobile-profiles` | MCInstall profile service | ✅ Done |
| 85 | `imobile-activation-lock` | FMI / DEP activation lock check | ✅ Done |
| 86 | `imobile-reset` | Diagnostics relay — erase / shutdown / restart | ✅ Done |
| 87 | `imobile-transfer` | Facilitated transfer, batch operations | ✅ Done |
| 88 | `imobile-restore` | TSS, APTicket, NOR flash, IPSW, multi-stage restore | ✅ Done |
| 89 | `imobile-watch-bridge` | Watch companion enumeration + Bluetooth link | 🟡 Partial |
| 90 | `imobile-emulation` | Shadow Execution Engine (ARM64 via Unicorn) | 🟡 Partial |
| 91–106 | *(17 additional Tier 4 modules)* | OTA delta, FUSE mount, dyld cache, kext, fuzzer, ... | ✅ Done |

---

## Tier 5 — Exploit

| # | Module | Description | Status |
|---|--------|-------------|--------|
| 107 | `imobile-exploit` | checkm8 USB exploit engine | ✅ Done |
| 108 | `imobile-jailbreak` | Jailbreak orchestration state machine | ✅ Done |
| 109 | `imobile-kpf` | Kernel patch finder | ✅ Done |
| 110 | `imobile-pongo` | PongoOS integration | ✅ Done |
| 111 | `imobile-bootchain` | iBoot / iBSS / iBEC chain management | ✅ Done |
| 112 | `imobile-decrypt` | App decryption (FairPlay) | ✅ Done |
| 113 | `imobile-entitlements` | Entitlement injection and validation | ✅ Done |
| 114 | `imobile-img3` | img3 container parse and patch | ✅ Done |
| 115 | `imobile-img4` | img4 / IM4P / IM4M parse and patch | ✅ Done |
| 116 | `imobile-inject` | Dynamic library injection | ✅ Done |
| 117 | `imobile-keychain` | Keychain dump (jailbroken) | ✅ Done |
| 118 | `imobile-mitm` | MITM proxy for device traffic | ✅ Done |
| 119 | `imobile-nor` | NOR flash read / write | ✅ Done |
| 120 | `imobile-sandbox` | Sandbox profile parser | ✅ Done |
| 121 | `imobile-secureboot` | Secure boot chain analysis | ✅ Done |
| 122 | `imobile-security-audit` | Security posture audit | ✅ Done |
| 123 | `imobile-tls-keylog` | TLS session key logger | ✅ Done |
| 124 | `imobile-trust-cache` | Trust cache manipulation | ✅ Done |
| 125 | `imobile-app-diff` | Before/after app binary diff | 🔲 Scaffolded |
| 126 | `imobile-proto-fuzzer` | Protocol fuzzer harness | 🔲 Scaffolded |
| 127 | `imobile-sandbox-inspector` | Live sandbox introspection | 🔲 Scaffolded |

---

## Tier 6 — Vertical (Domain-Specific)

*61 modules — all scaffolded, implementation begins after Tier 5 is complete.*

| Domain | Modules |
|--------|---------|
| Messaging | `imobile-messages` (SMS/iMessage export) |
| Media | `imobile-photos`, `imobile-voice-memos` |
| Health | `imobile-health` (HealthKit DB) |
| Web | `imobile-safari` (history, bookmarks, tabs) |
| Organization | `imobile-contacts`, `imobile-calendar`, `imobile-notes`, `imobile-reminders` |
| Finance | `imobile-wallet` (passes, cards) |
| Automation | `imobile-shortcuts` |
| Home | `imobile-homekit` |
| Reading | `imobile-books` |
| Parental | `imobile-screentime` |
| Audio | `imobile-ringtones` |
| App Data | `imobile-app-data` |
| MDM | `imobile-mdm`, `imobile-dep`, `imobile-scep`, `imobile-supervision` |
| Network | `imobile-vpn`, `imobile-wifi-passwords`, `imobile-network-config` |
| Carrier | `imobile-carrier`, `imobile-sim`, `imobile-cellular`, `imobile-imei` |
| Identity | `imobile-apple-id`, `imobile-icloud`, `imobile-findmy`, `imobile-apns` |
| Hardware | `imobile-bluetooth`, `imobile-battery`, `imobile-baseband` |
| Connectivity | `imobile-carplay`, `imobile-airdrop`, `imobile-airplay`, `imobile-continuity` |
| Hardware Repair | `imobile-jcid`, `imobile-programmer-compat`, `imobile-nand`, `imobile-sep` |
| Analytics | `imobile-analytics`, `imobile-crash-reporter` |
| Misc | `imobile-ane`, `imobile-lidar`, `imobile-maps`, `imobile-uwb`, `imobile-facetime` |
| Enterprise | `imobile-kiosk`, `imobile-shared-ipad`, `imobile-zero-touch` |

---

## Tier 7 — Repair

*5 modules — scaffolded, implementation begins after Tier 6.*

| # | Module | Description | Status |
|---|--------|-------------|--------|
| — | `imobile-cad-parser` | ODB++ / GenCAD boardview format parser | 🔲 Scaffolded |
| — | `imobile-netlist` | Netlist graph construction and query | 🔲 Scaffolded |
| — | `imobile-canvas-2d` | 2D PCB canvas rendering | 🔲 Scaffolded |
| — | `imobile-scene-graph` | 3D teardown scene graph | 🔲 Scaffolded |
| — | `imobile-render-3d` | Vulkan PBR renderer for PCB / teardown | 🔲 Scaffolded |

---

## Overlays

| Component | Description | Status |
|-----------|-------------|--------|
| `LibIMobileCLI` | Unified `imobile.exe` CLI — device, backup, restore, log, fs, apps, jailbreak, instruments, MDM | ✅ Active |
| `LibIMobileGui` | Windows Qt6 GUI — device panel (3D), screen mirror, filesystem, forensics, instruments, MDM, repair | ✅ Active |
| `LibIMobileBindings` | pybind11 Python bindings with rich logging bridge | ✅ Done |
| `LibIMobileC_Api` | Flat C ABI DLL wrapper for external consumers | 🔲 Scaffolded |
| `LibIMobileAccelLayer` | CUDA GPU acceleration — backup decrypt 16×, log analysis 20×, crash batch 13× | 🔲 Scaffolded |
| `LibIMobileInstaller` | Module manifest, GPU detector, dependency resolver, profile selector | 🔲 Scaffolded |
| `LibIMobileTests` | GoogleTest integration + benchmark + fuzz target suite | 🔲 Scaffolded |
| `LibIMobileWeb` | REST API + WebSocket server + browser UI | 🔲 Scaffolded |
| `LibIMobileAutomation` | Workflow DSL, event-driven automation, scheduler | 🔲 Scaffolded |
| `LibIMobileLM` | On-device LLM inference (llama.cpp), Whisper, tool-calling agent loop | 🔲 Scaffolded |
| `LibIMobilePlugin` | Plugin registry, SDK, plugin forge, inspector | 🔲 Scaffolded |
| `LibIMobileRemote` | Multi-device cluster, remote agent, device farm | 🔲 Scaffolded |
| `LibIMobileForensics` | Evidence acquisition, chain-of-custody, timeline, SQLite carving, report engine | 🔲 Scaffolded |

---

*[← Back to README](../../README.md)*
