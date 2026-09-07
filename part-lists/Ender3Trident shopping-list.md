# Ender3Trident Shopping List — DRAFT v3 (budget, review before merging into parts.md)

> **AI-edited:** This file was researched, drafted, and edited with AI assistance. Verify all prices, stock, and compatibility details before ordering.
>
> Sourcing research, prices checked 2026-09-06. Amazon-first where cheaper, West3D for Voron-specifics.
> Build: **Trident R2, 250mm, blind joints, Octopus Pro V1.1 + BTT Pi V1.2**, following the [Ender3dent](https://github.com/yell3D/Ender3dent) approach (maximize Ender 3 reuse).
> Prices are **padded estimates** (base + ~$5, rounded up) to cover tax/shipping/price drift unless noted. Base prices in Notes.
> **Quality policy:** electronics (Octopus Pro, Raspberry Pi, probe) must be **genuine** — no cheap/clone compatibles; if a part is listed as incompatible it's off the table. Everything else is lean but still **reputable-brand** (no no-name knockoffs).
> **Budget target: as cheap as possible while keeping quality — core ≈ $805; ~$755–770 with trims. Stealthburner + Dragon + CW2 gear set + NEMA14 pancake = classic SB/CW2, max accel, no mods. Runner-up if you ever want −$25: reuse a NEMA17 via a spacer mod (printables 950092).**
> Companion files: `Ender3Trident parts.md` (purchased) · `CSV-files/Ender3Trident have-vs-need.csv` (gap analysis)

## REUSE from 2× Ender 3 (NOT on buy list — per Ender3dent README)

| Ender3dent "can reuse" | What you have (2× Ender 3) | Replaces BOM line |
|---|---|---|
| Steppers (yes) | ~10× NEMA17 total: ~3 each from 2× Ender 3 + 4 extra. **Need 5 (A/X, B/Y, Z, Z1, Z2)** → plenty, ~5 spares. **(E-drive = bought NEMA14 pancake in the Toolhead section — not one of the NEMA17s.)** | 2× NEMA17 17HS19-2004S + 3× TR8x4 linear steppers |
| Leadscrew + 2nd leadscrew (yes) | 2× T8x8 leadscrews (365mm, 4-start) | 3× TR8x4 300mm linear steppers (buy 1 more leadscrew, see below) |
| Stock leadscrew coupler (yes, better than spring ones) | 2× Z couplers (D5*8) | buy 1 more coupler |
| Bed heater (yes) | 2× 235x235 220W hotbeds | Keenovo heater / LDO build plate kit |
| Flexplate (yes) | 2× 235x235 fiberboard | PEI sheet + 3M 468MP (add thin PEI/3M on top, see below) |
| Power Supply (yes, even the fat one) | 2× 24V 15A PSU | Mean Well LRS-200-24 |
| AC Inlet + Switch (yes, check voron mods) | 2× power inlet + 10A switch | Tyco 10EGG1-2 + ZF rocker (**verify** — Ender 3 inlet is unfiltered, switch is 10A not 16A) |
| Cables (yes, except toolhead wiring) | motor/power/bed harnesses | most of the wire/connector budget (toolhead wiring still new) |
| Display (yes, monochrome) | 2× 1284P (128x64) | Mini 12864 (**verify** pinout vs Octopus display port) |
| ~~Custom Extruder~~ **NO — now a BUY** | 2× Ender 3 extruders (E motor + gear + housing) | BMG kit + NEMA14 motor → **bought: CW2 gear set + NEMA14 pancake motor (Toolhead section). Ender 3 E-motor NOT reused.** |
| ~~Custom Hotend~~ **NO — now a BUY** | 2× Ender 3 hotends (heat block + nozzle + heater + catheter) | E3D V6 kit → **bought: Phaetus Dragon UHF (Toolhead section). Ender 3 hotend NOT reused.** |
| 40x40x10 fans | 6× 4010 24V fans | 40x40x10 axial fan |
| GT2 20T pulleys | 4× 2GT-d5-20-6mm | 3× GT2 20T pulleys |
| Rubber foot pads | 8× 20x40x3mm pads | 4× Rubber Foot (**verify** fit/flatness) |
| Creality mainboard (yes, as secondary MCU) | 2× 1284P mainboards | optional — NOT needed if Octopus Pro drives all 6 steppers + bed heater directly |

**Already purchased (see parts.md):** LDO frame kit 250mm, DIN rails 35mm, MGN9H 300 ×5, MGN12H 300 ×1.

## BUY — Core (≈ $805; ~$755 trimmed; see totals)

### Printed Parts (functional kit = buy; cosmetics = self-print PLA)

| Qty | Part | Est. $ | Source | Link | Notes |
|---|---|---|---|---|---|
| 1 set | Voron Trident functional ABS printed parts kit | 145 | West3D | https://west3d.com/products/printed-parts-for-voron-trident | $139.99 base (verified 9/6). Prints the **PIF "functional" kit scope** but is **explicitly NOT PIF-affiliated** (page says so). Made-to-order: ~5 bd — up to 3 wks. **Consolidates with your main West3D order, BUT excluded from free shipping** (separate big box; flat rate, page: "usually less than what we pay"). **At order time you must pick color + board + hotend BEFORE adding to cart** + use the special-instructions field. **Form picks: Toolhead = Stealthburner, Hotend = Dragon, Controller = Octopus** (standard, no Custom needed). Reviews (8): 4×5★ / 1×4★ / 2×2★ / 1×1★ — gripes = warped A/B-drives/idlers/XY-joints (vendor: pulled off plate before cool; now reprinted w/ extended cooling), some **missing functional parts** (incl. CW cable cover w/ thermistor mount) → **check EVERY bag against the PIF BOM on arrival**; vendor replaces/corrects free, incl. during-build issues. Cancellation/refund only pre-print (or >3 wks delay). **Alt (higher QC guarantee, slower):** Fabreeko PIF $139.99 (https://www.fabreeko.com/products/voron-trident-printed-parts-by-pif). Also: 3D Pros $139.99 (https://3dpros.online/products/voron-trident-printed-parts-kits), KB-3D/Bounty3D $149.99 (https://kb-3d.com/store/v1-trident/551-voron-trident-printed-parts-kit-configurable). Note: West3D **Labor Day sale 9/5–9/7 live now** — batch your West3D order this weekend. |
| 1 set | Cosmetics: skirts, panel clips, display mount, covers — **self-print in PLA** | 0 | self-print | cloned repo `STLs/Skirt/250/` (or upstream Voron-Trident GitHub) | **PLA is fine here** — these are cosmetic, non-load-bearing, away from heat, and PLA is trivially easy on your Ender 3. **Only caveat:** if you later enclose + print ABS/ASA, a heated enclosure softens PLA (~60°C glass transition) → reprint cosmetics in PETG/ASA then. Most pieces fit your 235×235 bed; the few longer skirt/hat panels can be printed later on the new printer (or split). Never substitute PLA for anything in the functional kit. |
| 1 set | Ender3dent mod parts (spacer standoffs, etc.) | handled | — | https://www.printables.com/model/644553 · https://www.printables.com/model/1255726 | Small PLA/PETG prints for the mods — printable on your Ender 3 (they're small, <235mm). |

### Fasteners

| Qty | Part | Est. $ | Source | Link | Notes |
|---|---|---|---|---|---|
| 1 kit | West3D Stainless Fastener Kit for Voron Trident (BDF) | 70 | West3D | https://west3d.com/products/west3d-stainless-steel-fastener-kit-for-voron-trident-bdf | $69.99 base — **keep this one.** "R2 UPGRADED AS OF 6/17/2026" — covers all 26 R2 BOM lines with surplus, ships roll-in T-nuts. Quality 304 stainless + brass inserts. Ender 3 screws are only "maybe" reusable, and the BDF kit is the reliable, complete choice. |

### Motion (~$90)

| Qty | Part | Est. $ | Source | Link | Notes |
|---|---|---|---|---|---|
| 2 | GT2 20T Toothed Idler (5mm ID 6mm W) | 10 | West3D | https://west3d.com/products/black-pulleys-and-idlers-gt2-20t-gt2-16t | $1.79 ea base. |
| 26 | F695-2RS Bearing (5x13x4mm flanged) | 20 | Amazon | https://www.amazon.com/dp/B0D1VV8WQF | ~$13/20pk base — **reputable brand (uxcell / KABOBEARING ABEC-9 / Harfington)**, not generic. Buy 2× 20pk (40ct) for ~$26, only ~26 needed. Cheaper than West3D's $0.99 ea. (Your 52× 625ZZ are 1mm smaller OD — not interchangeable.) |
| 3 | GE5C Spherical Bearing | 15 | West3D | https://west3d.com/products/ge5c-spherical-bearing-nsk | $2.99 ea base. Needed for the Trident Z gimbal. |
| 1 | 5x30mm Shaft | 5 | West3D | https://west3d.com/products/round-shafts-5x30mm-5x60mm | $0.49 base. |
| 2 | GT2 Open Belt 6mm, 1690mm each | 20 | West3D | https://west3d.com/products/gates-gt2-open-belt-ll-2gt-6-6mm-wide-voron-v0-v1-v2-switchwire | $0.49/100mm, order 17 per belt. Ender 3 belts (786/743mm) too short even spliced. |
| 1 | T8x8 Leadscrew 365mm (3rd Z column) | 10 | Amazon | https://www.amazon.com/s?k=T8x8+leadscrew+365mm+3D+printer | ~$8 base. Reuse 2× Ender 3 T8x8 leadscrews (365mm, 4-start) for the other 2 columns. |
| 1 | T8x8 Coupler D5*8 (3rd Z column) | 5 | Amazon | https://www.amazon.com/s?k=T8x8+coupler+5mm+3D+printer | ~$4 base. Reuse 2× Ender 3 Z couplers. Print spacer standoffs (Ender3dent mod 644553 / printables 1255726) so reusing the coupler doesn't lose Z height. |
| 1 | T8x8 Nut (brass, 22mm flange, 4× M3 holes) | 5 | Amazon | https://www.amazon.com/s?k=T8x8+brass+nut+22mm+flange | ~$3 base. **Must be 4-start (matches your T8x8 rod), NOT the BOM's TR8x4.** Same 22mm flange / 4-hole form as the Trident z_bed pocket — the Ender 3 nuts you reuse have the identical body, so they drop in too. This 3rd nut is the one extra. |

### Electronics (~$215)

| Qty | Part | Est. $ | Source | Link | Notes |
|---|---|---|---|---|---|
| 1 | **BTT Octopus Pro V1.1 (H723) + BTT Pi V1.2 + 7× drivers bundle** | 140 | Amazon | https://www.amazon.com/dp/B0CL6J66M4 | $139.99 base — **genuine BTT sold by BIGTREETECH via Amazon**. ONE order replaces three lines: Octopus Pro board + host computer + stepper drivers (~$155 à la carte → ~$140). Board = **V1.1 H723 (550MHz, 512KB flash)** — newer/faster than the V1.0 F446; **on-board MAX31865 PT100**, CAN, 6 controllable fans. **Host = BTT Pi V1.2 (Allwinner H616 quad-A53 1.5GHz, 1GB, 2.4G WiFi)** — first-party BTT, Klipper-ready; **NOT a genuine Raspberry Pi** (accepted tradeoff to stay under budget). Drivers = **5× TMC2209 + 2× TMC5160T** (7 total, 6 needed: A-B-Z-Z1-Z2-E). Title says 5×2209 but item details say 6×2209 — **count drivers on arrival**. Assign the TMC5160Ts to X/Y or Z and note their drive config differs from the silent 2209s. |
| 1 | Omron TL-Q5MC2-Z NPN NC inductive probe (self-leveling) | 20 | West3D | https://west3d.com/products/omron-tl-q5m-inductive-probe | $14.99 base, in stock — **genuine Omron**. |
| 3 | 60x60x20 Axial Fan 24V | 25 | West3D | https://west3d.com/products/gdstime-dc-24v-60x60x20-axial-fan-gda6020-dual-ball-bearing-5000rpm-1-7w-0-1a-xh2-54 | $6.99 ea base. Electronics bay. |
| 1 | Mean Well RS-25-5 (5V) | 15 | West3D | https://west3d.com/products/mean-well-rs-25-5-25w-5v-5a-power-supply-psu | $11.99 base. **In the R2 BOM.** Needed to feed the Pi clean 5V off 24V — **only skip if you verify the Octopus Pro USB-A 5V output reliably drives the Pi** (many do; then cut this row). |
| 2 | Fuse 5x20mm 8A (120V mains) | 5 | West3D | https://west3d.com/products/fuse-8a-250v-holder-cartridge-5-x-20mm-glass | $0.99 ea base. |
| 1 | BAT85 Diode | 5 | West3D | https://west3d.com/products/bat85-diode | $0.99 base. |
| 1 | Thermal Fuse 150C | 5 | West3D | https://west3d.com/products/125c-cutoff-15a-thermal-fuse | $1.39 base (150C variant). For the reused Ender 3 bed. |

> **Reused, BOM-covered at $0:** 2× 40x40x10 axial fans (Ender 3s → **Stealthburner** hotend + part cooling — no 5015 blower needed), C13 power cord (Ender 3), mini display (1284P reuse), AC inlet + switch (Ender 3, verify), PSU 24V 15A (Ender 3, replaces LRS-200-24 + TBC-09).

### Toolhead (Hotend + Extruder) (~$125)

| Qty | Part | Est. $ | Source | Link | Notes |
|---|---|---|---|---|---|
| 1 | Phaetus **Dragon UHF** hotend 24V | 75 | West3D | https://west3d.com/products/phaetus-dragon-uhf-hot-end | $74.99 base (Labor Day sale from $94.99) — **8× 5★ reviews**, cartridge-style heater+thermistor, unlimited-speed rated. This is the "Dragon" in West3D's configurator (E3D Dragon variant). Pairs with **Octopus Pro onboard MAX31865** if it ships PT100/PT1000; verify thermistor type. 24V heater fine on the reused Ender 3 PSU. |
| 1 | **Clockwork 2 gear set** (drive gear + idler + bearings) | 25 | Amazon | https://west3d.com/products/bondtech-oem-idga-set (West3D **sold out**) · https://www.amazon.com/dp/B0CF9BJBFB | **NOT the full BMG metal extruder (~$80) — CW2 uses just its gear pair.** Preferred: **Bondtech OEM IDGA Set (15169)** for CW2, $17.99–22.50 (West3D $19.99 **out of stock**; Filastruder/bondtech.se direct). Cheap compatible hardened BMG gear set (Amazon ~$13–15) works too. This satisfies the BOM "BMG Extruder Components Kit" line. The repo configs preset `gear_ratio: 50:10` for Stealthburner/CW2 (50:17 is Afterburner/CW1). |
| 1 | **NEMA14 pancake** 36STH20-1004AHG (E-drive motor) | 25 | West3D | https://west3d.com/products/ldo-nema14-36mm-pancake-stepper-motor-ldo-36sth20-1004ahg | $24.99 base — stock CW2 motor, light (~150g), classic toolhead + max accel. **Pairs with the Bondtech OEM IDGA gear set (integrated-shaft gear — the official CW2 combo)**; a standard pressed-on BMG gear works too if the pancake has a 5 mm D-shaft. Alternative for −$25: skip it and reuse a NEMA17 with a spacer mod (printables 950092) — same CW2 gear set. |

### Cables & Misc (~$160)

| Qty | Part | Est. $ | Source | Link | Notes |
|---|---|---|---|---|---|
| 1 kit | JST XH 2.54 kit (2/3/4/5P + pins) | 15 | West3D | https://west3d.com/products/230pcs-jst-xh-2-54-pitch-2-3-4-5-pin-kit-housing-and-pin-headers-wire-to-board | ~$13 base. Octopus endstops/fans/probe. |
| 1 kit | Molex MicroFit 3.0 kit (genuine) | 15 | Amazon | https://www.amazon.com/s?k=Micro-Fit+3.0+connector+kit | ~$12–15 base — **genuine Molex** crimp terminals/housings, not knockoffs. Only a handful of 2P/3P needed (steppers + toolhead). Power connectors = never cheap out. |
| 6 | WAGO 221 lever nuts (×3 415 + ×3 412) | 10 | West3D | https://west3d.com/products/wago-lever-nuts-fast-wire-cable-connectors-12-24awg-221-412-221-413-221-415 | $12.84 base (tighten estimate; alternative: reuse Ender 3 screw terminals). |
| 2 | PTFE Tube 4mm OD (2mm ID + 3mm ID), 1m each | 10 | West3D | https://west3d.com/products/bowden-ptfe-tube-4mm-od-2mm-id · https://west3d.com/products/bowden-ptfe-tube-4mm-od-3mm-id | $2.50/m base. (You have 800mm of 4/2.) |
| 1 | 3M VHB Tape 5952 | 10 | West3D | https://west3d.com/products/3m-vhb-tape-5952 | $6.99 base. |
| 1 roll | Foam tape 3mm, 5mm wide (10m) | 10 | West3D | https://west3d.com/products/5mm-x-10m-single-sided-self-adhesive-tape-3mm-thick | $5.99 base. |
| 1 | Mobil EP2 Grease (10ml syringe) | 15 | West3D | https://west3d.com/products/mobil-mobilux-ep2-10ml-filled-syringe-with-blunt-tip | $9.99 base. For leadscrews. |
| 8 | 6x3mm Neodymium Magnets (N52) | 10 | West3D | https://west3d.com/products/6mm-x-3mm-round-neomydium-magnets | $0.39 ea base. Bed/plate retention. |
| — | High-flex wire: 18AWG + 20AWG + 22-24AWG (short rolls) | 25 | Amazon | https://www.amazon.com/s?k=18awg+silicone+wire · https://www.amazon.com/s?k=22awg+silicone+wire+100ft | Kept lean — **reuse Ender 3 motor/power/bed harnesses where they fit** (Ender3dent: "Cables: yes, except toolhead wiring"). What you buy: **name-brand silicone** (e.g. genuine silicon/fine-strand) for toolhead + Octopus wiring. |
| 20 | Nylon cable ties 4" | 10 | Amazon | https://www.amazon.com/s?k=nylon+cable+ties+4+inch | ~$6 base. |
| 10 | Spade crimp terminals 4.8mm | 5 | Amazon | https://www.amazon.com/s?k=spade+crimp+terminal+4.8mm+female | ~$4 base. Check Ender 3 harnesses first — may already cover these. |
| 1 | Loctite Blue Threadlocker | 10 | Amazon | https://www.amazon.com/s?k=loctite+blue+threadlocker+243 | ~$7 base. |
| 1 | PEI sheet / 3M 468MP for bed top | 15 | Amazon | https://www.amazon.com/s?k=PEI+sheet+0.04+250mm | ~$10 base. Laminate onto reused Ender 3 flexplate/bed. |

### Totals — Core

| | Est. $ |
|---|---|
| Printed parts (kit) | 145 |
| Fasteners | 70 |
| Motion | 90 |
| Electronics | 215 |
| Toolhead (Dragon + CW2 gear set + NEMA14 pancake) | 125 |
| Cables & Misc | 160 |
| **Core total** | **~805** |
| Verifiable trims: RS-25-5 if Octopus 5V powers Pi (−15), drop 3mm-ID PTFE (−5, have 800mm 4/2), reuse Ender 3 ties/spades (−15), defer PEI sheet (−15) | −50 |
| **~Expected total** | **~755–770 after the easy trims** (still ~$55–70 over the $700 cap). The CW2 gear set instead of the full BMG = **−$60** vs the earlier standard path; the overage is the Dragon ($75) + NEMA14 pancake ($25). Swapping the pancake for the NEMA17 spacer mod later −$25 → ~$730–745. |

## BUY — Optional / Phase 2 (add when budget allows)

| Part | Est. $ | Source | Link | Notes |
|---|---|---|---|---|
| Acrylic panels 250mm (full set) | 40 | West3D | https://west3d.com/products/voron-trident-acrylic-panels-by-west3d-in-stock | $34.99 base. Phase 2 (enclosure). |
| ABS/ACM panels 250mm (replaces Coroplast) | 45 | West3D | https://west3d.com/products/voron-trident-abs-panels | $39 base. Phase 2. |
| Toolhead X/Y cable chain 10x11mm, 1m + end sets | 20 | Amazon | https://www.amazon.com/s?k=10x11mm+cable+chain+3d+printer+1m | BOM: "10x11 Cable Chain — 1m, 3 End Sets". **Generic is fine** (~$15-20). Use the **3-hole** end-mount printed part from the kit (manual: generic chains use 3-hole pattern; igus uses 2-hole — the Trident has mounts for both). **Can skip entirely to start** — cable guides + ties work for first prints. Upgrade path: igus ($52.99 West3D https://west3d.com/products/igus-cable-chain-kits) = smoother/quieter + built-in strain relief; get it only if the extra $35 is affordable. |
| Tesa wire loom tape | 15 | Amazon | https://www.amazon.com/s?k=tesa+wire+loom+harness+tape+51608 | ~$8 base. |
| Braided cable sheathing | 10 | West3D | https://west3d.com/products/braided-cable-sleeve-insulated-pet-expandable | $1.49/m base. |
| NeoPixel RGBW ×3 | 10 | West3D | https://west3d.com/products/sk6812-rgbw-5v-led-neopixel | $1.29 ea base. Bare LEDs — BOM wants assembled Mini Button PCBs. |
| Trident rubber feet (set of 4) | 15 | West3D | https://west3d.com/products/updated-rubber-feet-for-trident-v2-4-set-of-4 | $8.99 base. If Ender 3 pads don't sit flat. |

## Fallback (only if an Ender3dent reuse fails verification)

| If this reuse fails... | Buy instead | Est. $ | Link |
|---|---|---|---|
| Ender 3 AC inlet + switch | Tyco 10EGG1-2 + ZF rocker | 45 | https://west3d.com/products/tycoelectronics-10ehg1-2-filtered-power-inlet · https://west3d.com/products/zf-rocker-switch-dpst-16a-on-off-wrg32f2bbrln |
| Ender 3 PSU | Mean Well LRS-200-24 | 30 | https://west3d.com/products/mean-well-lrs-200-24-200w-24v-8-8a-power-supply-psu |
| Direct bed heater drive | Omron G3NA SSR + DIN bracket | 50 | https://west3d.com/products/omron-g3na-210b-utu-dc5-24v-solid-state-relay-ssr |
| Ender 3 bed (if it fails) | LDO Build Plate Complete Kit | 145 | https://west3d.com/products/voron-trident-aluminum-build-plate-complete-kit-by-ldo-systems-heater-magnet-and-fuse-pre-applied-to-plate |
| (Hotend/extruder are BUY items now — Dragon + CW2 gear set + NEMA14 pancake. No toolhead reuse falls back.) | — | — | — |
| (Optional −$25 later: replace the NEMA14 pancake with a reused NEMA17 + dferrg spacer mod — same CW2 gear set, swap the motor, just a PETG print) | 0 | https://www.printables.com/model/950092 |

## Caveats (verify before relying on reuse)

- **Toolhead = BUY, not reuse.** Dragon + CW2 gear set + NEMA14 pancake motor bought new (stock SB/CW2, no mods). The remaining Ender 3 reuses are static/low-risk: leadscrews + couplers, bed + flexplate, PSU 24V (takes the Dragon's 24V heater fine), AC inlet + switch, harnesses, display, NEMA17s, 4010 fans.
- **AC inlet + switch:** Ender 3 inlet is unfiltered and the switch is 10A (BOM wants filtered inlet + 16A). Verify before skipping the Tyco+ZF.
- **Z-axis with T8x8:** Ender 3 rod is **T8x8 (8mm lead, 2mm pitch, 4-start)** vs the BOM's **TR8x4 (4mm lead, 2-start)** — 2× Z speed, half resolution. Klipper handles it (steps/mm). **Thread-compat:** a T8x8 nut ONLY fits the 4-start T8x8 rod; the BOM's TR8x4 nut won't mate. Since all 3 Z reuse/run 8mm-lead rods, use matching T8x8 nuts (buy 1 more) and Klipper steps/mm is uniform. Ender3dent-validated; print the spacer standoffs (printables 644553 / 1255726).
- **Bed size:** Ender 3 bed is 235x235 in a 250 build area — effective build volume becomes 235x235x250. Mounting jig: https://www.printables.com/model/756948
- **Display:** 1284P is 128x64 like the Mini 12864, but verify pinout against the Octopus display port.
- **Creality mainboard:** NOT needed — Octopus Pro (6 drivers) covers all 6 steppers + bed heater + probe. Keep boards as spares.
- **Printed parts = the biggest hidden cost (~$145).** You can't print ABS, so the clean quality path is a **PIF/verified ABS functional kit** + **self-print the cosmetics in PLA** (see Printed Parts section — recommended). Alternative if strictly on a tight budget: print the structural kit yourself in **PETG** — but watch the 235×235 Ender 3 bed (several Trident parts are longer) and PETG softening near the hotend/enclosure; the kit also gives you the proper Voron-recommended ABS material and tolerances. ABS filament ≈ $25-35/roll × several rolls ≈ often more than the kit once you factor failed prints.
- **Quality keeps the price reasonable:** the ~$755-770 total works *because* of Ender 3 reuse (leadscrews, bed + flexplate, PSU, AC inlet, harnesses, NEMA17s, 4010 fans) plus buying **reputable-brand** where you must. The toolhead is Dragon ($75) + CW2 gear set ($25) + **NEMA14 pancake ($25)** — not the full-BMG route (−$60 vs the BMG-complete plan). Remaining overcap = the Dragon + pancake; the ±$25 lever swings to the NEMA17 spacer mod; the big lever if $700 is a hard wall is the hotend (free/stock reuse).
- **Roll-in vs drop-in T-nuts:** BDF kit ships roll-ins; fit tight in LDO extrusion.
- **Frame:** Ender3dent warns NOT to use V-Slot or ITEM/Slot-5 extrusion — your LDO frame kit is fine (proper 2020).
- Prices/stock verified 2026-09-06; West3D Labor Day sale 9/5–9/7 sitewide.
