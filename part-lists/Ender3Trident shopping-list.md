# Ender3Trident Shopping List — DRAFT v3 (budget, review before merging into parts.md)

> **AI-edited:** This file was researched, drafted, and edited with AI assistance. Verify all prices, stock, and compatibility details before ordering.
>
> Sourcing research, prices checked 2026-09-06. Amazon-first where cheaper, West3D for Voron-specifics.
> Build: **Trident R2, 250mm, blind joints, Octopus Pro V1.1 + BTT Pi V1.2**, following the [Ender3dent](https://github.com/yell3D/Ender3dent) approach (maximize Ender 3 reuse).
> Prices are **padded estimates** (base + ~$5, rounded up) to cover tax/shipping/price drift unless noted. Base prices in Notes.
> **Quality policy (2026-09-07):** electronics (Octopus Pro, BTT Pi, probe, drivers) must be **genuine** — no cheap/clone compatibles. **Mechanical/toolhead/misc may use budget/no-name/AliExpress parts** if functionally compatible; risk is noted per row.
> **Budget target (2026-09-07, relaxed non-electronics): core ≈ $863; ~$851 if RS-25-5 is trimmed; ~$811 with all easy trims. Frame + rails ≈ $225. Toolhead = Stealthburner + V6 hotend + CW2 gear set + NEMA14 pancake.**
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
| ~~Custom Hotend~~ **NO — now a BUY** | 2× Ender 3 hotends (heat block + nozzle + heater + catheter) | E3D V6 kit → **bought: V6 hotend (Toolhead section). Ender 3 MK8 hotend NOT reused.** |
| 40x40x10 fans | 6× 4010 24V fans | 40x40x10 axial fan |
| GT2 20T pulleys | 4× 2GT-d5-20-6mm | 3× GT2 20T pulleys |
| Rubber foot pads | 8× 20x40x3mm pads | 4× Rubber Foot (**verify** fit/flatness) |
| Creality mainboard (yes, as secondary MCU) | 2× 1284P mainboards | optional — NOT needed if Octopus Pro drives all 6 steppers + bed heater directly |

**Frame & rails (not yet purchased):** now budgeted in the **Frame & Rails** section below (~$225). *(Nothing has been bought yet — these were previously assumed owned.)*

## BUY — Core (≈ $863; ~$851 RS-trimmed; ~$811 all easy trims; see totals)

### Frame & Rails (~$225)

| Qty | Part | Est. $ | Source | Link | Notes |
|---|---|---|---|---|---|
| 1 | LDO Trident frame kit 250mm | 125 | West3D / Hobbyist Depot | https://west3d.com/products/ldo-trident-frame-kit-multiple-colors · https://hobbyistdepot.com/products/ldo-trident-frame-kit-multiple-colors | 2020 extrusion frame kit (250mm). **$124.99 sale** (list $139.99). **Verify 250mm variant + color at order.** Aggressive DIY: AliExpress raw 2020 10×1000mm $42.38 (https://www.aliexpress.com/item/3256809654623387.html) but requires cutting/drilling/tapping and unverified lengths. |
| 1 pair | DIN rails 35mm (steel) | 10 | West3D | https://west3d.com/products/din-rails-35mm-x-7-5mm-steel-pair | Electronics-bay mounting. $9.99. |
| 5 | MGN9H 300mm linear rail w/ carriage | 72 | Amazon (uxcell) | https://www.amazon.com/dp/B0D54LGWHJ · https://www.amazon.com/dp/B0D54KR8KG | 2× $27.29 2-packs + 1× $17.49–17.99 single = 5 rails. No-name risk: verify 300mm length + MGN9H carriage. |
| 1 | MGN12H 300mm linear rail w/ carriage | 18 | Amazon (uxcell) | https://www.amazon.com/dp/B0D54HML8M | X rail. $17.49–21.99. No-name risk: verify 300mm length. |

### Printed Parts (functional kit = buy; cosmetics = self-print PLA)

| Qty | Part | Est. $ | Source | Link | Notes |
|---|---|---|---|---|---|
| 1 set | Voron Trident functional ABS printed parts kit | 140 | West3D | https://west3d.com/products/printed-parts-for-voron-trident | $139.99 base (verified 9/7). Prints the **PIF "functional" kit scope** but is **explicitly NOT PIF-affiliated** (page says so). Made-to-order: ~5 bd — up to 3 wks. **Consolidates with your main West3D order, BUT excluded from free shipping** (separate big box; flat rate, page: "usually less than what we pay"). **At order time you must pick color + board + hotend BEFORE adding to cart** + use the special-instructions field. **Form picks: Toolhead = Stealthburner, Hotend = V6, Controller = Octopus** (standard, no Custom needed). Reviews (8): 4×5★ / 1×4★ / 2×2★ / 1×1★ — gripes = warped A/B-drives/idlers/XY-joints (vendor: pulled off plate before cool; now reprinted w/ extended cooling), some **missing functional parts** (incl. CW cable cover w/ thermistor mount) → **check EVERY bag against the PIF BOM on arrival**; vendor replaces/corrects free, incl. during-build issues. Cancellation/refund only pre-print (or >3 wks delay). **Alt (same price, slower):** Fabreeko PIF $139.99 (https://www.fabreeko.com/products/voron-trident-printed-parts-by-pif) — **no V6 option shown** (Revo/Dragon/Rapido/BMO only) → not compatible with this build. 3D Pros $139.99 (https://3dpros.online/products/voron-trident-printed-parts-kits) — **confirm V6 option before ordering**. KB-3D/Bounty3D $149.99 (https://kb-3d.com/store/v1-trident/551-voron-trident-printed-parts-kit-configurable). |
| 1 set | Cosmetics: skirts, panel clips, display mount, covers — **self-print in PLA** | 0 | self-print | cloned repo `STLs/Skirt/250/` (or upstream Voron-Trident GitHub) | **PLA is fine here** — these are cosmetic, non-load-bearing, away from heat, and PLA is trivially easy on your Ender 3. **Only caveat:** if you later enclose + print ABS/ASA, a heated enclosure softens PLA (~60°C glass transition) → reprint cosmetics in PETG/ASA then. Most pieces fit your 235×235 bed; the few longer skirt/hat panels can be printed later on the new printer (or split). Never substitute PLA for anything in the functional kit. |
| 1 set | Ender3dent mod parts (spacer standoffs, etc.) | handled | — | https://www.printables.com/model/644553 · https://www.printables.com/model/1255726 | Small PLA/PETG prints for the mods — printable on your Ender 3 (they're small, <235mm). |

### Fasteners

| Qty | Part | Est. $ | Source | Link | Notes |
|---|---|---|---|---|---|
| 1 kit | Tensor3D black Trident fastener kit (or West3D BDF) | 65 | Tensor3D / West3D | https://checkout.tensor3d.com/products/tensor3d-trident-fastener-kit · https://west3d.com/products/west3d-stainless-steel-fastener-kit-for-voron-trident-bdf | Tensor3D black **$64.99** (304 SS + ~20% extra) — **confirm T-nut fit for LDO frame** before ordering. Fallback: West3D BDF **$69.99** ("R2 UPGRADED AS OF 6/17/2026", complete, roll-in T-nuts). Generic M3 kits are partial only. |

### Motion (~$52)

| Qty | Part | Est. $ | Source | Link | Notes |
|---|---|---|---|---|---|
| 2 | GT2 20T Toothed Idler (5mm ID 6mm W) | 4 | West3D | https://west3d.com/products/black-pulleys-and-idlers-gt2-20t-gt2-16t | $1.79 ea base. |
| 26 | F695-2RS Bearing (5x13x4mm flanged) | 14 | AliExpress / Amazon | https://www.aliexpress.us/item/3256807982379901.html · https://www.amazon.com/dp/B0D1VV8WQF | AliExpress 2× 20pk = **$13.38** (no-name, verify 5×13×4 flanged). Amazon 2× 20pk ≈ $26 (reputable). (Your 52× 625ZZ are 1mm smaller OD — not interchangeable.) |
| 3 | GE5C Spherical Bearing | 9 | West3D | https://west3d.com/products/ge5c-spherical-bearing-nsk | $2.99 ea base. Needed for the Trident Z gimbal. |
| 1 | 5x30mm Shaft | 1 | West3D | https://west3d.com/products/round-shafts-5x30mm-5x60mm | $0.49 base. |
| 2 | GT2 Open Belt 6mm, 1690mm each | 6 | AliExpress / West3D | https://www.aliexpress.us/item/2251832625518193.html · https://west3d.com/products/gates-gt2-open-belt-ll-2gt-6-6mm-wide-voron-v0-v1-v2-switchwire | AliExpress 5m open GT2-6mm = **$5.76** (no-name, requires cutting/splicing to 2×1690mm). Fallback: West3D GATES 34×100mm = $16.66. |
| 1 | T8x8 Leadscrew 365mm (3rd Z column) | 8 | AliExpress / Amazon | https://www.aliexpress.com/w/wholesale-T8x8-leadscrew-365mm.html · https://www.amazon.com/s?k=T8x8+leadscrew+365mm+3D+printer | AliExpress T8x8 365mm + nut combo ≈ **$7.22** (verify 4-start + 365mm length). Fallback: Amazon 2-pack $12.59. Reuse 2× Ender 3 T8x8 leadscrews for the other 2 columns. |
| 1 | T8x8 Coupler D5*8 (3rd Z column) | 10 | Amazon | https://www.amazon.com/s?k=T8x8+coupler+5mm+3D+printer | $9.99 5-pack. Reuse 2× Ender 3 Z couplers. Print spacer standoffs (Ender3dent mod 644553 / printables 1255726) so reusing the coupler doesn't lose Z height. |
| 1 | T8x8 Nut (brass, 22mm flange, 4× M3 holes) | 0 | included | — | Included in the T8x8 leadscrew combo. **Must be 4-start (matches your T8x8 rod), NOT the BOM's TR8x4.** Reuse 2× Ender 3 nuts; the combo provides the 3rd. |

### Electronics (~$202)

| Qty | Part | Est. $ | Source | Link | Notes |
|---|---|---|---|---|---|
| 1 | **BTT Octopus Pro V1.1 (H723) + BTT Pi V1.2 + 7× drivers bundle** | 140 | Amazon | https://www.amazon.com/dp/B0CL6J66M4 | $139.99 base — **genuine BTT sold by BIGTREETECH via Amazon**. ONE order replaces three lines: Octopus Pro board + host computer + stepper drivers (~$155 à la carte → ~$140). Board = **V1.1 H723 (550MHz, 512KB flash)** — newer/faster than the V1.0 F446; **on-board MAX31865 PT100**, CAN, 6 controllable fans. **Host = BTT Pi V1.2 (Allwinner H616 quad-A53 1.5GHz, 1GB, 2.4G WiFi)** — first-party BTT, Klipper-ready; **NOT a genuine Raspberry Pi** (accepted tradeoff to stay under budget). Drivers = **5× TMC2209 + 2× TMC5160T** (7 total, 6 needed: A-B-Z-Z1-Z2-E). Title says 5×2209 but item details say 6×2209 — **count drivers on arrival**. Assign the TMC5160Ts to X/Y or Z and note their drive config differs from the silent 2209s. |
| 1 | Omron TL-Q5MC2-Z NPN NC inductive probe (self-leveling) | 20 | West3D | https://west3d.com/products/omron-tl-q5m-inductive-probe | $14.99 base, in stock — **genuine Omron**. |
| 3 | 60x60x20 Axial Fan 24V | 21 | West3D | https://west3d.com/products/gdstime-dc-24v-60x60x20-axial-fan-gda6020-dual-ball-bearing-5000rpm-1-7w-0-1a-xh2-54 | $6.99 ea base. Electronics bay. |
| 1 | Mean Well RS-25-5 (5V) | 12 | West3D | https://west3d.com/products/mean-well-rs-25-5-25w-5v-5a-power-supply-psu | $11.99 base. **In the R2 BOM.** Needed to feed the Pi clean 5V off 24V — **only skip if you verify the Octopus Pro USB-A 5V output reliably drives the Pi** (many do; then cut this row). |
| 3 | Fuse 5x20mm 8A (120V mains) | 3 | West3D | https://west3d.com/products/fuse-8a-250v-holder-cartridge-5-x-20mm-glass | $0.99 ea base. |
| 3 | BAT85 Diode | 3 | West3D | https://west3d.com/products/bat85-diode | $0.99 ea base. |
| 2 | Thermal Fuse 150C | 3 | West3D | https://west3d.com/products/125c-cutoff-15a-thermal-fuse | $1.39 ea base (150C variant). For the reused Ender 3 bed. |

> **Reused, BOM-covered at $0:** 2× 40x40x10 axial fans (Ender 3s → **Stealthburner** hotend + part cooling — no 5015 blower needed), C13 power cord (Ender 3), mini display (1284P reuse), AC inlet + switch (Ender 3, verify), PSU 24V 15A (Ender 3, replaces LRS-200-24 + TBC-09).

### Toolhead (Hotend + Extruder) (~$57)

| Qty | Part | Est. $ | Source | Link | Notes |
|---|---|---|---|---|---|
| 1 | **E3D-style V6 hotend** (complete, 24V) | 18 | West3D | https://west3d.com/products/v6-all-metal-hotend-kit | **$17.99** in stock. **Cart: remove the TriangleLab Dragon ACE 104NT ($64.99) line; pick Hotend = V6 in the West3D printed-parts configurator** (SB front/toolhead uses the V6 mount). V6 fits the Stealthburner V6 front, CW2 + IDGA gear set unchanged, 24V heater fine on the reused Ender 3 PSU. Only tradeoff vs Dragon = flow/accel headroom, irrelevant at stock Ender 3 speeds. |
| 1 | **Clockwork 2 gear set** (Bondtech OEM IDGA) | 18 | Bondtech | https://www.bondtech.se/product/oem-idga-set/ | **$18.00** in stock (backorderable). **NOT the full BMG metal extruder (~$80) — CW2 uses just its gear pair.** Bondtech OEM IDGA Set (15169) is the CW2-compatible choice. Cheap BMG clones are **not confirmed CW2/IDGA-compatible** — do not substitute. The repo configs preset `gear_ratio: 50:10` for Stealthburner/CW2. |
| 1 | **NEMA14 pancake** 36STH20-1004AHG (E-drive motor) | 21 | West3D | https://west3d.com/products/ldo-nema14-36mm-pancake-stepper-motor-ldo-36sth20-1004ahg | **$20.99** in stock — stock CW2 motor, light (~150g), classic toolhead + max accel. **Pairs with the Bondtech OEM IDGA gear set (integrated-shaft gear — the official CW2 combo)**. Alternative for −$21: skip it and reuse a NEMA17 with a spacer mod (printables 950092) — same CW2 gear set. |

### Cables & Misc (~$122)

| Qty | Part | Est. $ | Source | Link | Notes |
|---|---|---|---|---|---|
| 1 kit | JST XH 2.54 kit (2/3/4/5P + pins) | 6 | West3D | https://west3d.com/products/230pcs-jst-xh-2-54-pitch-2-3-4-5-pin-kit-housing-and-pin-headers-wire-to-board | $5.99 base. Octopus endstops/fans/probe. |
| 1 kit | Molex MicroFit 3.0 kit (genuine) | 15 | Amazon / Mouser | https://www.amazon.com/s?k=Micro-Fit+3.0+connector+kit | ~$12–15 — **genuine Molex** crimp terminals/housings, not knockoffs. Only a handful of 2P/3P needed (steppers + toolhead). Power connectors = never cheap out. |
| 6 | WAGO 221 lever nuts (×3 415 + ×3 412) | 13 | West3D | https://west3d.com/products/wago-lever-nuts-fast-wire-cable-connectors-12-24awg-221-412-221-413-221-415 | $12.84 base. |
| 2 | PTFE Tube 4mm OD (2mm ID + 3mm ID), 1m each | 2 | AliExpress | https://www.aliexpress.us/item/2251832739488684.html · https://www.aliexpress.us/item/3256806230155312.html | ~$0.99 each (no-name, verify ID/OD). Fallback: West3D $2.50/m. (You have 800mm of 4/2.) |
| 1 | 3M VHB Tape 5952 | 0 | Amazon / West3D | https://www.amazon.com/dp/B00HLY78TE · https://west3d.com/products/3m-vhb-tape-5952 | **Skip if using 3M 468MP for the bed** (see PEI row). If needed: Amazon 6.35mm roll $9.19 (West3D 5mm OOS). AliExpress "3M 5952" $0.99 is likely counterfeit — avoid for structural bonds. |
| 1 roll | Foam tape 3mm, 5mm wide (10m) | 1 | AliExpress | https://www.aliexpress.us/item/3256805843054059.html | ~$0.99 (no-name, verify 3mm thick + 5mm wide). Fallback: West3D $5.99. |
| 1 | Grease 10ml syringe (lithium / EP2) | 1 | AliExpress / West3D | https://www.aliexpress.us/item/3256811942532783.html · https://west3d.com/products/mobil-mobilux-ep2-10ml-filled-syringe-with-blunt-tip | AliExpress SIKEZHAN lithium grease ~$0.99 (no-name, fine for light 3DP loads). Fallback: Mobil EP2 $9.99. |
| 8 | 6x3mm Neodymium Magnets (N42/N52) | 1 | AliExpress / West3D | https://www.aliexpress.us/item/3256809739424229.html · https://west3d.com/products/6mm-x-3mm-round-neomydium-magnets | AliExpress 40× 6×3mm N42 ~$0.99 (no-name, verify dims). Fallback: West3D $0.39 ea. |
| — | High-flex wire: 18AWG + 20AWG + 22-24AWG (short rolls) | 26 | Amazon | https://www.amazon.com/dp/B0FH1CDFGG · https://www.amazon.com/dp/B0746HG158 | 18AWG 100ft $20.49 + 22AWG 2-color 10ft $5.18. **Reuse Ender 3 motor/power/bed harnesses where they fit.** AliExpress 10m silicone wire "from $0.99" is unverified per-SKU — avoid for power. |
| 20 | Nylon cable ties 4" | 10 | Amazon | https://www.amazon.com/dp/B078NT5F2B | $9.99 for 1000-pack (value). |
| 10 | Spade crimp terminals 4.8mm | 9 | Amazon | https://www.amazon.com/dp/B07VSD3HDM | Twidec 440pcs assortment $8.99 (2.8/4.8/6.3mm + sleeves). |
| 1 | Loctite Blue Threadlocker | 9 | Amazon | https://www.amazon.com/s?k=loctite+blue+threadlocker+243 | Loctite 243 6ml $9.38. AliExpress "243 blue" 50ml ~$0.99 is a knockoff — OK for general threads, not critical. |
| 1 | PEI sheet 235×235 + 3M 468MP for bed top | 29 | Amazon | https://www.amazon.com/dp/B0CXCS9HXK · https://www.amazon.com/dp/B0CXT2VBV1 | 235×235 PEI sheet $13.99 + 468MP 10×10 5pk $14.99. Laminate onto reused Ender 3 flexplate/bed. **Do NOT use a 250×250 magnetic PEI plate** — it won't fit the 235×235 Ender 3 bed. |

### Totals — Core

| | Est. $ |
|---|---|
| Frame & Rails (frame kit + DIN + 5× MGN9H + MGN12H) | 225 |
| Printed parts (kit) | 140 |
| Fasteners | 65 |
| Motion | 52 |
| Electronics | 202 |
| Toolhead (V6 + CW2 gear set + NEMA14 pancake) | 57 |
| Cables & Misc | 122 |
| **Core total** | **~863** |
| Verifiable trims: RS-25-5 if Octopus 5V powers Pi (−12), drop 3mm-ID PTFE (−1, have 800mm 4/2), reuse Ender 3 ties/spades (−10), defer PEI sheet (−29) | −52 |
| **~Expected total** | **~851 if only RS-25-5 is trimmed; ~811 if all the easy trims above are taken** (frame + rails ≈ $225). The CW2 gear set instead of the full BMG = **−$60**, V6 instead of Dragon = **−$55**, no-name rails/motion/misc = **~$250** vs the earlier reputable-brand baseline. Swapping the NEMA14 pancake for the NEMA17 spacer mod later −$21 → ~$830 (from $851) or ~$790 (from $811). |

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
| (Hotend/extruder are BUY items now — V6 + CW2 gear set + NEMA14 pancake. No toolhead reuse falls back.) | — | — | — |
| (Optional −$21 later: replace the NEMA14 pancake with a reused NEMA17 + dferrg spacer mod — same CW2 gear set, swap the motor, just a PETG print) | 0 | https://www.printables.com/model/950092 |

## Caveats (verify before relying on reuse)

- **Toolhead = BUY, not reuse.** V6 hotend + CW2 gear set + NEMA14 pancake motor bought new (stock SB/CW2, Hotend option = V6). The remaining Ender 3 reuses are static/low-risk: leadscrews + couplers, bed + flexplate, PSU 24V (takes the V6's 24V heater fine), AC inlet + switch, harnesses, display, NEMA17s, 4010 fans.
- **AC inlet + switch:** Ender 3 inlet is unfiltered and the switch is 10A (BOM wants filtered inlet + 16A). Verify before skipping the Tyco+ZF.
- **Z-axis with T8x8:** Ender 3 rod is **T8x8 (8mm lead, 2mm pitch, 4-start)** vs the BOM's **TR8x4 (4mm lead, 2-start)** — 2× Z speed, half resolution. Klipper handles it (steps/mm). **Thread-compat:** a T8x8 nut ONLY fits the 4-start T8x8 rod; the BOM's TR8x4 nut won't mate. Since all 3 Z reuse/run 8mm-lead rods, use matching T8x8 nuts (buy 1 more) and Klipper steps/mm is uniform. Ender3dent-validated; print the spacer standoffs (printables 644553 / 1255726).
- **Bed size:** Ender 3 bed is 235x235 in a 250 build area — effective build volume becomes 235x235x250. Mounting jig: https://www.printables.com/model/756948
- **Display:** 1284P is 128x64 like the Mini 12864, but verify pinout against the Octopus display port.
- **Creality mainboard:** NOT needed — Octopus Pro (6 drivers) covers all 6 steppers + bed heater + probe. Keep boards as spares.
- **Printed parts = the biggest hidden cost (~$140).** You can't print ABS, so the clean quality path is a **PIF/verified ABS functional kit** + **self-print the cosmetics in PLA** (see Printed Parts section — recommended). Alternative if strictly on a tight budget: print the structural kit yourself in **PETG** — but watch the 235×235 Ender 3 bed (several Trident parts are longer) and PETG softening near the hotend/enclosure; the kit also gives you the proper Voron-recommended ABS material and tolerances. ABS filament ≈ $25-35/roll × several rolls ≈ often more than the kit once you factor failed prints.
- **Quality keeps the price reasonable:** the ~$811–851 total works *because* of Ender 3 reuse (leadscrews, bed + flexplate, PSU, AC inlet, harnesses, NEMA17s, 4010 fans) plus **budget/no-name mechanical parts** (allowed as of 2026-09-07). The frame + linear rails (~$225) are the largest single block and are **not yet purchased**. The toolhead is V6 ($18) + CW2 gear set ($18) + **NEMA14 pancake ($21)**. The ±$21 lever swings to the NEMA17 spacer mod; further lean levers if needed: Tensor3D silver rev A fastener kit (−$25, stock unverified) or AliExpress raw 2020 extrusion instead of the LDO frame (−$83, high DIY risk).
- **Roll-in vs drop-in T-nuts:** Tensor3D/BDF kits ship roll-ins; fit tight in LDO extrusion.
- **Frame:** Ender3dent warns NOT to use V-Slot or ITEM/Slot-5 extrusion — your LDO frame kit is fine (proper 2020).
- Prices/stock verified 2026-09-07; West3D Labor Day sale 9/5–9/7 sitewide.
