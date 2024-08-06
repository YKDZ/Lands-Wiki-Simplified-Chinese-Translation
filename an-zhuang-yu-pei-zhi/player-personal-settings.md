# Player Personal Settings

You can configure these flags inside your config.yml file. Options: `default_2_list, display_2_list`

These flags are applied to new players. Existing players can toggle these flags in their personal settings GUI menu, by executing `/lands menu main` and then navigating to the personal settings menu. They only control bahaviour related to this single player, such as receiving invites.

## Available Personal Settings

* **RECEIVE\_INVITES**\
  Allow other lands to invite the player to their land?
* **ENTER\_MESSAGES**\
  Show enter and leave messages when the player enters or leaves a land?
* **SHOW\_INBOX**\
  Show inbox messages, from lands the player is part of, in chat?

## Config

Here can add new flags.

```
# Players can toggle personal flags to customize their experience.
player:
  flags:
    # Configure a default list of flags that is enabled.
    # This only applies to new players, or those who haven't toggeled any flags yet.
    default_2_list:
      - 'receive_invites'
      - 'enter_messages'
      - 'show_inbox'

    # Configure which flags should be displayed in the menu.
    # ALL = all flags are displayed.
    display_2_list:
      - 'all'
```

## Other Flag Types

* Role Flags: https://github.com/Angeschossen/Lands/wiki/Roles-and-their-Flags
* Natural Flags: https://github.com/Angeschossen/Lands/wiki/Natural-Flags
