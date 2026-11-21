# Elevated goat + poultry shed, Parvathagiri, Warangal: full project record

Last updated: 18 Nov 2026. This is the single place that describes the current design, the land, the 3D/VR model, the cost and every decision so far.

## Quick links

| What | Where |
|---|---|
| 3D / VR model (live, open on phone, PC or Meta Quest 3S) | https://jagapathibanoth6-dotcom.github.io/gaot-shed/ |
| GitHub repository | https://github.com/jagapathibanoth6-dotcom/gaot-shed |

## Site

- Location: Parvathagiri, Warangal, Telangana. Agricultural land, no flood issue. Sand already filled about 1.5 ft above ground around the farm.
- Directions as the owner uses them: front = North (uttaram, road side), back = South (dakshinam), right = East (turpu), left = West.
- Land traced from the owner's Google Maps measurement: **13,790 m² = 3.41 acres** (owner calls it 3 acres). Edges: North 512 ft, East 240.37 ft, South 573.24 ft, West 330.44 ft. Perimeter 502 m.
- Shed sits **10 ft from the west boundary**, near the north (road) side, inside about 15 guntas.
- Rest of the land: planned oil palm (about 153 palms shown in the model). Grass for goats from leased land.
- Weather notes: wind zone about 44 m/s; Cyclone Montha brought extreme rain (36.7 cm at Parvathagiri). Roof anchoring and pile pull-out resistance matter.

## Shed: overall

- Size **75 × 50 ft** (3,750 sq ft), elevated goat floor with hens underneath. About 200 goats.
- Whole frame steel, no wood. 35 pillars on a 12.5 ft grid, RCC piles + pile caps, ground tie beams both ways, 1 × 1 ft concrete pedestal 2 ft above ground, then steel columns (14 edge 150×150 SHS, 21 inner 125×125 SHS).
- X-bracing in end bays only.
- Gable roof with fibre cement sheets. Ceiling fans in the roof space above the goats.

## Goat level

- **Floor at 11.5 ft**, plastic slatted floor (not wooden bars). Clear height for people **7 ft**.
- **6 pens** (3 each side of the central aisle). Main entry (aisle) side kept normal.
- **1.5 ft walkway** between pens with feeders on both sides of every walkway.
- End pens (front and back): feeder moved to the walkway side as an **L-shape**, gate at the corner.
- Walls: 2 ft sheet band bottom, 2 ft top, mesh between. **Hen-type mesh used for the goats.**
- Water: taps with **wide 40 L tubs, two per pen**, on the long walls.
- Lights: **3 LED lines** (middle + both sides).
- **Switchback ramp**: from the middle, up to a corner landing at mid-height, then to the top middle.
- All blue gutters and troughs removed.

## Hen level (under the goat floor)

