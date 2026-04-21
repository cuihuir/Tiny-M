**[中文版 / Chinese](README_cn.md)**

# Tiny-M

A compact CoreXY 3D printer based on [Voron V0](https://github.com/VoronDesign/Voron-0), with a build volume of 150x150x150mm.

> **Tribute to gsl12**
>
> Tiny-M was designed and released as open source by gsl12, who made many optimizations on the Voron V0 platform. Unfortunately, due to health reasons, development stopped in August 2023. The V5 release permanently remains in beta.
>
> This repository is forked from [gsl12/Tiny-M](https://github.com/gsl12/Tiny-M) to carry on the open-source spirit, continuing maintenance and improvements.

## References

| Project | Description |
|---------|-------------|
| [gsl12/Tiny-M](https://github.com/gsl12/Tiny-M) | Original author's repo, current version V4 |
| [gsl12/Tiny-M-V5-beta](https://github.com/gsl12/Tiny-M-V5-beta) | V5 beta (unfinished) |
| [pangqc/voron-tiny-m](https://gitee.com/pangqc/voron-tiny-m) | XiaoChen DIY modified version, with complete BOM, enclosure solution, and assembly tutorials |

## About This Project

This is a replica and maintenance project with the following goals:

- Organize and update the BOM (Bill of Materials) for easier sourcing
- Reference XiaoChen DIY's modifications (optical endstop, enclosure, direct drive extruder, etc.) and optimize based on actual build experience
- Supplement and improve assembly documentation
- Continuously update improvements made during the build process

## Hardware Specifications

- Build volume: 150 x 150 x 150 mm
- Motion system: CoreXY
- Frame: 2020 aluminum extrusion
- X-axis rail: 1x 200mm MGN12H
- Y-axis rails: 2x 200mm MGN9H
- Z-axis rails: 2x 200mm MGN12H
- Stepper motors: NEMA 17
- Power supply: 24V
- Firmware: Klipper

## Extruder Options

Both Bowden and direct drive configurations are supported:

- [CroXY Sailfin](https://github.com/CroXY3D/Sailfin-Extruder) - Direct drive
- [Annex Engineering Sherpa Mini](https://github.com/Annex-Engineering/Sherpa_Mini-Extruder) - Direct drive
- [Bondtech LGX Lite](https://www.bondtech.se/product/lgx-lite-extruder-custom/) - Direct drive
- E3D V6 remote hotend - Bowden setup

## Controller Boards

- FYSETC Cheetah V1.1b (TMC2209)
- SKR Mini E3 + TMC2209
- MKS Robin E3D (XiaoChen DIY variant)

## Directory Structure

```
├── BOM/              # Bill of Materials
├── CAD/              # CAD source files
├── DXFs/             # Machining drawings
├── STLs/             # Printable STL files
├── images/           # Images
├── klipper_firmware/ # Klipper firmware config
├── slicer/           # Slicer profiles
└── usermods/         # User modifications
```

## Print Settings

Structural parts are recommended to be printed in ABS or ABS+:

- Nozzle: 0.4mm
- Extrusion width: 0.48mm
- Layer height: 0.2 - 0.3mm
- Top/bottom layers: 5
- Walls: 4
- Infill: 40% (triangular recommended)

Skirt parts can be printed in other filament types.

## XY Joint Versions

There are 3 versions of the XY joints. V4 is recommended:

- **V2** - Uses 2GT 20T pulleys (no set screw hub), requires grinding flanges to fit
- **V3** - Uses 2GT 20T toothed idlers, no M5 nuts
- **V4** - Split into 3 parts, removes one M5 screw for better alignment, optimized belt path, more rigid

## User Modifications

See the [usermods](https://github.com/gsl12/Tiny-M/tree/master/usermods) directory, including:

- Belted Z Mod
- 190mm Prusa Mini bed plate mod
- All-metal bed undercarriage
- 5mm shoulder screw mod
- 5mm dowel pin mod
- Rear cable guide
- Tophat mod

## Community

- [CroXY Discord](https://discord.gg/tmZkjWs) - Tiny-M channel
- [Mark Hoy's Build Log](https://github.com/mark-hoy/tiny-m-build)
- [XiaoChen DIY on Bilibili](https://space.bilibili.com/437455484) - Assembly video tutorials

## Acknowledgements

- **gsl12** - Original creator of Tiny-M
- **Voron Design** - Voron V0 original design
- **XiaoChen DIY (pangqc)** - Complete BOM, enclosure solution, and Chinese assembly documentation
- All Tiny-M community contributors

## License

This project follows the original repository's open source license.
