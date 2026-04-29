# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Tiny-M is a compact CoreXY 3D printer (150x150x150mm build volume) based on Voron V0, originally designed by gsl12. This is a **fork for replica/maintenance** — not a software project. The repo contains BOM management, documentation, tooling, CAD/STL files, and Klipper firmware config.

The project is currently in **material sourcing phase**.

## Key Conventions

- **Documentation is bilingual**: English primary (`*.md`), Chinese version (`*_cn.md`). Each file cross-references its counterpart at the top.
- **BOM structure**: Active BOM lives at `BOM/BOM.md` / `BOM_cn.md`. Reference/source BOMs are in `BOM/reference/`. Do not modify reference BOMs.
- **Commits**: Use conventional commit format (`docs:`, `feat:`, `fix:`). Do NOT commit without user confirmation.
- **Language**: Respond in 中文 for communication. Technical terms and code identifiers stay in original form.

## Reference Sources

| Source | Directory |
|--------|-----------|
| gsl12 original (V4) | `BOM/reference/DRAFT-BOM-gsl12.md` |
| XiaoChen DIY V2.2 | `BOM/reference/XiaoChen-DIY-BOM-v2.2.md` |
| XiaoChen full repo | `/home/tope/project/voron-tiny-m/` |

## Tools

### `tools/jlc_reorder.py` — JLC Extrusion Model Reorder

Reorders TXCJ aluminum extrusion processing codes to 嘉立创 standard order.

```bash
# Excel mode (reads JLC型号 column, outputs new xlsx)
python3 tools/jlc_reorder.py -x input.xlsx -o output.xlsx

# CLI mode
python3 tools/jlc_reorder.py "TXCJ-H7-2020D-L300-LC-Z5-A10-DA-SC"

# Pipe mode
cat models.txt | python3 tools/jlc_reorder.py
```

Processing code order: SC → DA/LA/RA → 斜切 → 盲孔 → LC → RC → LE → RE → LBC/RBC → LBE/RBE → LK/RK → LM/RM

## Design Decisions

- **X-axis rail**: MGN12 (upgraded from gsl12's MGN9) with **extended carriages** (加长滑块) to fit E3D V6 hotend mount
- **Z-axis carriages**: MGN12H extended version
- **Z endstop**: Optical endstop (XiaoChen DIY mod, replacing original mechanical endstop)
- **Heatbed plate**: 150x150x8mm with countersunk holes (DXF at `DXFs/heatbed-aluminum-plate-v1.1.DXF`, depth 2–3.5mm)
