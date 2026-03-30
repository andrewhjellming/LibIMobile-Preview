# GUI Preview

The LibIMobile Windows GUI frontend is built with **Qt6** and grows alongside the library. Each view wires directly into the underlying C++ tier modules via a thin bridge layer — no mock data.

---

## Device Panel

The device panel shows live device info, a 3D model viewer (Qt Quick 3D + glTF), and screen mirror overlay. Models auto-fit via AABB bounding box normalization. The panel updates in real-time as values are read from the connected device via lockdown + MobileGestalt.

<div align="center">
<img src="../../Assets/Gui-Preview/Screenshot 2026-03-21 114918.png" width="820" alt="Device Panel">
</div>

---

## Filesystem Browser

Browse the on-device AFC filesystem. Navigate directories, preview files, and transfer data directly from the GUI — backed by `imobile-afc`.

<div align="center">
<img src="../../Assets/Gui-Preview/Screenshot 2026-03-21 114932.png" width="820" alt="Filesystem Browser">
</div>

---

## Instruments

Live profiling panels powered by the DTX wire protocol — CPU, memory, energy, GPU counters, network monitor, and process list. Each panel streams real data from `imobile-instruments` / `imobile-dvt`.

<div align="center">
<img src="../../Assets/Gui-Preview/Screenshot 2026-03-21 114949.png" width="820" alt="Instruments">
</div>

---

## Log Stream

Unified log stream from `imobile-syslog` — os_trace_relay on iOS 10+ and syslog relay fallback on older devices. Filter by level, subsystem, or category in real-time.

<div align="center">
<img src="../../Assets/Gui-Preview/Screenshot 2026-03-21 115015.png" width="820" alt="Log Stream">
</div>

---

## MDM / Forensics

MDM panel (profiles, DEP enrollment, supervision) and the forensics view (artifact extraction, chain-of-custody, SQLite carving, timeline analysis).

<div align="center">
<img src="../../Assets/Gui-Preview/Screenshot 2026-03-21 115023.png" width="820" alt="MDM and Forensics">
</div>

---

## Exploit / Security Panel

Jailbreak eligibility check, checkm8 exploit panel, and security audit view — showing multi-method eligibility results across the connected device's hardware configuration.

<div align="center">
<img src="../../Assets/Gui-Preview/Screenshot 2026-03-21 115031.png" width="820" alt="Exploit Panel">
</div>

---

## View Index

| View | Description | Status |
|------|-------------|--------|
| Device Panel | Live device info, 3D model, screen mirror | ✅ Wired |
| Filesystem Browser | AFC browse, transfer, preview | ✅ Wired |
| App Manager | Install, uninstall, enumerate apps | ✅ Wired |
| Log Stream | os_trace_relay + syslog relay | ✅ Wired |
| Instruments | CPU, memory, energy, GPU, network profilers | ✅ Wired |
| Backup / Restore | Encrypted backup pipeline, restore | ✅ Wired |
| MDM | Profiles, DEP, supervision panel | ✅ Wired |
| Forensics | Artifact extraction, SQLite carving, chain-of-custody | ✅ Wired |
| SQLite Browser | Query, schema, WAL inspector, diff, carver | ✅ Wired |
| Exploit | checkm8, jailbreak eligibility, security audit | ✅ Wired |
| Repair | PCB boardview, netlist, 3D teardown | 🔲 Planned |
| Screen Mirror | Live screen mirror overlay | 🟡 Partial |

---

*[← Back to README](../../README.md)*
