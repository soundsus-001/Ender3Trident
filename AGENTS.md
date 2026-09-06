# AGENTS.md

Hardware project (WIP): building a Voron Trident 3D printer, 250mm build size, with Ender-3 integration (credits yell3D Ender3Dent). No application code, no build/test/lint/typecheck commands exist — work here is docs, BOMs, and CAD/STL files.

## Layout

- `part-lists/` — project-specific parts: `Ender3Trident parts.md` (purchased parts + links) and `CSV-files/` (BOMs)
- `vorontrident250mm.csv` — 250mm BOM; byte-identical duplicate of `part-lists/CSV-files/Trident250mmBOM.csv`. Keep them in sync or consolidate.
- `Voron-Trident-Cloned-Repo/` — reference clone of upstream `VoronDesign/Voron-Trident` (STLs, Klipper firmware configs, DXFs, FreeCAD/STEP CAD, assembly manual PDF). **Untracked and gitignored** — exists only on this machine, not in the repo.

## Voron-Trident-Cloned-Repo gotchas

- It is a **nested git repo** (own `.git`, origin = VoronDesign/Voron-Trident). The outer repo no longer tracks it (gitlink removed, listed in `.gitignore`), so nothing in it is pushed with the outer repo.
- Treat it as read-only upstream reference. Project-specific changes belong in the outer repo (part-lists, README, root CSVs).
- It has local uncommitted modifications (e.g. staged deletion of `voron_trident_SB.png`). Don't commit, reset, or "sync" it without asking.

## BOM format

Semicolon-separated `Category;Description;Qty;Notes`; `Category` is only filled on the first row of each group (blank thereafter).

## Voron STL naming conventions (in the cloned repo)

- `[a]_` prefix = additional/optional part
- `_x2`, `_x3`, ... suffix = quantity
- `STLs/superseded_parts/` = deprecated versions — do not use
- Skirt parts are split by build size in `STLs/Skirt/{250,300,350}/` (top level = 250)

## Firmware

Klipper `printer.cfg` variants per controller in `Voron-Trident-Cloned-Repo/Firmware/`: `M8P/` (versioned v1.0/v1.1/v2.0), `Octopus/`, `Kraken/`, plus SKR 1.3 / SKR 1.4 EXPMOT configs at the top level.