# Natural Flags

You can configure these flags inside your config.yml file. Options: default\_list, display\_list\
Wilderness flags can be edited in the `/lands admin menu` menu.

**Reset flag(s) to their defined state from config.yml:**

> /Lands admin land \<land | \*> resetFlag \<flag | all>\
> Keep in mind that changing flags in the configuration files requires a server reload / restart.

* **ENTITY\_GRIEFING**\
  Allow entities to grief blocks?
* **TNT\_GRIEFING**\
  Allow tnt to destroy blocks?
* **PISTON\_GRIEFING**\
  Allow pistons from a wilderness to push into the area?\
  This should be set to false, since it protects against griefing from other players.
* **MONSTER\_SPAWN**\
  Should monsters spawn? This does not include spawners by default.\
  To include spawners, you need to enable the include-spawners option.
* **PHANTOM\_SPAWN**\
  Should phantoms spawn? This does not include spawners by default.\
  To include spawners, you need to enable the include-spawners option.
* **ANIMAL\_SPAWN**\
  Should animals spawn? This does not include spawners.
* **WATERFLOW\_ALLOW**\
  Allow water to flow? This should be set to false, since it protects against griefing from other players.
* **FIRE\_SPREAD**\
  Should fire spread? Fire can not spread from wilderness into lands, even without this flag being set.
* **LEAF\_DECAY**\
  Should leaves decay?
* **PLANT\_GROWTH**\
  Should plants (including trees) grow?
* **SNOW\_MELT**\
  Should snow and ice be able to melt?
* **BLOCK\_SPREADING**\
  Should blocks, such as amethyst blocks be able to spread into an area? This only affects blocks that are spreading from an area that is part of the same land. Blocks from the wilderness can never spread into claims, regardless of whether this flag is set or not.

## Other Land Flags

These flags might not appear in the natural flag's menu. Instead, they usually have their own menu, where they can be toggled directly.

* **TITLE\_HIDE**\
  Hide the land enter title?
* **REQUEST\_ACCEPT**\
  Automatically accept new membership requests?

## Config

Here can add new flags.

```
  # Natural flags configuration. Role flags can be configured in the roles.yml file.
  # List of available landFlags: https://github.com/Angeschossen/Lands/wiki/Natural-Flags
  # NOTE: This option requires server reload / restart.
  land-flags:
    # Configure DEFAULT natural flags which will apply to new land creations.
    default_list:
      - monster_spawn
      - phantom_spawn
      - animal_spawn
      - leaf_decay
      - plant_growth
      - snow_melt

    # Natural flags which should be visible in the flags menu.
    display_list:
      - entity_griefing
      - tnt_griefing
      - piston_griefing
      - monster_spawn
      - phantom_spawn
      - animal_spawn
      - waterflow_allow
      - fire_spread
      - leaf_decay
      - plant_growth
      - snow_melt
```
