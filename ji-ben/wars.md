# Wars

This page explains how the war system of Lands works from the perspective of a player.

## 1. Declare War

To declare war against your enemy, simply execute `/Wars declare <land>`.\
Now a menu will open which asks you about setting a tribute. This tribute will be paid by the enemy (defender) in case they surrender later.\
After you clicked on the send button, the enemy will receive your war declaration with information, like when the war starts and which tribute you set in case they want to surrender.

## 2. War Preparation Time

After the declaration is sent, the war preparation time starts. During this time, the defender has time to prepare against for the upcoming fight. How long the preparation time is depends on your server's configuration. All players of both lands will get a notification periodically. By executing `/Wars info` or `/Wars menu` you can get information about the upcoming war.

## 3. The War starts

When the war preparation time is over, all players of both lands are able to fight against their enemy. There may be certain options enabled on your server that prevent invading the enemies land, while their players are offline. By executing `/Wars info` or `/Wars menu` you can get information about the current war.

### 3.1 What happens if a player is part of multiple lands? Which team will they join?

Defending lands are prioritized and the team is calculated once and stays the same.

### 3.2 Allies

Direct allies (a land or lands of a nation) will be able to support you in your war. They'll also be visible in the `/wars` menu. They also can be attacked by the enemy.

## 4. During the War

During the wartime, you may be able to invade the enemies land and steal items from their containers, but this fully depends on your server's configuration. You may even be able to break and place certain or all blocks. Again, this depends on the server you're playing on. Also, the server may have configured a minimum amount of members of the enemy which need to be online, before you can invade their land.

### 4.1 Capture Points

Capture points can be crafted or are given to you by the server. You can view the crafting recipe during the war in the `/wars` menu. You must place them at the edge of the enemies land (inside). After that, you must clear all enemy presence in this area and hold the capture point for a specific time. You'll be able to view a progress bar at the top of your screen. Be aware that the defenders get notified once you place a capture point! Depending on your server's configuration, your land may claim the captured area after you held it successfully.

## 5. The War is over

Your server has a configured max. wartime, which will be visible for you during the wartime. The team with the most kills wins the war. The winner will be rewarded with a robbery money amount with is taken from the defender's balance (usually their land bank; this depends on your server's configuration). Your server may also have set up custom rewards in the Lands wars config. If both teams have the same amount of kills, the war will end in a draw and no team will be rewarded. Depending on your server's configuration, you may receive a war shield.
