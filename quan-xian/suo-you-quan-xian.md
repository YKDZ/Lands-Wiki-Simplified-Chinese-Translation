# 所有权限

To assign permissions to players you must install a permissions plugin, like Luckperms. Below you find a list of permissions that you can assign to players or their permission groups. Please note that if a player has /op, they will have all permissions.

## Recommended Permission Setup

You can find a recommended permission setup for players here: [Recommended Permission Setup](https://github.com/Angeschossen/Lands/wiki/Recommended-Permission-Setup)

## Player Permissions

These permissions are safe to set for your players.

### Numbered Permissions

IMPORTANT:

* **Replace `<number>` with an actual number.** Example: `lands.lands.<number>` -> lands.lands.5
* If you make changes to numbered permissions and want to synchronize these changes to lands of which the owners are offline: Execute `/lands admin land * syncPermissions`. Please note that this is not required. Without executing this command, the limits will automatically update if the land owner is online or once the land owner logs in again.

#### Stacked Numbered Permissions

By default the highest numbered permission that a player has will define the limit. You can change this by enabling the `permission-stacking` option in the `config.yml` file. This will accumulate each limit. Example: A player has lands.lands.5 and lands.lands.4 set. This would result in lands.lands.9.

#### Numbered Permission Nodes

`lands.lands.<number>`\
Example: lands.lands.5\
Description: In how many lands can the player be a member?\
NOTE: This does not include owned lands. If you want to set\
how many lands the player can own, just set the permission below (lands.ownlands.).

`lands.ownlands.<number>`\
Example: lands.ownlands.2\
Description: How many lands can the player own?

`lands.chunks.<number>`\
Example: lands.chunks.75\
Description: How many chunks should the player be\
able to claim? This is per land.

`lands.chunks.support.<number>`\
Example: lands.chunks.support.5\
Description: How many chunks can the player contribute to lands he's member of? Example: lands.chunks.support.5 -> each land in which the player is trusted and not owned by the player, will receive an additional amount of 5 claims.

`lands.members.<number>`\
Example: lands.members.20\
Description: Set max members per land. This includes the owner.

`lands.areas.<number>`\
Example: lands.areas.30\
Description: Set max "sub areas" per land.

`lands.roles.<number>`\
Example: lands.roles.10\
Description: Set max roles per land.

`lands.rentals.<number>`\
Example: lands.rentals.1\
Description: Allow the player to rent or buy an amount of areas per land. If set to 0, the player won't be able to rent or buy any areas. If set to 1, the player will only be able to rent or buy one area per land. And so on.

`lands.parts.<number>`\
Example: lands.parts.10\
Description: Set the max. amount of disconnected parts for the players owned lands. This includes the initial claim. So setting `lands.parts.1`, won't do anything. This will only take effect, if the option `treat-as-new` is disabled in config.yml. This permission allows players to claim a collections of chunks that are disconnected from the original land, but the `force-near` option will still be enforced once the maximum amount is reached.

`lands.free.chunks.<number>`\
Example: lands.free.chunks.10\
Description: The player can claim `<number>` chunks FOR FREE for each land they own. If they already claimed `<number>` of chunks this won't have any effect. Please note that an amount of chunks, depending on the "claim-radius" option in config.yml, will always be free. No matter, if this permission has been set or not.

`lands.free.lands.<number>`\
Example: lands.free.lands.1\
Description: Set free lands amount (/Lands create).

`lands.selection.<number>`\
Example: lands.selection.1000\
Description: Max chunks amount for /Lands selection. The default value is 1000.

`lands.camps.<number>`\
Example: lands.camps.3\
Description: Maximum amount of camps.

`lands.allies.<number>`\
Example: lands.allies.3\
Description: Maximum amount of allies per land / nation.

`lands.enemies.<number>`\
Example: lands.enemies.3\
Description: Maximum amount of enemies per land / nation.

`nations.lands.<number>`\
Example: nations.lands.10\
Description: Defines how many lands can be part of the nation of this player.

### Command Permissions

Commands wiki page: https://github.com/Angeschossen/Lands/wiki/Commands

### Teleportation

The following permissions limit all teleportation initiated by Lands. Players have them by default. However, in some cases the teleportation is initiated by executing a command. In such case they need the permission to use the command as well. You don't need to explicitly set them.

#### Disabling Teleportation

If you want to disable a teleportation you need to unset the permission in your permissions plugin. Example for LuckPerms: `/luckperms group default permission set lands.teleport.sub_area false` The value `false` is important here.

#### Teleportation Permissions

`lands.teleport.chunk`\
Description: Allow teleportation to claimed chunks via /lands claimlist.\
Note: This permission is set by default.

`lands.teleport.rentable`\
Description: Allow teleportation to rentable areas or lands setup for purchase.\
Note: This permission is set by default.

`lands.teleport.land_spawn`\
Description: Allow to teleport to a land spawn.\
Note: This permission is set by default.

`lands.teleport.random_teleport`\
Description: Allow to random teleport via /lands wild.\
Note: This permission is set by default.

`lands.teleport.war`\
Description: Allow to teleport to war spawn via /wars spawn.\
Note: This permission is set by default.

`lands.teleport.sub_area`\
Description: Allow to teleport to a sub area.\
Note: This permission is set by default.

`lands.teleport.unstuck`\
Description: Allow to teleport via /lands unstuck.\
Note: This permission is set by default.

### Toggle Natural Flags

These permissions are needed to toggle natural flags like monster spawning for your land.

```
      lands.setting.*:
        description: Allow players to toggle natural flags.
        children:
          lands.setting.entity_griefing:
            description: Allow to toggle entity griefing
          lands.setting.block_spreading:
            description: Allow to toggle block spreading
          lands.setting.phantom_spawn:
            description: Allow to toggle phantom spawning
          lands.setting.piston_griefing:
            description: Allow to toggle piston griefing
          lands.setting.monster_spawn:
            description: Allow to toggle monster spawn
          lands.setting.animal_spawn:
            description: Allow to toggle animal spawn
          lands.setting.waterflow_allow:
            description: Allow to toggle waterflow
          lands.setting.tnt_griefing:
            description: Allow to toggle tnt griefing
          lands.setting.fire_spread:
            description: Allow to toggle fire spread
          lands.setting.leaf_decay:
            description: Allow to toggle leaf decay
          lands.setting.plant_growth:
            description: Allow to toggle plant growth
          lands.setting.snow_melt:
            description: Allow to toggle snow melt
          lands.setting.wither_attack_animal:
            description: Allow to toggle wither attack animal
```

### Toggle Role Flags

These permissions are needed to toggle role flags for your land.

```
      lands.role.setting.*:
        description: Allow players to toggle all role flags.
        children:
            lands.role.setting.block_break:
              description: Allow players to toggle the 'block_break' flag.
            lands.role.setting.block_place:
              description: Allow players to toggle the 'block_place' flag.
            lands.role.setting.harvest:
              description: Allow players to toggle the 'harvest' flag.
            lands.role.setting.attack_player:
              description: Allow players to toggle the 'attack_player' flag.
            lands.role.setting.attack_animal:
              description: Allow players to toggle the 'attack_animal' flag.
            lands.role.setting.block_ignite:
              description: Allow players to toggle the 'block_ignite' flag.
            lands.role.setting.interact_general:
              description: Allow players to toggle the 'interact_general' flag.
            lands.role.setting.interact_door:
              description: Allow players to toggle the 'interact_door' flag.
            lands.role.setting.interact_container:
              description: Allow players to toggle the 'interact_container' flag.
            lands.role.setting.interact_mechanism:
              description: Allow players to toggle the 'interact_mechanism' flag.
            lands.role.setting.interact_villager:
              description: Allow players to toggle the 'interact_villager' flag.
            lands.role.setting.fly:
              description: Allow players to toggle the 'fly' flag.
            lands.role.setting.land_enter:
              description: Allow players to toggle the 'land_enter' flag.
            lands.role.setting.player_trust:
              description: Allow players to toggle the 'player_trust' flag.
            lands.role.setting.player_untrust:
              description: Allow players to toggle the 'player_untrust' flag.
            lands.role.setting.player_setrole:
              description: Allow players to toggle the 'player_setrole' flag.
            lands.role.setting.land_claim:
              description: Allow players to toggle the 'land_claim' flag.
            lands.role.setting.land_claim_border:
              description: Allow players to toggle the 'land_claim_border' flag.
            lands.role.setting.spawn_set:
              description: Allow players to toggle the 'spawn_set' flag.
            lands.role.setting.spawn_teleport:
              description: Allow players to toggle the 'spawn_teleport' flag.
            lands.role.setting.balance_withdraw:
              description: Allow players to toggle the 'balance_withdraw' flag.
            lands.role.setting.area_assign:
              description: Allow players to toggle the 'area_assign' flag.
            lands.role.setting.setting_edit_land:
              description: Allow players to toggle the 'setting_edit_land' flag.
            lands.role.setting.setting_edit_role:
              description: Allow players to toggle the 'setting_edit_role' flag.
            lands.role.setting.setting_edit_taxes:
              description: Allow players to toggle the 'setting_edit_taxes' flag.
            lands.role.setting.vehicle_use:
              description: Allow players to toggle the 'vehicle_use' flag.
            lands.role.setting.attack_monster:
              description: Allow players to toggle the 'attack_monster' flag.
            lands.role.setting.ender_pearl:
              description: Allow players to toggle the 'ender_pearl' flag.
            lands.role.setting.interact_trapdoor:
              description: Allow players to toggle the 'interact_trapdoor' flag.
            lands.role.setting.item_pickup:
              description: Allow players to toggle the 'item_pickup' flag.
            lands.role.setting.land_rename:
              description: Allow players to toggle the 'land_rename' flag.
            lands.role.setting.player_ban:
              description: Allow players to toggle the 'player_ban' flag.
            lands.role.setting.setting_edit_various:
              description: Allow players to toggle the 'setting_edit_various' flag.
            lands.role.setting.trample_farmland:
              description: Allow players to toggle the 'trample_farmland' flag.
            lands.role.setting.war_manage:
              description: Allow players to toggle the 'war_manage' flag.
```

### Toggle Personal Flags

```
      lands.player.setting:
        description: Allow players to toggle all personal flags.
        children:
          lands.player.setting.enter_messages:
            description: Allow players to toggle the 'enter_messages' flag.
          lands.player.setting.receive_invites:
            description: Allow players to toggle the 'receive_invites' flag.
          lands.player.setting.show_inbox:
            description: Allow players to toggle the 'show_inbox' flag.
```

### Playtime Max Rewards

**Only needed if playtime rewards are enabled in the config.**

```
      lands.chunks.max.<number>:
        description: The player wont be able to get any chunks rewarded if his current lands.chunks.<number> permission is equal or higher.
      lands.ownlands.max.<number>:
        description: The player wont be able to get any land creations rewarded if his current lands.ownlands.<number> permission is equal or higher.
      lands.lands.max.<number>:
        description: The player wont be able to get any land joins rewarded if his current lands.lands.<number> permission is equal or higher.
      lands.members.max.<number>:
        description: The player wont be able to get any member limit rewarded if his current lands.members.<number> permission is equal or higher.
      lands.chunks.support.max.<number>:
        description: The player wont be able to get any support chunks rewarded if his current lands.chunks.support.<number> permission is equal or higher.
```

## Staff Permissions

These permissions should only be set for your staff.

### Bypass Permissions

```
      lands.bypass.*:
        description: Bypass all protections and other restrictions
        children:
          lands.bypass.block_break:
            description: Bypass block break protection
          lands.bypass.block_place:
            description: Bypass block place protection
          lands.bypass.block_ignite:
            description: Bypass block ignite protection
          lands.bypass.interact_general:
            description: Bypass interaction protection
          lands.bypass.interact_mechanism:
            description: Bypass interaction protection
          lands.bypass.interact_door:
            description: Bypass interaction protection
          lands.bypass.interact_container:
            description: Bypass interaction protection
          lands.bypass.interact_villager:
            description: Bypass villager protection
          lands.bypass.attack_animal:
            description: Bypass animal attack protection
          lands.bypass.attack_player:
            description: Bypass player attack protection
          lands.bypass.member.untrust:
            description: Untrust players or remove invites in other lands
          lands.bypass.fly:
            description: Bypass fly flag
          lands.bypass.worldedit:
            description: Bypass WorldEdit restrictions in other players lands
          lands.bypass.land_enter:
            description: Bypass land enter flag
          lands.bypass.selection:
            description: Bypass error message of other plugin cancelling selection
            
          lands.bypass.wilderness.*:
            description: Bypass all wilderness protections (for worlds in disallow-wilderness_list)
            children:
              lands.bypass.wilderness.block_break:
                description: Bypass block break protection for disallow-wilderness_list in config
              lands.bypass.wilderness.block_place:
                description: Bypass block place protection for disallow-wilderness_list in config
              lands.bypass.wilderness.block_ignite:
                description: Bypass block ignite protection for disallow-wilderness_list in config
              lands.bypass.wilderness.interact_general:
                description: Bypass interaction protection for disallow-wilderness_list in config
              lands.bypass.wilderness.interact_mechanism:
                description: Bypass interaction protection for disallow-wilderness_list in config
              lands.bypass.wilderness.interact_door:
                description: Bypass interaction protection for disallow-wilderness_list in config
              lands.bypass.wilderness.interact_container:
                description: Bypass interaction protection for disallow-wilderness_list in config
              lands.bypass.wilderness.attack_animal:
                description: Bypass animal attack protection for disallow-wilderness_list in config
              lands.bypass.wilderness.attack_player:
                description: Bypass player attack protection for disallow-wilderness_list in config
              lands.bypass.wilderness.worldedit:
                description: Bypass WorldEdit restrictions in wilderness.
              lands.bypass.wilderness.fly:
                description: Fly in wilderness

          lands.bypass.cooldown.*:
            description: Bypass cooldowns
            children:
              lands.bypass.cooldown.wild:
                description: Bypass /lands wild cooldown
              lands.bypass.cooldown.rename:
                description: Bypass /lands rename cooldown
              lands.bypass.cooldown.teleport:
                description: Bypass chunk teleport cooldown
              lands.bypass.cooldown.spawn:
                description: Bypass /lands spawn cooldown
              lands.bypass.cooldown.unstuck:
                description: Bypass /lands unstuck cooldown

          lands.bypass.spawn.private:
            description: Teleport to private land spawns

          lands.bypass.war.*:
            description: Bypass war restrictions
            children:
              lands.bypass.war.trust:
                description: Trust players during war.
              lands.bypass.war.claim:
                description: Claim during war.

          lands.bypass.option.*:
            description: Bypass special config options.
            children:
              lands.bypass.option.force-near:
                description: Bypass force-near option from config.

          lands.bypass.cmd.untrusted.*:
            description: Bypass blacklisted commands for untrusted players from config.yml. Use lands.bypass.cmd.untrusted.COMMAND to specify a command.
          lands.bypass.cmd.general.*:
            description: Bypass blacklisted commands for untrusted and trusted players from config.yml. Use lands.bypass.cmd.general.COMMAND to specify a command.
          lands.bypass.priority:
            description: Edit roles even if they have the same or a higher priority than your own role.
          lands.bypass.expiration:
            description: This permission only works when you use Luckperms as your permission plugin. Players with this permission will bypass the configured land expiration from your config.

          lands.bypass.teleport.*:
            description: Bypass teleport restrictions.
            children:
              lands.bypass.teleport.delay:
                description: Skip teleport delay.
              lands.bypass.teleport.cmd:
                description: Execute commands during teleportation.
```

### Moderator Utilities

```
      lands.mod.*:
        description: Access to all moderator actions.
        children:
          lands.mod.command.*:
            description: Access to all moderator commands.
            children:
              lands.mod.command.chatspy:
                description: /Lands chatspy
```

## Administrator Permissions

These permissions should only be set for administrators.

```
      lands.admin.*:
        description: Access to all admin actions. Commands require execution of /Lands edit <land> (to select the land).
        children:
          lands.admin.disabled-features:
            description: Allow to use disabled features such as setting areas up for rental.
          lands.admin.land_edit:
            description: Allow to edit other lands via /lands edit. This may also ignore requirements such as max members for some commands.
          lands.admin.land_delete:
            description: Allow to delete other lands or unclaim chunks from other lands.
          lands.admin.land_setowner:
            description: Allow the usage of /Lands setowner for lands the player doesn't own
          lands.admin.setting_edit_land:
            description: Edit land settings of other lands (like mob spawning etc.)
          lands.admin.setting_edit_role:
            description: Edit role settings of other lands.
          lands.admin.setting_edit_taxes:
            description: Edit taxes settings of other lands.
          lands.admin.command.*:
            description: Access to all admin commands
            children:
              lands.admin.command.reload:
                description: Access to /Lands reload
              lands.admin.command.wilderness:
                description: Open wilderness menu /Lands admin wilderness
              lands.admin.command.land.*:
                description: Access to admin land commands
                children:
                  lands.admin.command.land.delete:
                    description: Delete land
                  lands.admin.command.land.edit:
                    description: Open GUI for land
                  lands.admin.command.land.trust:
                    description: Trust players to land
                  lands.admin.command.land.untrust:
                    description: Untrust players from land
                  lands.admin.command.land.rename:
                    description: Rename land
                  lands.admin.command.land.settings.reset:
                    description: Reset settings of land
                  lands.admin.command.land.setowner:
                    description: Set new owner for land
              lands.admin.command.give.claimblock:
                description: Give claimblocks to player
              lands.admin.command.import:
                description: Import data from other plugins
              lands.admin.command.convert:
                description: Convert database

      nations.admin.*:
        description: Access to all Nations admin actions
        children:
          nations.admin.nation_edit:
            description: Edit other players nations of their lands from /lands edit
```
