# AGENTS.md

Hardware project (WIP): building a Voron Trident 3D printer, 250mm build size, with Ender-3 integration (credits yell3D Ender3Dent). No application code, no build/test/lint/typecheck commands exist — work here is docs, BOMs, and CAD/STL files.

## Layout

- `part-lists/` — project-specific parts: `Ender3Trident parts.md` (purchased parts + links) and `CSV-files/` (BOMs)
- `vorontrident250mm.csv` — 250mm BOM; byte-identical duplicate of `part-lists/CSV-files/Trident250mmBOM.csv`. Keep them in sync or consolidate.
- `Voron-Trident-Cloned-Repo/` — vendored copy of upstream `VoronDesign/Voron-Trident` (STLs, Klipper firmware configs, DXFs, FreeCAD/STEP CAD, assembly manual PDF). Its `.git` was removed, so the files are tracked directly by this repo; there is no link to the upstream remote.

## Voron-Trident-Cloned-Repo gotchas

- It is a **vendored snapshot** of upstream (`.git` removed, no remote). To update from upstream, re-clone `VoronDesign/Voron-Trident` elsewhere and diff/replace files — do not try to `git pull` inside it.
- Treat it as read-only upstream reference. Project-specific changes belong in the outer repo (part-lists, README, root CSVs).

## BOM format

Semicolon-separated `Category;Description;Qty;Notes`; `Category` is only filled on the first row of each group (blank thereafter).

## Voron STL naming conventions (in the cloned repo)

- `[a]_` prefix = additional/optional part
- `_x2`, `_x3`, ... suffix = quantity
- `STLs/superseded_parts/` = deprecated versions — do not use
- Skirt parts are split by build size in `STLs/Skirt/{250,300,350}/` (top level = 250)

## Firmware

Klipper `printer.cfg` variants per controller in `Voron-Trident-Cloned-Repo/Firmware/`: `M8P/` (versioned v1.0/v1.1/v2.0), `Octopus/`, `Kraken/`, plus SKR 1.3 / SKR 1.4 EXPMOT configs at the top level.