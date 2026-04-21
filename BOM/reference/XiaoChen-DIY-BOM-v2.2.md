**[中文版 / Chinese](XiaoChen-DIY-BOM-v2.2_cn.md)**

# Tiny-M BOM (XiaoChen DIY V2.2)

> Source: [XiaoChen DIY (pangqc/voron-tiny-m)](https://gitee.com/pangqc/voron-tiny-m) V2.2
>
> Tutorial videos: https://www.bilibili.com/video/BV1b94y1m7Kd/

---

## 1. Hardware Procurement List

### Aluminum Extrusion

| Item | Spec | Qty | Notes |
|------|------|-----|-------|
| 2020 Extrusion | 300mm | 4 | Four vertical pillars |
| 2020 Extrusion | 260mm | 10 | Top L/R x2, middle L/R x2, bottom L/R x2, horizontal x3, X-axis x1 |
| 2020 Extrusion | 250mm | 2 | Two Z-axis |
| 2020 Extrusion | 130mm | 3 | Three for heatbed |

### Linear Rails & Carriages

| Item | Spec | Qty | Notes |
|------|------|-----|-------|
| MGN9 Rail | 200mm | 2 | Y-axis |
| MGN12 Rail | 200mm | 3 | X-axis x1, Z-axis x2 |
| MGN9H Carriage | - | 2 | Y-axis |
| MGN12H Carriage | - | 3 | X-axis x1, Z-axis x2 |

### Hotend (E3D Bowden Version)

| Item | Spec | Qty | Notes |
|------|------|-----|-------|
| E3D Bowden Hotend | - | 1 | |
| 4010 Blower Fan | - | 2 | |
| 4020 Cooling Fan | - | 1 | |
| Voron 0/0.1 Belt Clip | Rectangle | 2 | |

### Endstops

| Item | Spec | Qty | Notes |
|------|------|-----|-------|
| XY Endstop | Mechanical | 2 | |
| Z Optical Endstop | - | 1 | XiaoChen DIY mod: replaces original mechanical endstop |

### Stepper Motors

| Item | Spec | Qty | Notes |
|------|------|-----|-------|
| XY Motor | 42x47 | 2 | |
| Z Motor | NEMA 17 | 1 | |
| Extruder Motor | NEMA 17 | 1 | |
| GT2 20T Pulley | - | 3 | Mounted on motors |

### Heatbed

| Item | Spec | Qty | Notes |
|------|------|-----|-------|
| T8 Lead Screw | 220mm | 1 | |
| Spider Coupler | OD25 H30 5-to-8 | 1 | Or standard 5-to-8 coupler |
| T8 Anti-backlash Nut | POM recommended | 1 | Prefer flange without raised ridge |
| Custom Aluminum Plate | 150x150x8mm | 1 | |
| Magnetic PEI Steel Sheet | 150x150mm | 1 | |
| Silicone Heater Pad | 220V 110W | 1 | |
| Solid State Relay | DC-AC | 1 | |
| Thermal Fuse | RH 250V 15A 125C | 1 | |
| Drag Chain | 10x10 bridge type | 1m | Open or closed |
| Leveling Spring | OD10 H25 | 3 | |
| Flat Head M3x30 Screw | - | 3 | Paired with springs & thumbscrews |
| Thumbscrew Nut | - | 3 | |

### Electronics

| Item | Spec | Qty | Notes |
|------|------|-----|-------|
| Controller Board | MKS Robin E3D | 1 | |
| SBC | Orange Pi Zero2 | 1 | |
| SD Card | 16GB | 1 | |
| SD Card Reader | - | 1 | |
| LCD Display | Mini 12864 | 1 | |
| Stepper Driver | TMC2209 | 4 | |
| Power Supply | 24V 250W | 1 | |
| Buck Converter | 24V to 5V | 1 | For Orange Pi |
| Rocker Switch | With power | 1 | |
| Power-off Relay | 1-ch 5V optocoupled | 1 | |

### Misc

| Item | Spec | Qty | Notes |
|------|------|-----|-------|
| Rubber Feet | H12, OD18 | 4 | |
| AB Motor Pulley Spacer | ID5 OD10 H9 | 2 | Or print STL alternative |
| BMG Dual Gear Extruder | - | 1 | |
| GT2 Belt | 6mm width | 4m | |

---

## 2. Screws, Nuts, Washers & Bearings Summary

### Screws

| Type | Qty | Notes |
|------|-----|-------|
| SHCS M2x12 | 5 | |
| SHCS M3x8 | 81 | |
| SHCS M3x10 | 13 | |
| SHCS M3x12 | 8 | |
| SHCS M3x16 | 1 | |
| SHCS M3x20 | 4 | |
| SHCS M3x25 | 4 | |
| SHCS M3x30 | 6 | |
| SHCS M3x35 | 16 | |
| SHCS M3x45 | 2 | |
| SHCS M3x50 | 2 | |
| SHCS M5x8 | 6 | |
| SHCS M5x10 | 8 | |
| SHCS M5x14 | 2 | |
| SHCS M5x16 | 2 | |
| SHCS M5x40 | 4 | |
| BHCS M3x6 | 1 | Direct drive only |
| BHCS M3x8 | 4 | |
| BHCS M3x12 | 1 | Direct drive only |
| BHCS M3x14 | 2 | Direct drive only |
| BHCS M3x20 | 2 | |
| BHCS M3x25 | 1 | Direct drive only |
| BHCS M5x6 | 4 | |
| BHCS M5x8 | 5 | |
| BHCS M5x10 | 35 | |
| BHCS M5x12 | 2 | |
| BHCS M5x14 | 6 | |
| BHCS M5x16 | 2 | |
| BHCS M5x20 | 1 | |
| BHCS M5x30 | 4 | |
| BHCS M5x35 | 4 | |

### Nuts

| Type | Qty | Notes |
|------|-----|-------|
| M3 Spring Nut | 25 | |
| M3 Sliding Nut | 37 | Prepare 28 more for rails |
| M3x4x5 Heatset Insert | 22 | |
| M3 Hex Nut | 15 | |
| M5 Spring Nut | 16 | |
| M5 Sliding Nut | 31 | |

### Bearings

| Type | Qty | Notes |
|------|-----|-------|
| F695-2RS Flange Bearing (5mm) | 20 | |
| GT2 20T Toothed Idler (6mm belt) | 2 | |

### Washers

| Type | Qty | Notes |
|------|-----|-------|
| 5x10x1mm | 22 | |
| 5x10x0.5mm | 2 | |

---

## 3. Detailed Screw & Nut Breakdown by Assembly

### Linear Rails

| Assembly | Screw | Qty | Nut | Qty | Notes |
|----------|-------|-----|-----|-----|-------|
| MGN12 Rail (X-axis) | SHCS M3x8 | 10 | M3 Spring Nut | 5 | 20mm pitch, 200mm rail, 10 screws total |
| | | | M3 Sliding Nut | 5 | |
| MGN9 Rail (Y-axis) | SHCS M3x8 | 20 | M3 Spring Nut | 10 | |
| | | | M3 Sliding Nut | 10 | |
| MGN12 Rail (Z-axis) | SHCS M3x8 | 20 | M3 Spring Nut | 10 | |
| | | | M3 Sliding Nut | 10 | |
| MGN12 Carriage (X) | - | - | - | - | Screws listed under hotend |
| MGN9 Carriage (Y) | - | - | - | - | Screws listed under gantry |
| MGN12 Carriage (Z) | - | - | - | - | Screws listed under heatbed |

### Hotend (E3D Bowden Version)

| Assembly | Screw | Qty | Nut | Qty | Notes |
|----------|-------|-----|-----|-----|-------|
| Mount to X-carriage | SHCS M3x8 | 4 | | | |
| Belt clamp mount | SHCS M3x45 | 2 | M3 Hex Nut | 2 | |
| Belt tension | BHCS M3x8 | 2 | | | |
| Side brackets (near rail) | SHCS M3x30 | 1 | M3 Hex Nut | 1 | |
| Through side brackets | SHCS M3x50 | 2 | M3 Hex Nut | 2 | |
| 4020 Fan mount | BHCS M3x20 | 2 | Heatset M3x4x5 | 1 | |
| X endstop | SHCS M2x12 | 1 | | | |

### Gantry (Y-axis)

| Assembly | Screw | Qty | Nut/Washer/Bearing | Qty | Notes |
|----------|-------|-----|-----|-----|-------|
| MGN9 Carriage (Y) | SHCS M3x8 | 8 | | | 4 per side |
| AB Idler pulleys | BHCS M5x30 | 4 | Washer 5x10x1 | 8 | 2 screws, 4 washers per side |
| | | | Washer 5x10x0.5 | 2 | 1 per side |
| | | | F695 Bearing | 4 | 2 per side |
| | | | GT2 20T Idler | 2 | 1 per side |
| Gantry bracket | SHCS M3x20 | 2 | | | 1 per side |
| Gantry bracket | SHCS M2x12 | 2 | | | 1 per side |
| X-axis extrusion | BHCS M5x8 | 5 | M5 Sliding Nut | 5 | Left 3, right 2 |
| X-axis endstop tab | BHCS M5x20 | 1 | M5 Sliding Nut | 1 | Washer 5x10x1 x3 for height |

### AB Motors

| Assembly | Screw | Qty | Nut/Washer/Bearing | Qty | Notes |
|----------|-------|-----|-----|-----|-------|
| Through frame mount | SHCS M3x30 | 4 | M3 Hex Nut | 4 | 2 per side |
| Through frame to extrusion | SHCS M3x35 | 8 | M3 Sliding Nut | 8 | 4 per side |
| Motor mount | SHCS M3x35 | 8 | | | 4 per side |
| Idler pulley mount | BHCS M5x35 | 2 | M5 Sliding Nut | 2 | 1 per side |
| | | | Washer 5x10x1 | 4 | 2 per side |
| | | | F695 Bearing | 4 | 2 per side |
| Idler pulley mount | SHCS M5x40 | 2 | Washer 5x10x1 | 6 | 3 per side |
| | | | F695 Bearing | 8 | 4 per side |
| Y endstop | SHCS M2x12 | 2 | | | On B motor bracket |
| Top side extrusion | BHCS M5x14 | 2 | | | 1 per side |

### Front AB Belt

| Assembly | Screw | Qty | Nut/Washer/Bearing | Qty | Notes |
|----------|-------|-----|-----|-----|-------|
| Top L/R extrusion | BHCS M5x16 | 2 | | | 1 per side |
| AB Idler pulley | SHCS M5x40 | 2 | Washer 5x10x1 | 4 | 2 per side |
| | | | F695 Bearing | 4 | 2 per side |
| L/R frame | BHCS M5x35 | 2 | M5 Sliding Nut | 2 | 1 per side |

### Heatbed

| Assembly | Screw | Qty | Nut | Qty | Notes |
|----------|-------|-----|-----|-----|-------|
| Carriage mount (upper, 2 per side) | SHCS M3x10 | 4 | | | |
| Carriage mount (lower, 2 per side) | SHCS M3x12 | 4 | | | |
| Extrusion mount (1 per side) | SHCS M3x10 | 2 | M3 Sliding Nut | 2 | |
| Extrusion mount (3 per side) | SHCS M5x10 | 6 | M5 Sliding Nut | 6 | |
| Tiny logo bracket (front) | SHCS M5x10 | 2 | M5 Sliding Nut | 2 | |
| | SHCS M5x14 | 2 | | | |
| Three extrusion join | BHCS M5x10 | 2 | | | Through tapped holes |
| Z motor mount - motor | SHCS M3x25 | 4 | | | |
| Z motor mount - bracket | BHCS M5x10 | 3 | M5 Sliding Nut | 3 | |
| T8 anti-backlash nut | SHCS M3x12 | 4 | M3 Hex Nut | 4 | |
| Lead screw coupling | SHCS M5x16 | 2 | M5 Sliding Nut | 2 | Added in V1.3 |
| Drag chain (one end) | BHCS M3x10 | 2 | M3 Hex Nut | 2 | Added in V1.3 |
| Bottom extrusion jig (lower plate) | SHCS M5x8 | 2 | M5 Sliding Nut | 2 | |
| Top extrusion jig (upper plate) | SHCS M5x8 | 2 | M5 Sliding Nut | 2 | |

### Z Endstop Assembly

| Assembly | Screw | Qty | Nut | Qty | Notes |
|----------|-------|-----|-----|-----|-------|
| Optical endstop bracket | BHCS M5x10 | 2 | M5 Spring Nut | 2 | Mount to Z 250mm extrusion |
| Optical endstop switch | BHCS M3x8 | 2 | Heatset M3x4x5 | 2 | Mount to bracket |
| Heatbed L-side carriage | | | Heatset M3x4x5 | 1 | |
| Height adjustment screw | SHCS M3x20 | 1 | | | Inside knurled nut, for endstop adjustment |

### Extrusion Frame Connections

| Assembly | Screw | Qty | Nut | Qty | Notes |
|----------|-------|-----|-----|-----|-------|
| Middle L/R 260mm | BHCS M5x10 | 2 | | | 1 per extrusion |
| Heatbed 250mm vertical | BHCS M5x6 | 4 | M5 Sliding Nut | 4 | 2 per extrusion |
| Front 300mm pillars | BHCS M5x10 | 6 | | | 3 per extrusion |
| Rear 300mm pillars | BHCS M5x10 | 4 | | | 2 per extrusion |
| Bottom L/R 260mm | BHCS M5x10 | 2 | | | 1 per extrusion |
| Heatbed 130mm | BHCS M5x10 | 2 | | | 1 per extrusion |
| Drag chain (other end) | SHCS M3x8 | 2 | M3 Sliding Nut | 2 | |

### Rubber Feet

| Assembly | Screw | Qty | Notes |
|----------|-------|-----|-------|
| H12 OD20 | BHCS M5x14 | 4 | |

### Electronics Mounting

| Assembly | Screw | Qty | Nut | Qty | Notes |
|----------|-------|-----|-----|-----|-------|
| Rocker switch (on skirt) | SHCS M5x8 | 2 | M5 Spring Nut | 2 | |
| PSU bracket (to PSU) | SHCS M3x8 | 6 | | | |
| PSU bracket (to frame) | BHCS M5x12 | 2 | M5 Spring Nut | 2 | |
| | BHCS M5x10 | 2 | M5 Spring Nut | 2 | |
| Orange Pi Zero2 bracket | BHCS M5x10 | 2 | Heatset M3x4x5 | 4 | |
| | SHCS M3x10 | 4 | | | Mount SBC |
| Relay bracket (power-off) | BHCS M5x10 | 2 | M5 Spring Nut | 2 | |
| | SHCS M3x8 | 4 | Heatset M3x4x5 | 4 | |
| 24V-5V Buck Converter | BHCS M5x10 | 2 | M5 Spring Nut | 2 | |
| | SHCS M3x8 | 4 | Heatset M3x4x5 | 4 | |
| Solid State Relay | BHCS M5x10 | 2 | M5 Spring Nut | 2 | |
| | SHCS M3x8 | 2 | Heatset M3x4x5 | 2 | |
| MKS Robin E3D bracket | BHCS M5x10 | 2 | M5 Spring Nut | 2 | |
| | SHCS M3x30 | 2 | | | Upper two holes |
| | SHCS M3x8 | 1 | | | Center hole |
| | SHCS M3x20 | 1 | | | Lower-right hole |
| | SHCS M3x10 | 3 | Heatset M3x4x5 | 4 | Fan mount |
| | SHCS M3x16 | 1 | | | Fan mount |

### Sailfin Direct Drive Extruder (Add-on)

| Assembly | Screw | Qty | Nut | Qty | Notes |
|----------|-------|-----|-----|-----|-------|
| Through L/R sides | SHCS M3x35 | 2 | Heatset M3x4x5 | 2 | |
| Through L/R (belt clamp) | SHCS M3x35 | 2 | Heatset M3x4x5 | 2 | |
| Through L/R (fan mount) | SHCS M3x35 | 2 | Heatset M3x4x5 | 2 | |
| Through L/R (near carriage) | SHCS M3x35 | 1 | Heatset M3x4x5 | 1 | |
| Mount to X-carriage | SHCS M3x8 | 4 | Heatset M3x4x5 | 2 | |
| Wire tie-down | SHCS M3x8 | 2 | | | |
| Belt clamp | BHCS M3x8 | 2 | | | |
| Extruder mount | SHCS M3x10 | 2 | Heatset M3x4x5 | 2 | |
| Motor mount | BHCS M3x14 | 2 | | | |
| Through screw | BHCS M3x25 | 1 | Heatset M3x4x5 | 1 | |
| Front retention | BHCS M3x6 | 1 | Heatset M3x4x5 | 1 | |
| Filament lever knob | | | Heatset M3x4x5 | 1 | |
| Rear dual-layer clamp | BHCS M3x12 | 1 | Heatset M3x4x5 | 1 | |
| X endstop | SHCS M2x12 | 1 | | | |

---

## 4. Extrusion Tapping & Drilling

### Tapping

| Extrusion | Tapping Direction | Tap Size |
|-----------|-------------------|----------|
| Top L/R 260mm | Both ends | M5x10 |
| Four 300mm pillars | One end | M5x10 |
| | Other end | M5x8 |
| Middle L/R 260mm | Both ends | M5x10 |
| Bottom L/R 260mm | Both ends | M5x10 |
| Horizontal 260mm (x3) | Both ends | M5x10 |
| Heatbed 130mm (x2) | Both ends | M5x10 |
| Z-axis 250mm | No tapping | - |
| X-axis 260mm | No tapping | - |

### Drilling

| Extrusion | Drill Position | Hole Size |
|-----------|----------------|-----------|
| Front 300mm pillars (x2) | One end, 10mm from edge | M5 |
| | Other end, 60mm from edge (drill both horizontally and vertically) | M5 |
| Rear 300mm pillars (x2) | One end, 10mm from edge | M5 |
| | Other end, 60mm from edge (same side as other end) | M5 |
| Bottom L/R 260mm | One end, 36mm from edge | M5 |
| Middle L/R 260mm | One end, 36mm from edge | M5 |
| Z-axis 250mm | Both ends, 10mm from edge | M5 |
| Heatbed 3rd 130mm | Both ends, 40mm from edge | M5 |

---

## 5. Assembly Embedded Nuts & Jigs

### Embedded Nuts

| Nut Type | Qty | Notes |
|----------|-----|-------|
| M5 Sliding Nut | 15 | |
| M3 Sliding Nut | 8 | Rail nuts not included; recommend 28 more |

### Assembly Jigs

| Jig | Qty | Notes |
|-----|-----|-------|
| Z-axis heatbed 78.5mm positioning | 2 | Printed jig |
| Z-axis 250mm rail positioning | 2 | Printed jig |
| Rear pillars bottom 260mm positioning | 1 | Printed jig |
| Front pillars bottom 260mm positioning | 1 | Printed jig |

---

## 6. Feet & Rail Mounting Screws

| Item | Screw | Qty | Nut | Qty | Notes |
|------|-------|-----|-----|-----|-------|
| Rubber Feet | BHCS M5x14 | 4 | | | |
| Z-axis rails (x2) | SHCS M3x8 | 16 | M3 Sliding Nut | 16 | |
| X-axis rail (x1) | SHCS M3x8 | 8 | M3 Sliding Nut | 8 | |
| Y-axis rails (x2) | SHCS M3x8 | 20 | | | No nuts needed, pre-embedded |
