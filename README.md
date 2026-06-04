# Engantor

A personal ModuleManager config pack for a **Realism Overhaul / RP-1** install of
Kerbal Space Program (RSS, KSP 1.12.x). It adds RP-1 career, Realism Overhaul,
Kerbalism, and Waterfall support for a number of part mods that don't ship it,
plus assorted bug-fix patches.

All files are ModuleManager `.cfg` patches — drop the folder in `GameData/` and
they apply automatically. Nothing here contains models or textures; it's
patches only, layered on top of the mods listed below.

## File naming convention

| Prefix | Purpose |
|--------|---------|
| `rp1-*` | RP-1 tech-tree placement, costs, avionics, `RP0conf` |
| `ro-*` | Realism Overhaul propellants, masses, engine/tank conversions |
| `kerbalism-*` | Kerbalism / ROKerbalism life-support resources |
| `fix-*` | Bug fixes & mod-interaction patches (nodes, RSSROConfig, propellants, etc.) |
| `waterfall-*` | Waterfall plume configs |
| `deferred-*` | Deferred-rendering shader fixes |
| `patch-*` | One-off part tweaks |
| `vaborganizer-*` | VAB Organizer category configs |

## Mods covered

Artemis Construction Kit (Benjee10 Orion/SLS), Space Shuttle System
(giuliodondi), PEKKAsMods (Falcon/Electron/Alpha/Vulcan/Starship/Helios/Psyche),
EDBMods FutureTech + New Glenn, KNES, HabTech2 + htRobotics, ISAQuestBlueMoon,
Near Future Technologies (Solar/Propulsion/Spacecraft/Construction/Electrical/
Exploration), Bluedog Design Bureau, Tantares, SSPX, Launchers Pack, Canadarm,
Modular RCS, and others.

## Notes

- Several patches work around the **ROEngines engine-consolidation** behaviour,
  which deletes non-`ROE-*` parts that share an `engineType` with its own engines
  (SSME, AJ10, R4D11, Raptor). The fix is to strip the `engineType` tag after the
  engine config is baked in.
- Avionics `massLimit` values are sized to each vehicle's real stack mass.
- Life-support quantities follow the ROKerbalism per-crew consumption profile.
