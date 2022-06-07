# MCBE Vanilla Behavior Pack Changelog

**Note:** This changelog will only ever contain the changes from the latest released version or the latest preview, depending on the branch. For previous changelogs, see either the changelogs in [releases](https://github.com/CoalBuster/MCBEVanillaBehaviorPack/releases) or checkout the tag of the version.

For the full changelog, check the knowledge base section over at [feedback.minecraft.net](https://feedback.minecraft.net/hc/en-us/categories/115000410252-Knowledge-Base).

This changelog only discusses observed technical changes from the diff between versions. It is constructed in a best-effort kinda way; Certain changes may be over-looked as it is being put together manually.

Also note that sometimes assumptions could be made, as official information is often missing. For the absolute truth (but possibly undocumented), refer to the official docs. Read with care.

## MCBE Release 1.18.30

### Entities

#### Format Version 1.18.20

- New component `minecraft:exhaustion_values` (type: object) with parameters:
  - `heal`: double
  - `jump`: double
  - `sprint_jump`: double
  - `mine`: double
  - `attack`: double
  - `damage`: double
  - `walk`: double
  - `sprint`: double
  - `swim`: double

- New component `minecraft:behavior.celebrate_survive` (type: object) with parameters:
  - `priority`: integer
  - `duration`: double
  - `fireworks_interval`: object
    - `range_min`: double
    - `range_max`: double
  - `on_celebration_end_event`: Trigger

- New component `minecraft:behavior.move_outdoors` (type: object) with parameters:
  - `priority`: integer
  - `speed_multiplier`: double
  - `timeout_cooldown`: double

- New component `minecraft:behavior.work_composter` (type: object) with parameters:
  - `active_time`: integer
  - `speed_multiplier`: double
  - `goal_cooldown`: integer
  - `can_work_in_rain`: boolean
  - `work_in_rain_tolerance`: integer
  - `on_arrival`: Trigger

- Added parameter to component `minecraft:player.exhaustion`:
  - `max`: integer

- Added parameter to component `minecraft:player.saturation`:
  - `max`: integer

- Added parameter to `items`-array object of component `minecraft:shareables`:
  - `pickup_only`: boolean

- Changed parameter value of component `minecraft:behavior.go_home`:
  - `on_home`: ~~object~~ -> array
