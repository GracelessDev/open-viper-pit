# Open Viper Pit

An open-source F-16C home cockpit, built for the highest fidelity a small space and a limited budget allow.

> **Status:** early design. The ICP + DED is the first panel in progress. Expect things to change.

## Goals

- **Real behaviour, not just real looks.** Switches act like the jet's: magnetically held switches release when the sim says they should, spring-loaded positions return, and lit buttons reflect the cockpit's state.
- **Real, independent displays.** Each display gets its own physical screen: the DED, both MFDs, the RWR and so on. No single monitor cut into pieces.
- **Faithful where it counts.** Layout, feel and function come first. Where space or budget forces a compromise, it's documented.
- **Buildable on a budget.** Common, sourceable parts, 3D-printed structure, and hand-wiring friendly designs.
- **Modular.** Each panel group runs on its own microcontroller and connects through a powered USB hub, with a single USB-C connection to the PC.

## Sim support

- **DCS World** (F-16C Block 50) via [DCS-BIOS](https://github.com/DCS-Skunkworks/dcs-bios)
- **Falcon BMS** support planned

## Panels

| Panel | Status |
| --- | --- |
| ICP + DED | In design |
| MISC panel (Master Arm, Laser Arm, RF, Autopilot) | Planned |
| Left aux console (landing gear) | Planned |
| MFDs | Planned |
| RWR | Planned |
| TWA / ECM | Planned |

## Repository layout

```
cad/        FreeCAD source files
  common/   reference models shared by all panels (switches, boards, displays)
  icp/      one folder per panel
stl/        printable exports, per panel
firmware/   microcontroller code, per panel
docs/       build notes, wiring and parts lists
```

## Hardware basics

- **Microcontrollers:** ESP32-S3 (native USB) for larger panels, classic ESP32 for smaller ones
- **Keys:** MX-style tactile switches with printed caps
- **Toggles:** Dailywell 1M-series miniature toggles
- **Encoders:** Bourns PEC11R
- **Displays:** SSD1322 256×64 OLED for the DED

Full parts lists will live in each panel's `docs/` folder.

## Licence

To be decided. The plan is an open hardware licence for the designs and an open-source licence for the firmware.

## Disclaimer

This is an independent hobby project. It is not affiliated with or endorsed by Lockheed Martin, Eagle Dynamics, Benchmark Sims, or any other cockpit project.

---

Maintained by **GracelessDev**.
