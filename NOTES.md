# MASTER FRAME ASSEMBLY — SIH 26030

## Established baseline
- Entry point: `main.kcl`. Continue this assembly in all later stages; preserve accepted components and datums unless mechanical compatibility requires a change.
- Authoritative dimensions: `parts/parameters.kcl`, exposed through `masterParameters.kcl`. Geometry families and individual frame/interface parts are in `parts/`; installed placement belongs to `main.kcl`.
- Closed, installed solid envelope: 2000 X × 800 Y × 1700 Z mm. Origin is the front-left floor corner. +X is process flow, +Y points rearward, +Z upward.
- Cable datum: Y = 300 mm, Z = 900 mm. Prototype diameter range: 5–40 mm. `cableDatum` is a non-solid construction reference, not a modeled cable.
- Frame: nominal 40 × 40 × 3 mm square hollow members, deck top Z = 750 mm, elevated rails top Z = 790 mm, interface plate top Z = 798 mm. Hollow tubes are generic fabricated members, not a vendor-specific T-slot profile.
- Eleven station plates: 120 × 360 × 8 mm; four Ø9 mm through-holes on 90 × 280 mm pitch. Holes are above the deck with underside clearance. Final module adapter and attachment details remain to be specified.

## Station reservations
All horizontal station plate centers use Y = 300, Z = 794 mm. Coordinates are provisional interfaces to preserve during subsequent module design.

| Reservation | X center, mm |
|---|---:|
| Reel/pay-off | 130 |
| Motorized feed | 290 |
| Eight-roller straightener | 480 |
| Diameter/geometry sensor | 650 |
| Precision clamp | 790 |
| Circumferential cutter | 950 |
| Longitudinal stripping | 1130 |
| Flattening/transfer | 1300 |
| Type-1/Type-2 dumbbell punch | 1510 |
| Ejection | 1710 |
| Vision station / camera | 1850 |

Additional camera upright: center (1850, 601, 1180) mm, vertical pierced plate. LED interface: center (1850, 455, 1399) mm, horizontal pierced plate supported by the mast arm. Neither camera nor light is modeled.

## Enclosure and controls
- Separate transparent polycarbonate-intent panels, two framed front doors, removable rear bays, roof and side panels. Left entry opening Ø60 mm is centered on the cable datum.
- Yellow open-ended internal hoods reserve feed, cutting/stripping, and punch protection. Outer enclosure is the intended primary barrier; hoods are not independently closed safety guards.
- Two door-interlock mounting locations and fixed-side support bridges are modeled, not selected or functioning interlocks.
- Front-right HMI is a nominal 9–10 inch packaging placeholder, with a true aperture in the door glazing and a rear mounting crossbar. Manufacturer-specific cutout, connectors and door cable routing remain open.
- Red/yellow emergency-stop geometry marks an accessible front-right location, not an installed validated safety circuit.
- Empty control cabinet envelope: X 1300–1940, Y 20–720, Z 140–680 mm. Removable skins, front cover, latch, mounting backplate and stand-offs are separate bodies.
- Backplate planning zones (not modeled electronics): lower band for supply/drives, middle band for PLC/safety relay/terminals, upper band for edge computer. Final selections, heat dissipation, wiring space and segregation must be checked.
- Separate pneumatic backplate centered (1160, 704, 410) mm, supported from the frame and accessed behind the removable rear cover. No manifold or pneumatic devices yet.

## Access and open engineering checks
- Reserve 350 mm external service space behind Y = 800 mm, extending to Y = 1150 mm; this is an installation allowance, not extra machine width or a guaranteed personnel-access width. Door opening space is additional and not included in the closed envelope.
- No processing modules, reels, rollers, cutters, dies, sensors, camera or LED have been generated. Module sizes and travel must be checked against the compact station pitch before installation; a full-size reel may require an external pay-off in a later compatible stage.
- Member loads, punch reaction, deflection, vibration, anchorage, lifting and foot capacity are not analyzed. The punch location is near the X = 1500 mm deck crossmember; local reinforcement may still be necessary.
- Guard gaps, cable-entry reach protection, door swing, seals, interlock actuation and safety circuits require formal design/risk review. Not safety-certified or production-ready.
- Joining, panel retention and hardware are preliminary. Generic head/shank representations have no helical threads. Complete fabrication holes, welds, tolerances and a purchase BOM after equipment selection.
- Repeated plate/tube/circular families use functions; their sketches are code-editable, not point-and-click editable inside function bodies.

## CAD verification
Final `main.kcl` execution passed without warnings/errors; the report identifies 64 fully constrained sketches and no under/over-constrained sketches. Frame parts, mounting plate, gusset, entry panel and door surround were also executed separately. Overview and focused views checked the station plates, cable entry, doors, HMI, emergency-stop location and rear layout. Interface holes, tube cores, gusset holes, cable-entry aperture and HMI glazing aperture use explicit subtraction; no cutter solids remain as substitute features. This is geometric CAD validation, not collision certification, FEA or safety validation.
