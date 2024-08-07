# 命令

> `/lands`\
> `权限：lands.command.menu`\
> 描述：打开城镇菜单

> `/lands help [页码]`\
> `权限：lands.command.help`\
> 描述：展示插件命令帮助

> `/lands claim`\
> `权限：lands.command.claim`\
> 描述：占领区块

> `/lands claim auto`\
> `权限：lands.command.claim.auto`\
> 描述：占领之后走过的所有区块

> `/lands create`\
> `权限：lands.command.create`\
> 描述：建立城镇

> `/lands merge <城镇名>`\
> `权限：lands.command.merge`\
> 描述：将指定的城镇与当前城镇合并

> `/lands accept <城镇名>`\
> `权限：lands.command.accept`\
> 描述：同意邀请

> `/lands chat [城镇名] <message>`\
> `权限：lands.command.chat`\
> 描述：加入城镇聊天频道

> `/lands delete <城镇名 | here>`\
> `权限：lands.command.delete`\
> 描述：删除一个城镇或子区域，如果使用 `here` 参数则为当前所在的城镇或子区域

> `/lands deny`\
> `权限：lands.command.deny`\
> 描述：拒绝邀请

> `/lands deposit [城镇名] <金额>`\
> `权限：lands.command.deposit`\
> 描述：向城镇金库存款

> `/lands edit <城镇名>`\
> `权限：lands.command.edit`\
> 描述：进入对一个城镇的编辑模式\
> 类似 /lands claim 的命令将会以这个城镇为目标执行

> `/lands info [城镇名]`\
> `权限：lands.command.info`\
> 描述：展示一个城镇的基本信息

> `/lands invites`\
> `权限：lands.command.invites`\
> 描述：展示所有收到的邀请

> `/lands leave <城镇名 | here>`\
> `权限：lands.command.leave`\
> 描述：离开一个城镇或子区域，如果使用 `here` 参数则为当前所在的城镇或子区域

> `/lands map`\
> `权限：lands.command.map`\
> 描述：展示城镇地图

> `/lands menu`\
> `权限：lands.command.menu`\
> 描述：打开城镇菜单\
> 增加 `here` 参数则打开当前所在区块对应城镇的菜单\

> `/lands menu here`\
> `权限：lands.command.menu`\
> 描述：打开当前所在区块对应城镇的菜单

> `/lands rename [城镇名] <新名称>`\
> `权限：lands.command.rename`\
> 描述：重命名城镇

> `/lands selection`\
> `权限：lands.command.selection`\
> 描述：为如 /lands claim 的操作选定一个区域\
> 使用 `/lands selection expand` 命令将区域拓展至占满 Y 轴\
> 可能的操作:\
> /lands claim\
> /lands unclaim\
> /lands trust\
> /lands untrust

> `/lands assign <子区域名>`\
> `权限：lands.command.assign`\
> 描述：将一个选区分配给指定子区域（调整大小）或新建一个子区域\
> 另可使用命令 `/lands selection assign`.

> `/lands setrole <玩家名> <子区域名, *> <职位名>`\
> `权限：lands.command.setrole`\
> 描述：设置一个玩家的职位\
> 子区域参数指定了城镇中的特定子区域为目标

> `/lands setspawn`\
> `权限：lands.command.setspawn`\
> 描述：为城镇设置传送点

> `/lands spawn [城镇名]`\
> `权限：lands.command.spawn`\
> 描述：传送到城镇传送点

> `/lands top`\
> `权限：lands.command.top`\
> 描述：展示排行榜前十的城镇

> `/lands trust <玩家名> [area,*]`\
> `权限：lands.command.trust`\
> 描述：邀请一个玩家作为成员\
> 子区域参数是可选的

> `/lands unclaim`\
> `权限：lands.command.unclaim`\
> 描述：放弃占领区块

> `/lands unclaim auto`\
> `权限：lands.command.unclaim.auto`\
> 描述：放弃占领之后走过的所有区块

> `/lands unclaimall`\
> `权限：lands.command.unclaimall`\
> 描述：放弃占领城镇的所有区块

> `/lands untrust <玩家名> [area,*]`\
> `权限：lands.command.untrust`\
> 描述：移出玩家\
> 子区域参数是可选的

> `/lands storage`\
> `权限：lands.command.storage`\
> 描述：打开城镇储存库

> `/lands view`\
> `权限：lands.command.view`\
> 描述：使城镇领土边界对你可视化

> `/lands unstuck`\
> `权限：lands.command.unstuck`\
> 描述：传送到离你最近的非城镇领土的区块、
> 如果你卡在了城镇中，可以用这个命令离开城镇

> `/lands wild [世界名]`\
> `权限：lands.command.wild`\
> 描述：传送到世界中的随机位置\
> 拥有权限 `lands.admin.command.wild` 的玩家可以为其他玩家执行此操作\
> 你可以在插件配置文件中设置此命令的具体行为

> `/lands wild [世界名] [玩家名]`\
> `权限：lands.admin.command.wild`\
> 描述：为其他玩家执行 /wild 命令

> `/lands withdraw <金额> [城镇名]`\
> `权限：lands.command.withdraw`\
> 描述：从城镇金库中取款

> `/lands balance [城镇名]`\
> `权限：lands.command.balance`\
> 描述：查看城镇金库余额

> `/lands taxes`\
> `权限：lands.command.taxes`\
> 描述：查看即将收取的税费信息

> `/lands rent`\
> `权限：lands.command.rent`\
> 描述：[管理租售](zu-shou-xi-tong.md)

> `/lands relations`\
> `权限：lands.command.relations`\
> 描述：管理外交关系

> `/lands confirmtp`\
> `权限：None`\
> 描述：确认传送到不安全的位置

#### 联邦

> `/nations create`\
> `权限：nations.command.create`\
> 描述：建立一个联邦

> `/nations accept`\
> `权限：nations.command.accept`\
> 描述：同意邀请

> `/nations delete`\
> `权限：nations.command.delete`\
> 描述：解散联邦

> `/nations deny`\
> `权限：nations.command.deny`\
> 描述：拒绝邀请

> `/nations leave`\
> `权限：nations.command.leave`\
> 描述：推出联邦

> `/nations rename`\
> `权限：nations.command.rename`\
> 描述：重命名联邦

> `/nations menu`\
> `权限：nations.command.menu`\
> 描述：打开联邦菜单

> `/nations setcapital`\
> `权限：nations.command.setcapital`\
> 描述：设置联邦的首都

> `/nations spawn`\
> `权限：nations.command.spawn`\
> 描述：传送到联邦传送点

> `/nations trust`\
> `权限：nations.command.trust`\
> 描述：邀请城镇作为成员

> `/nations untrust`\
> `权限：nations.command.untrust`\
> 描述：移出城镇

> `/nations relations`\
> `权限：nations.command.relations`\
> 描述：管理外交关系

> `/nations top`\
> `权限：nations.command.top`\
> 描述：查看联邦排行榜

#### 战争

> `/wars declare`\
> `权限：wars.command.declare`\
> 描述：对城镇或联邦宣战

> `/wars deny`\
> `权限：wars.command.deny`\
> 描述：双方取消或拒绝宣战

> `/wars info`\
> `权限：wars.command.info`\
> 描述：当前战争的信息

> `/wars menu`\
> `权限：wars.command.menu`\
> 描述：打开当前战争的菜单

> `/wars list`\
> `权限：wars.command.list`\
> 描述：查看所有正在进行的战争

> `/wars spawn`\
> `权限：wars.command.spawn`\
> 描述：传送到敌方领土的边界
