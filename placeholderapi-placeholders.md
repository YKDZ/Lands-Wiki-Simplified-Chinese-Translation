# PlaceholderAPI Placeholders

### Display Placeholders for the Player's current Location

You can even display a placeholder for a player's current location, by just appending `_here` to it.

### Limit the Length of a Placeholder

Append `_length(<number>)` to the placeholder and replace `<number>` with a number of your choice.

### General

> **`%lands_lands%`**\
> Description: List of lands the player owns or is trusted in. Example: land1, land2

> **`%lands_lands_amount%`**\
> Description: Amount of lands the player owns and is trusted in.

> **`%lands_lands_own%`**\
> Description: List of lands the player owns. Example: ownland1, ownland2

> **`%lands_lands_own_amount%`**\
> Description: Amount of lands the player owns.

> **`%lands_lands_trusted%`**\
> Description: List of lands the player is trusted in, but doesn't own. Example: trustedland1, trustedland2

> **`%lands_lands_trusted_amount%`**\
> Description: Amount of lands the player is trusted in. This doesn't include owned lands.

> **`%lands_next_tax%`**\
> Description: Next tax payment round

> **`%lands_next_upkeep%`**\
> Description: Time until next upkeep payment.

> **`%lands_affiliation%`**\
> Description: Combination of land and nation name. You can edit the\
> format in your language file.

> **`%lands_affiliation_color%`**\
> Description: Get the color of the nation, the player is in. If the land\
> isn't part of any nation, the land color will be returned instead.

> **`%lands_land_bool%`**\
> Description: If you don't append \_here: returns true if player owns or is part of a land.\
> If you append \_here: returns true, if the chunk at the player's location is claimed.

> **`%lands_land_trusted_bool%`**\
> Description: Returns true, if the player is trusted in the area.

> **`%lands_limit_<permission>%`**\
> Description: Returns numbered permission value. Replace `<permission>` with any [numbered permission](https://github.com/Angeschossen/Lands/wiki/Permissions#numbered-permissions).\
> Example: lands.ownlands would return 5, if the player has lands.ownlands.5 as the maximum amount of owned lands.

> **`%lands_combat-tag%`**\
> Description: Whether or not the player has a combat tag.

> **`%lands_combat-tag_bool%`**\
> Description: Same as `%lands_combat-tag%`, but returns fixed values: true or false.

### Land

> **`%lands_land_name%`**\
> Description: Name of land

> **`%lands_land_name_plain%`**\
> Description: Name of land without any color or formatting.

> **`%lands_land_name_cmd%`**\
> Description: Get name of land that is used for commands. Basically, this replaces all spaces in the land name, with underscores and doesn't contain any color or format.

> **`%lands_land_owner%`**\
> Description: Owner name

> **`%lands_land_category%`**\
> Description: Name of the land's category.

> **`%lands_land_role%`**\
> Description: Role in land

> **`%lands_land_role_color%`**\
> Description: Get role color, which results of the role name.

> **`%lands_land_members%`**\
> Description: Amount of members in land

> **`%lands_land_members_online_amount%`**\
> Description: Amount of members of the land that are online.

> **`%lands_land_members_online%`**\
> Description: Names of the land members that are currently online.

> **`%lands_land_balance%`**\
> Description: Balance of the land.

> **`%lands_land_balance_short%`**\
> Description: Balance of the land in short format. This depends on the "general.eco-format.short-unit" option in config.yml.\
> Config:

```
    # The short format will use the normal format if the value is lower than 1000.
    # If the value is higher or equal than 1000, it will return {value} divided by 1000.
    # This format is only used by a small amount of messages.
    short: '${value}k'
```

> **`%lands_land_chunks%`**\
> Description: Land size

> **`%lands_land_chunks_max%`**\
> Description: Max claim amount for land

> **`%lands_land_chunks_remaining%`**\
> Description: Remaining possible claims for land

> **`%lands_land_tax%`**\
> Description: Tax value of land

> **`%lands_land_upkeep%`**\
> Description: Upkeep costs of land

> **`%lands_land_balance%`**\
> Description: Land balance

> **`%lands_land_chunk_cost_next%`**\
> Description: Cost value of next claim

> **`%lands_land_level%`**\
> Description: Name of the current level.

> **`%lands_land_level_index%`**\
> Description: Index of the current level. Example: 1

> **`%lands_land_level_next%`**\
> Description: Name of the next level.

> **`%lands_land_level_next_index%`**\
> Description: Index of the next level. Example: 1

> **`%lands_land_color%`**\
> Description: Get land color which comes from the name.

> **`%lands_land_id%`**\
> Description: ID of the land.

> **`%lands_land_area_name%`**\
> Description: Name of the subarea.

> **`%lands_land_area_name_plain%`**\
> Description: Name of the subarea without color.

> **`%lands_land_icon%`**\
> Description: Returns the type of the land's icon item. Will return "AIR", if there's no land.

### Nation

#### \_any Option

Display placeholders for any nation the player is in. So not just their current /edit land or the land at their position. Just append "\_any" to the placeholder, to display the information for any nation the player is in.

> **`%lands_nation_name%`**\
> Description: Nation name

> **`%lands_nation_name_plain%`**\
> Description: Name of nation without any color or formatting.

> **`%lands_nation_color%`**\
> Description: Get nation color which comes from the name.

> **`%lands_nation_level%`**\
> Description: Current level of the nation

> **`%lands_nation_level_index%`**\
> Description: Index of the current nation level. Example: 1

> **`%lands_nation_level_next%`**\
> Description: Next level of the nation

> **`%lands_nation_level_next_index%`**\
> Description: Index of the next nation level. Example: 1

> **`%lands_nation_shield%`**\
> Description: Get remaining shield time.

> **`%lands_nation_id%`**\
> Description: ID of the nation.

> **`%lands_nation_bool%`**\
> Description: If you don't append \_here: returns true if player owns or is part of a nation.\
> If you append \_here: returns true, if the chunk at the player's location belongs to a nation.

### War

> **`%lands_war_enemy%`**\
> Description: The enemy in current war.

> **`%lands_war_time%`**\
> Description: Remaining time of the current state (preparation or fight).

> **`%lands_war_state%`**\
> Description: The current state of the war (preparation or fight).

### Relation Placeholders

Placeholders that involve more than one player.

> **`%rel_lands_war_relation%`**\
> Description: Returns relation of two players (enemy, ally) during war. Returns an empty string while if the two players are not taking part in the same war.

> **`%rel_lands_relation%`**\
> Description: Returns relation of two players (enemy, ally, neutral) during war and while not in a war.

### Top Lands and Nations

Format: `%lands_top_<context>_<sorting>_<place>_<value>%`

#### Parameter Explanation

* `<context>` needs to be replaced with either `land` or `nation`.
* `<sorting>` needs to be replaced with `balance`, `chunks`, `members`, `level`, `ratio-kd` (kills/deaths in wars ratio) or `ratio-wl` (won/lost wars ratio).
* `<place>` needs to be replaced with the place. Example: `1`
* `<value>` needs to be replaced with name, owner, balance, size, members, ratio-kd or ratio-wl.
