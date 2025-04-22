---
slug: commands
title: Commands
tags: [commands, permissions]
---

This section contains a complete list of commands provided by the LandGuard plugin, along with their usage, description, and permissions required (if applicable). These commands allow players and administrators to interact with and manage lands easily through the in-game chat.

---

### 📜 Command List

| Command                                        | Permission                      | Description                                                             |
|------------------------------------------------|---------------------------------|-------------------------------------------------------------------------|
| `/lg`                                          | landguard.gui.use               | Opens the main LandGuard GUI menu for land management.                  |
| `/lg land create`                              | landguard.land.create           | Starts the process to create a new land.                                |
| `/lg land cancel`                              | landguard.cancel                | Cancels the land creation process.                                      |
| `/lg land delete <landId>`                     | landguard.land.delete           | Deletes an existing land owned by the player.                           |
| `/lg land list`                                | landguard.land.info.all         | Lists all lands owned by the player.                                    |
| `/lg land tp <landId>`                         | landguard.land.teleport         | Teleports the player to the specified land.                             |
| `/lg land info <landId>`                       | landguard.land.info             | Displays information about a specific land.                             |
| `/lg land expand <landId> <direction> <rows>`  | landguard.land.expand           | Expands the land in a certain direction for a certain number of rows.   |
| `/lg land rename <landId> <name>`              | landguard.land.rename           | Changes the name of the player's selected land.                         |
| `/lg land setdesc <landId> <description>`      | landguard.land.description      | Updates the description of the player's selected land.                  |
| `/lg confirm`                                  | landguard.confirm               | Confirms an action such as land creation.                               |
| `/lg member add <landId> <player>`             | landguard.members.add           | Adds a player to the land as a visitor.                                 |
| `/lg member remove <landId> <player>`          | landguard.members.remove        | Removes a player from the land.                                         |
| `/lg member promote <landId> <player>`         | landguard.members.promote       | Promotes a member to a higher access group.                             |
| `/lg member demote <landId> <player>`          | landguard.members.demote        | Demotes a member to a lower access group.                               |
| `/lg permission add <landId> <groupName> <permission>` | landguard.permissions.add | Adds a permission to an access group of a land.                 |
| `/lg permission remove <landId> <groupName> <permission>` | landguard.permissions.remove | Removes a permission from an access group of a land.      |
| `/lg flag toggle <landId> <flag>`              | landguard.flags.toggle          | Toggles a protection flag for the land.                                 |
| `/lg help`                                     | landguard.help                  | Shows a list of all player-available commands.                          |
| `/lg reload`                                   | landguard.reload                | Reloads the plugin configuration.                                       |
