# 命令

> `/lands`\
> `Permission: lands.command.menu`\
> Description: Open the menu.

> `/lands help [page]`\
> `Permission: lands.command.help`\
> Description: Display command usages of Lands.

> `/lands claim`\
> `Permission: lands.command.claim`\
> Description: Claim chunks.

> `/lands claim auto`\
> `Permission: lands.command.claim.auto`\
> Description: Claim chunks while walking.

> `/lands create`\
> `Permission: lands.command.create`\
> Description: Create a land.

> `/lands merge <land>`\
> `Permission: lands.command.merge`\
> Description: Merge a land (parameter) into your other land.

> `/lands accept <land>`\
> `Permission: lands.command.accept`\
> Description: Accept invites.

> `/lands chat [land] <message>`\
> `Permission: lands.command.chat`\
> Description: Chat with land.

> `/lands delete <land | here>`\
> `Permission: lands.command.delete`\
> Description: Delete a land or subarea at your current position, if you provide "here" for the land parameter.

> `/lands deny`\
> `Permission: lands.command.deny`\
> Description: Deny invite.

> `/lands deposit [land] <amount>`\
> `Permission: lands.command.deposit`\
> Description: Deposit money to land bank.

> `/lands edit <land>`\
> `Permission: lands.command.edit`\
> Description: Enter edit mode for a land.\
> Actions like /lands claim will be executed for this land.

> `/lands info [land]`\
> `Permission: lands.command.info`\
> Description: Show information about a land.

> `/lands invites`\
> `Permission: lands.command.invites`\
> Description: Open received invites GUI.

> `/lands leave <land | here>`\
> `Permission: lands.command.leave`\
> Description: Leave a land or the area at your current position, if you provide "here" for the land parameter.

> `/lands map`\
> `Permission: lands.command.map`\
> Description: Show lands map.

> `/lands menu`\
> `Permission: lands.command.menu`\
> Description: Open Lands GUI.\
> Append "here" to the command to open the GUI\
> for the chunk you're standing in.

> `/lands menu here`\
> `Permission: lands.command.menu`\
> Description: Open Lands GUI for the chunk you're standing in.

> `/lands rename [land] <new name>`\
> `Permission: lands.command.rename`\
> Description: Rename land.

> `/lands selection`\
> `Permission: lands.command.selection`\
> Description: Select a region for actions like /lands claim.\
> Use `/lands selection expand` to expand the selection to all y levels.\
> Possible actions:\
> /lands claim\
> /lands unclaim\
> /lands trust\
> /lands untrust

> `/lands assign <area>`\
> `Permission: lands.command.assign`\
> Description: Assign selection to a area (resize) or create a new area. Alternatively you can use `/lands selection assign`.

> `/lands setrole <player> <area,*> <role>`\
> `Permission: lands.command.setrole`\
> Description: Set a role of a player.\
> The area parameter defines a sub area of the land.

> `/lands setspawn`\
> `Permission: lands.command.setspawn`\
> Description: Set spawn for land.

> `/lands spawn [land]`\
> `Permission: lands.command.spawn`\
> Description: Teleport to land spawn.

> `/lands top`\
> `Permission: lands.command.top`\
> Description: Show top ten lands.

> `/lands trust <player> [area,*]`\
> `Permission: lands.command.trust`\
> Description: Trust a player.\
> Area parameter is optional.

> `/lands unclaim`\
> `Permission: lands.command.unclaim`\
> Description: Unclaim a chunk.

> `/lands unclaim auto`\
> `Permission: lands.command.unclaim.auto`\
> Description: Unclaim chunks while walking.

> `/lands unclaimall`\
> `Permission: lands.command.unclaimall`\
> Description: Unclaim all chunks for the land.

> `/lands untrust <player> [area,*]`\
> `Permission: lands.command.untrust`\
> Description: Untrust player.\
> Area parameter is optional.

> `/lands storage`\
> `Permission: lands.command.storage`\
> Description: Open the land item storage inventory.

> `/lands view`\
> `Permission: lands.command.view`\
> Description: Visualise land borders.

> `/lands unstuck`\
> `Permission: lands.command.unstuck`\
> Description: Teleport to the nearest unclaimed chunk. This allows you to teleport out of claims, if you're stuck inside.

> `/lands wild [world] [player]`\
> `Permission: lands.command.wild`\
> Description: Teleport to a random location. The optional player parameter is\
> only available to players with the permission "lands.admin.command.wild"\
> You can customize this command in the config file.

> `/lands wild [world] [player]`\
> `Permission: lands.admin.command.wild`\
> Description: Execute /wild for other players.

> `/lands withdraw <amount> [land]`\
> `Permission: lands.command.withdraw`\
> Description: Withdraw money from land bank.

> `/lands balance [land]`\
> `Permission: lands.command.balance`\
> Description: View land's balance.

> `/lands taxes`\
> `Permission: lands.command.taxes`\
> Description: View upcoming tax payments.

> `/lands rent`\
> `Permission: lands.command.rent`\
> Description: [Manage rentals.](https://github.com/Angeschossen/Lands/wiki/Rent-System)

> `/lands relations`\
> `Permission: lands.command.relations`\
> Description: Manage relations.

> `/lands confirmtp`\
> `Permission: None`\
> Description: Confirm unsafe destination.

#### Nations

> `/nations create`\
> `Permission: nations.command.create`\
> Description: Create a nation.

> `/nations accept`\
> `Permission: nations.command.accept`\
> Description: Accept invite.

> `/nations delete`\
> `Permission: nations.command.delete`\
> Description: Delete nation.

> `/nations deny`\
> `Permission: nations.command.deny`\
> Description: Deny invite.

> `/nations leave`\
> `Permission: nations.command.leave`\
> Description: Leave nation.

> `/nations rename`\
> `Permission: nations.command.rename`\
> Description: Rename nation.

> `/nations menu`\
> `Permission: nations.command.menu`\
> Description: Open nation menu.

> `/nations setcapital`\
> `Permission: nations.command.setcapital`\
> Description: Set capital of nation.

> `/nations spawn`\
> `Permission: nations.command.spawn`\
> Description: Teleport to nation spawn.

> `/nations trust`\
> `Permission: nations.command.trust`\
> Description: Add land.

> `/nations untrust`\
> `Permission: nations.command.untrust`\
> Description: Remove land.

> `/nations relations`\
> `Permission: nations.command.relations`\
> Description: Manage relations.

> `/nations top`\
> `Permission: nations.command.top`\
> Description: View top nations.

#### Wars

> `/wars declare`\
> `Permission: wars.command.declare`\
> Description: Declare war against a land or nation.

> `/wars deny`\
> `Permission: wars.command.deny`\
> Description: Deny mutual war declaration.

> `/wars info`\
> `Permission: wars.command.info`\
> Description: Info about current war.

> `/wars menu`\
> `Permission: wars.command.menu`\
> Description: Open menu for current war.

> `/wars list`\
> `Permission: wars.command.list`\
> Description: View all active wars.

> `/wars spawn`\
> `Permission: wars.command.spawn`\
> Description: Teleport to the enemies border.
