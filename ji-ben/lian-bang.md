# 联邦

## 什么是联邦

联邦是城镇的集合。城镇所有者可以通过执行命令 `/nations create <名称>` 来建立一个联邦。对应城镇将会成为这个新联邦的首都。一旦联邦被建立，就可以邀请其他城镇加入。

## 为联邦成员开放权限

你可以通过在城镇菜单中修改名为“联邦”的职位的相关设置来管理与你同属一个联邦的所有城镇的成员在你的城镇中能进行的行为。

## 城镇与联邦维护费

属于一个联邦的城镇将不再向服务器，而是向他们所属的联邦支付维护费。联邦也可以自由配置下属的城镇需要支付的维护费金额。同时，联邦本身需要向服务器支付维护费。这意味着联邦可以通过向下属城镇收取维护费从而缓解自身向服务器支付的维护费的压力。联邦可以在菜单中配置向下属城镇收取的维护费金额。可以通过命令 `/nations` 来打开联邦菜单。如果你同时是多个城镇的成员且它们分属不同的联邦，可以通过命令 `/lands edit <城镇>` 以使 `/nations` 命令作用于不同的联邦。

## 联邦与战争

Nations can declare war against other nations, like lands, by executing `/wars declare <land or nation>`. All lands in the nation will fight in this war. If a player is part two of lands that are not in the same nation, the player will join the team in which they are part of the most lands. In this case, lands they own will be prioritized. Depending on your server's configuration, a single land can also declare war against a whole nation.

## 联邦等级

A nation can level up by various factors which depend on your server's setup. Levels will reward you and your nation members with more claims and other benefits. You can view the level of your current nation by executing `/nations` and the clicking on the statistics item.
