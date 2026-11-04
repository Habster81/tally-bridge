# Tally Bridge

### Connecting Video Switchers and Cameras

**Reliable tally indication – even in productions using equipment from different manufacturers.**

Tally Bridge is a free Windows 11 application that reads Program and Preview states from video switchers and controls the tally indicators of assigned network cameras.
Since Version 0.9.2 there is also a Linux Version availlable.

It helps camera operators immediately identify which camera is currently on air.

**Free for personal, educational and professional use.**

[**Download Tally Bridge – Official Website**](https://www.habster.ch/tally%20bridge/)

---

## Key Features

- Live monitoring of up to **16 video switcher inputs**
- Program (red) and Preview (green) status indicators
- Individual camera-to-input mapping
- Support for ATEM, TriCaster, TSL 3.1 and TSL 5
- Camera control via Sony VISCA, Canon XC and Panasonic protocols
- Camera testing without a connected video switcher
- Local diagnostic logs and test history
- Optional Primary / Secondary coordination across multiple PCs
- Standby and Relay operating modes
- Automatic fallback to a local video switcher
- Configuration import and export
- Optional Windows autostart and background operation
- Optional update checks
- Voluntary compatibility test reporting

## Mixer Configuration & Input Monitoring

![Tally Bridge – Mixer Configuration](https://www.habster.ch/wp-content/uploads/2026/10/ui-mixer.png)

Tally Bridge displays up to 16 video switcher inputs in real time.

- **Program (PGM):** Red indicator
- **Preview (PVW):** Green indicator

Each camera can be assigned to a specific mixer input.

Cameras can be individually added, enabled, edited and tested.

### Supported Video Switcher Interfaces

| Interface | Notes |
|---|---|
| Blackmagic ATEM | Requires installed ATEM Software Control |
| NewTek / Vizrt TriCaster | Optional web authentication |
| TSL 3.1 | Supported protocol adapter |
| TSL 5 | Supported protocol adapter |

### Camera Protocols

| Manufacturer | Protocol |
|---|---|
| Sony | VISCA |
| Canon | XC |
| Panasonic | Panasonic camera protocols |

**Important:** Preview indication depends on the capabilities of the individual camera model.

The presence of a protocol adapter does not mean that every compatible-looking device has been tested on physical hardware. Please consult the official compatibility information for the latest verified results.

## Camera Configuration, Testing & Diagnostics

![Tally Bridge – Camera Configuration](https://www.habster.ch/wp-content/uploads/2026/10/ui-smoke.png)

Tally Bridge provides individual camera management, testing and diagnostic functions.

A camera test can be performed without a connected video switcher.

During testing, the Program tally indicator is briefly activated before the intended operating state is restored.

Successful tests are stored locally with their date.

The diagnostic log provides information about connections and protocol communication.

### Optional Compatibility Reports

After a successful camera or mixer test, users may voluntarily submit a compatibility report.

Reports may include:

- Device model
- Firmware version
- Verified test functionality
- Separate Program and Preview results

Device IP addresses, login credentials, serial numbers and user-defined camera names are excluded from the public report.

These reports help other users evaluate equipment compatibility.

## Multi-PC Operation – Primary / Secondary

Tally Bridge supports optional coordination between multiple Windows PCs.

Instances are linked using a six-digit pairing ID.

Coordination is disabled by default and must be explicitly enabled.

Each group has exactly one designated Primary instance.

Secondary instances can operate in two different modes.

### Standby Mode

When Primary is reachable, Secondary pauses its camera control.

If Primary becomes unavailable, Secondary takes over using its own video switcher and locally configured cameras.

This enables a failover configuration.

### Relay Mode

When Primary is reachable, Secondary uses the tally input states received from Primary to control its own cameras.

If Primary becomes unavailable, Secondary automatically switches to its locally connected video switcher.

### Automatic Recovery

When Primary becomes available again, the system automatically returns to the configured coordination behavior.

A silent connection loss is typically detected after approximately three seconds. An explicit disconnection may trigger a faster takeover.

The local video switcher continues to be monitored for fallback operation.

**Important limitation:** During a network partition, both sides may become active simultaneously. The coordination mechanism does not provide an exclusive lock for cameras configured on multiple instances.

Multi-PC configurations should be tested under the actual production network conditions before use.

### Primary / Secondary Architecture

![Tally Bridge – Primary Secondary Architecture](https://www.habster.ch/wp-content/uploads/2026/10/primary-secondary-schema.png)

### Coordination Settings

![Tally Bridge – Coordination Settings](https://www.habster.ch/wp-content/uploads/2026/10/ui-peer.png)

Each instance stores its own role, pairing ID and operating mode.

## Designed for Live Production

Tally Bridge includes several features intended for ongoing production use:

- Minimize the application to the Windows system tray
- Optionally continue running after the main window is closed
- Automatically launch after Windows login
- Optionally activate the saved bridge configuration at startup
- Export and import configurations
- Check for software updates at startup

Update notifications are shown only when a newer version is available.

## System Requirements

- **Operating System:** Windows 11 since Version 0.9.2. also Ubuntu 24.04 LTS · Intel/AMD 64 Bit
- **Network:** Connectivity to the configured video switchers and cameras
- **Hardware:** Compatible video switcher and camera equipment

Please refer to the official website for additional installation requirements and device compatibility information.

## Download

**[Download Tally Bridge from Habster.ch](https://www.habster.ch/tally%20bridge/)**

The software is available free of charge for personal, educational and professional applications.

Downloads, documentation, updates and current compatibility information are provided through the official website.

## License & Source Code

Tally Bridge is proprietary software (Closed Source).

The source code is not publicly available.

This GitHub repository is intended for software information, documentation and links to the official download page.

The software is distributed under the terms provided by the publisher.

All rights reserved by the respective copyright holder.

## Support Development

Tally Bridge is provided free of charge.

Voluntary contributions through **Support my Projects** help support ongoing development and keep the software available for free.

[Visit Habster.ch](https://www.habster.ch)

---

## Deutsche Kurzbeschreibung

**Tally Bridge – Die Verbindung zwischen Videomischer und Kameras**

Tally Bridge ist eine kostenlose Windows-11-Anwendung, die den Program- und Preview-Status von Videomischern ausliest und die Tally-Leuchten zugeordneter Netzwerkkameras steuert.

Die Software unterstützt ATEM, TriCaster, TSL 3.1 und TSL 5 sowie Kameras mit Sony-VISCA-, Canon-XC- und Panasonic-Protokollen.

Bis zu 16 Mischereingänge können überwacht werden. Kameras lassen sich individuell zuordnen, konfigurieren und testen.

Für grössere Produktionen steht eine optionale Primary/Secondary-Koordination mit Standby- und Relay-Betrieb zur Verfügung.

**[Tally Bridge herunterladen und weitere Informationen](https://www.habster.ch/tally%20bridge/)**

---

**Habster Software Tools**

[Official Website](https://www.habster.ch) | [NDI Signal Stabilizer](https://github.com/Habster81/ndi-signal-stabilizer)
