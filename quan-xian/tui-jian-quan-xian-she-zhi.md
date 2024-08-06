# 推荐权限设置

This page is a list of recommended permissions for players on your server. Please note that this is a general recommendation and might not reflect your server's needs. Also, most features of Lands can be disabled. Therefore, this recommendation might include permissions that are not required for your setup.

## Numbered Permissions

* It's recommended that every server set's all numbered permissions listed, if the server wants to use all features.
* You'll need to go through them and decide which numbers (max. lands etc.) you want to set.

_View all permissions:_ [_Link_](https://github.com/Angeschossen/Lands/wiki/Permissions#numbered-permissions)

## Command Permissions

* `lands.command.*`\
  Description: That gives players access to all player related commands. If you want to remove some commands, you either need to negate the specific command permission or you need to set each command permission specifically.\
  _View all permissions:_ [_Link_](https://github.com/Angeschossen/Lands/wiki/Commands)
* `nations.command.*`\
  Description: Use all player related `/nations <cmd>` commands.\
  _View all permissions:_ [_Link_](https://github.com/Angeschossen/Lands/wiki/Commands#nations)
* `wars.command.*`\
  Description: Allow players to use all player related `/wars <cmd>` commands.\
  _View all permissions:_ [_Link_](https://github.com/Angeschossen/Lands/wiki/Commands#wars)

## Teleportation

`lands.teleport.*`\
Description: This allows players to teleport to individual claimed chunks of their land etc. This does not include spawn teleportation, as this is covered by `lands.command.spawn`. If you want to limit teleportation, you'll need to set permissions accordingly.

_View all permissions:_ [_Link_](https://github.com/Angeschossen/Lands/wiki/Permissions#teleportation)

## Toggle Role Flags

`lands.role.setting.*`\
Description: This allows players to toggle all role flags for their land.

_View all permissions:_ [_Link_](https://github.com/Angeschossen/Lands/wiki/Permissions#toggle-role-flags)

## Toggle Natural Flags

`lands.setting.*`\
Description: This allows players to toggle all natural flags (like monster spawning etc.) for their land.

_View all permissions:_ [_Link_](https://github.com/Angeschossen/Lands/wiki/Permissions#toggle-natural-flags)

## Toggle Personal Flags

`lands.player.setting.*`\
Description: Allow players to toggle all their personal flags.

_View all permissions:_ [_Link_](https://github.com/Angeschossen/Lands/wiki/Permissions#toggle-personal-flags)

## List of recommended Permissions for regular Players

This list isn't meant to be a standard. Each server is different. This is just an example.

### Numbered Permissions

If you want to enforce players playing together and not join multiple lands, while having their own, the `invite-owner` can be set to `false` in config.yml. So a player can only own a land or be part trusted in a number of lands. It's no problem at all to allow players being part of many lands and own their own too. You don't need to set this option to false. It's up to you.

* lands.camps.1 - This let's them create 1 camp.
* lands.lands.2 - They can be trusted in 2 lands.
* lands.ownlands.2 - They can own 2 lands.
* lands.chunks.100 - They can claim at least 100 chunks per land that they own. They might be able to claim more depending on the permission node `lands.chunks.support.<number>` (node explained below) or level attributes (configureable in `levels.yml`.
* lands.chunks.support.5 - they increase the claim limit by 5 in lands they're trusted.
* lands.members.25 - They can have trusted players for each land they own.
* lands.areas.50 - They can create 50 sub areas for each land they own.
* lands.roles.100 - They can create 100 roles for each area in lands they own.
* lands.rentals.1 - They can rent or buy one area per land.
* lands.allies.10 - Lands that they own, can have 10 allies.
* lands.enemies.10 - Lands that they own, can have 10 enemies.
* nations.lands.10 - A nation, of which the capital is a land they own, can add 10 lands.

### Command Permissions

* lands.command.\*
* wars.command.\*
* nations.command.\*

### Teleportation

* lands.teleport.\*

### Toggle Flags

* lands.setting.\*
* lands.role.setting.\*
* lands.player.setting.\*