- Under-floor sheet slopes from the middle down to about **6 ft at the sides** (can't go lower without losing drainage slope).
- Brick wall about 3.15 ft, then **fine sand-filter mesh** (cheap) up to the sheet.
- **Hen door at the front (ramp) end wall**, in the bay next to the X-brace. Goat ramp goes to one side, hen entry the other.
- Steel supports under the chicken roof (under-sheet) added.
- **3 LED lines**, wall fans, nest boxes, feeders, drinkers.
- Summer: poly cover all round, mini fan-pad later (not in estimate). Rainy season: shade nets.

## Roof cooling

- Dried paddy straw on the roof (owner's plan, not in estimate).
- **Roof sprinklers** / drip line along the ridge, fed from the tank (in estimate).
- **Roof tie-down pipes (v37):** 5 lines of ½ in GI pipe along the full 77 ft roof: one on the ridge, two on each slope (9 ft and 18 ft from the ridge), each sitting over a purlin. J-bolts every 3 ft go through the pipe and the sheet crest into the purlin, with GI + rubber washers and sealant. They clamp the sheets against wind uplift and stop the paddy straw sliding off.

## Water tank and store room

- **20,000 L tank on a 16 ft stand** (enough head to fill the goat-level tubs).
- Walls between the stand pillars make a **store room**; door faces the front; **batteries kept inside**.
- Position: **south (back) end, beside the east side**, same alignment as the shed, ramp and hen way kept clear.
- Fed from a **borewell** (assumed 300 ft) with a submersible pump.

## Yard, fence, gate, road

- **6 ft mesh fence around the farm yard only** (about 510–522 ft), following the land boundary on the west.
- **Main gate at the west edge**, front side.
- **Access road** (about 134 ft) through the neighbour's strip to the main road. We only have road rights there.

## Cost estimate (Nov 2026)

| Section | Amount (₹) |
|---|---:|
| 1 Foundation & concrete | 6,44,890 |
| 2 Steel frame | 13,87,748 |
| 3 Roof and sheets | 2,25,048 |
| 4 Goat floor and walls | 5,37,200 |
| 5 Hen level | 1,39,835 |
| 6 Fans and lights | 1,86,600 |
| 7 Labour (daily wages) | 6,85,624 |
| 8 Water, borewell, sprinklers | 2,80,400 |
| 9 Tank stand and store room | 2,69,250 |
| 10 Yard fence, gate, access road | 1,81,170 |
| 11 Engineer | 1,40,000 |
| 12 Labour for yard works | 1,08,912 |
| **Subtotal** | **47,86,677** |
| Contingency 10% | 4,78,668 |
| **Total** | **52,65,345** (about ₹1,404 per sq ft) |

- Excluded: solar and batteries, oil palm, fence on the rest of the land, fan-pad, straw cover, electricity connection and borewell permission fees, land filling (done).
- Owner is the engineer: removing section 11 saves about ₹1.54 lakh with contingency.
- Full itemised list: `docs/cost-estimate.md` and `data/cost-estimate-boq.csv`.

## 3D / VR model: how it works

- Single HTML file, Three.js r128 from cdnjs, WebXR for the Quest. `index.html` in this repo is the live version (v37).
- Units: metres inside, shown in feet. Height marks in feet everywhere.
- Controls: drag to rotate, scroll/pinch to zoom; control panel starts collapsed; viewpoints; in VR, teleport with controllers.
- Layer groups can be turned on/off: land, tank, dimensions, electrical, bracing, foundation, roof, frame, floor, ramp, under-sheet, poultry, environment, pens.
- Animals are instanced (realistic goats and hens) for speed.
- Key numbers in the code: `FL=11.5` (goat floor), `o=0.85`, `WH` goat wall, `PW` pen width, `WW` walkway, tank `TX, TZ, TH=16`, yard fence `FX1, FZ0`, `LAND` polygon.
- To update: edit `index.html`, push to `main`; GitHub Pages republishes in about a minute; refresh on the Quest.

## Version history (versions/ folder)

- v00: original model from the old account. v01–v37: each change in order:
  feet height marks → plastic floor sheet → levels raised then lowered → hen door moved → blue gutters removed → realistic animals → switchback ramp → 6 pens with 1.5 ft walkways → L-shaped end feeders → mesh types → taps and wide tubs → fans in roof → 7 ft goat clear → steel under-sheet supports → 3 light lines per level → 20,000 L tank + store room → tank to edge, batteries inside → yard fence and gate → full land from Google trace → shed 10 ft from west → tank to the south end (v36) → 5 roof tie-down pipes (v37, current).

## Open checks before building

- Have the steel sizes and foundation checked against wind (44 m/s) and load.
- Under-floor sheets span 12.5 ft between beams: add purlins or use metal sheets.
- Roof uplift: strong anchor bolts and piles that resist pull-out.
- Many 900 mm BLDC wall fans are 230 V AC inside; confirm the supply type.
- Get local quotes for all "assumed" rates; borewell depth decides that cost.
