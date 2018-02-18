**Reward** rewards players with money *(using the Economics and/or Server Rewards plugin)* for killing animals, other players, entities, and activity.

## Dependencies

### Required

**Note:** you need to have at least one of these, you can use both as well.

- [Economics](https://umod.org/plugins/economics)
- [ServerRewards](http://oxidemod.org/plugins/serverrewards.1751/)

### Optional

- [Friends API](http://oxidemod.org/plugins/friends-api.686/)
- [Rust:IO Clans](http://oxidemod.org/plugins/rust-io-clans.842/)
- [Human NPC Core](http://oxidemod.org/plugins/human-npc-core.856/)

## Permissions

- **rewards.admin** -- for console commands and setreward chat command
- **rewards.vip** -- for VIP multipliers
- **rewards.showrewards** -- for the showrewards chat command

## Chat Commands

- **/setreward `<reward name> <value>`** -- Sets rewards config and saves it
- **/showrewards** -- Shows current rewards config

## Console Commands

- **setreward `<reward name> <value>`** -- Sets rewards config and saves it
- **showrewards** -- Shows current rewards config

## Multipliers

If enabled from config, players will get different rewards based on the weapon used and/or the distance from which the player killed the victim.

Distance multipliers in config (like distance_x) means distance is greater than x.

All multipliers are configurable from the config file.

If more than one multiplier is enabled, the total multiplier will be the product of all multipliers, which is then multiplied by the normal reward.

**VIP_Multipliers** give users/groups with the `rewards.vip` permission an extra multiplier *(default x2)*

**Example:** I kill a horse *(reward = 15)* with a Assault Rifle *(multiplier = 1.5)* from 162 meters ***(multiplier = 1.3)* in Happy Hour *(multiplier = 2)*, I get 15x *(1.5 x 1.3 x 2)* = **58.50**

**Happy Hour:** Disable it for now because it doesn't work as it should

## Friends and Clans

If the respective options are enabled from config, the plugin checks if the victim is a *'Friend'* or is in the same *'Clan'* of the killer, if so, no reward is given to the killer. This was made to avoid friends abusing and killing each other. This can also be avoided by enabling the `TakeMoneyFromVictim` which takes money from victim and gives it to killer
