# SIH 26030 — persistent project memory

- Continue the **MASTER FRAME ASSEMBLY** in `main.kcl`; never replace it with a new machine in later steps.
- Preserve existing approved parts, dimensions, positions and interfaces unless necessary for mechanical compatibility; explain such changes.
- Dimensions live in `parts/parameters.kcl`; root `masterParameters.kcl` is the public parameter interface.
- Overall closed solids: 2000 × 800 × 1700 mm. Frame nominal 40 mm square hollow section. Datum origin: front-left floor corner; process +X, rear +Y, up +Z.
- Cable axis Y = 300 mm, Z = 900 mm. Diameter range 5–40 mm. Deck top 750 mm; module interface plate tops 798 mm.
- Station X centers: 130, 290, 480, 650, 790, 950, 1130, 1300, 1510, 1710, 1850 mm, in requested process order. See `NOTES.md` for names and interface details.
- This stage creates frame/enclosure/guards/control-space and mounting infrastructure ONLY. Future processing modules are intentionally absent.
- Use separate bodies and part definitions, not an all-machine boolean union. Placement belongs in `main.kcl`.
- Plan 350 mm external rear service allowance; keep it outside the 800 mm machine envelope.
- HMI and emergency stop are location/packaging placeholders. No safety certification or structural-load validation has been performed.
- Last execution: successful, 64 fully constrained sketches, no warnings/errors.
