# LuckPerms 上下文

If you have Luckperms installed you can give players permission in specific Lands areas. Download: https://www.spigotmc.org/resources/28140

Available contexts exclusively for Luckperms:\
Please keep in mind that land and area names are case-sensitive.

#### LuckPerms Context

The following context entries can also be used for a player's current location by just appending `_here` to the entry. Example: `lands_land_name_here`.

> `lands_land_name=landname`\
> Description: Returns land name or `wilderness`. Append `_here` to get the result, for the land at the player's current position.

> `lands_land_area_name=areaname`\
> Description: Returns area name or `wilderness`. Append `_here` to get the result, for the area at the player's current position.

> `lands_land_area_role_name=rolename`\
> Description: Returns the name of the player's role.

> `lands_land_bool=true or false`\
> Description: Returns true, if the player owns or is part of a land. If you append `_here`, it will return true, if the player's current position is claimed.

> `lands_land_trusted_bool=true or false`\
> Description: Returns true, if the player is trusted. Append `_here` to get the result for the land at the player's current position.

> `lands_combat_tag_bool=true or false`\
> Description: Returns whevter or not the player is in combat.

> `lands_land_level=number`\
> Description: Set permission if land has level x. You can append `_here` too.

> `lands_nation_level=number`\
> Description: Set permission if nation has level x. You can append `_here` too.

#### Others

> `lands_trusted_in=landname`\
> Description: Check if a player is trusted in a given land. Example: `lands_trusted_in=test`: The player will receive the permission if they own or are part of land "test".

#### Examples:

Giving a permission only if player is part of a specific land:\
`/lp user Luck permission set test.permission lands_trusted_in=test`

Giving a permission only in wilderness:\
`/lp user Luck permission set test.permission lands_land_name_here=wilderness`\
NOTE: You can also remove permission if they're in wilderness by setting a negated (-) permission.

Giving a permission only in claims where the player is trusted:\
`/lp user Luck permission set test.permission lands_land_trusted_bool=yes`
