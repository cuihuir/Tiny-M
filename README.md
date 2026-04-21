<div align="center">

[English](README.md) | [中文版](README_cn.md)

# Tiny-M

A compact CoreXY 3D printer based on [Voron V0](https://github.com/VoronDesign/Voron-0)

**Build Volume** `150×150×150mm` &nbsp;|&nbsp; **Motion** `CoreXY` &nbsp;|&nbsp; **Firmware** `Klipper` &nbsp;|&nbsp; **Power** `24V`

<img src="images/tiny-m_v4.jpg" width="460">

</div>

---

> **Tribute to gsl12** — Tiny-M was designed by gsl12 with many optimizations on the Voron V0 platform. Due to health reasons, development stopped in August 2023. V5 permanently remains in beta. This repo continues the open-source spirit.

## 🛠 Build Progress

<table>
<tr><th>Phase</th><th>Status</th><th>Details</th></tr>
<tr><td>BOM & Sourcing</td><td>🔄 <strong>In Progress</strong></td><td>Frame extrusion BOM completed, 19 pcs ordered via JLC</td></tr>
<tr><td>Frame Assembly</td><td>⬜ Pending</td><td>Awaiting extrusion delivery</td></tr>
<tr><td>Motion System</td><td>⬜ Pending</td><td>Linear rails, motors, belts</td></tr>
<tr><td>Hotend & Extruder</td><td>⬜ Pending</td><td></td></tr>
<tr><td>Heatbed</td><td>⬜ Pending</td><td></td></tr>
<tr><td>Electronics</td><td>⬜ Pending</td><td></td></tr>
<tr><td>Enclosure</td><td>⬜ Pending</td><td></td></tr>
<tr><td>Software Config</td><td>⬜ Pending</td><td>Klipper setup & tuning</td></tr>
</table>

<details>
<summary><strong>📝 Recent Updates</strong></summary>

- **BOM restructured** — Converted gsl12 & XiaoChen DIY V2.2 BOMs to bilingual Markdown ([BOM/](BOM/))
- **Frame ordered** — 19 pcs of 2020 extrusion customized via JLC (TXCJ). See [BOM-Frame-JLCFA](BOM/BOM-Frame-JLCFA.md)
- **JLC tooling** — [`tools/jlc_reorder.py`](tools/jlc_reorder.py) auto-reorders processing codes to JLC format
- **Bilingual docs** — All docs in English (`*.md`) and Chinese (`*_cn.md`)

</details>

---

## 📦 References

| Project | Description |
|---------|-------------|
| [gsl12/Tiny-M](https://github.com/gsl12/Tiny-M) | Original author, V4 |
| [gsl12/Tiny-M-V5-beta](https://github.com/gsl12/Tiny-M-V5-beta) | V5 beta (unfinished) |
| [pangqc/voron-tiny-m](https://gitee.com/pangqc/voron-tiny-m) | XiaoChen DIY mod — complete BOM, enclosure, tutorials |

## ⚙️ Hardware Specs

| | |
|---|---|
| **Frame** | 2020 aluminum extrusion |
| **X-axis** | 1× MGN12H 200mm |
| **Y-axis** | 2× MGN9H 200mm |
| **Z-axis** | 2× MGN12H 200mm |
| **Motors** | NEMA 17 |

## 🔧 Extruder Options

- [CroXY Sailfin](https://github.com/CroXY3D/Sailfin-Extruder) — Direct drive
- [Annex Sherpa Mini](https://github.com/Annex-Engineering/Sherpa_Mini-Extruder) — Direct drive
- [Bondtech LGX Lite](https://www.bondtech.se/product/lgx-lite-extruder-custom/) — Direct drive
- E3D V6 Bowden hotend

## 📂 Directory Structure

```
├── BOM/              # Bill of Materials & sourcing
├── CAD/              # CAD source files
├── DXFs/             # Machining drawings
├── STLs/             # Printable parts
├── klipper_firmware/  # Klipper config
├── slicer/           # Slicer profiles
├── tools/            # Utility scripts
└── usermods/         # Community modifications
```

## 🖨 Print Settings (ABS/ABS+)

| Setting | Value |
|---------|-------|
| Nozzle | 0.4mm |
| Extrusion width | 0.48mm |
| Layer height | 0.2–0.3mm |
| Top/bottom layers | 5 |
| Walls | 4 |
| Infill | 40% (triangular) |

## 🔗 Community

- [CroXY Discord](https://discord.gg/tmZkjWs) — Tiny-M channel
- [Mark Hoy's Build Log](https://github.com/mark-hoy/tiny-m-build)
- [小辰DIY on Bilibili](https://space.bilibili.com/437455484)

## 💎 Acknowledgements

**gsl12** · **Voron Design** · **XiaoChen DIY (pangqc)** · All Tiny-M contributors

## 📄 License

This project follows the original repository's open source license.
