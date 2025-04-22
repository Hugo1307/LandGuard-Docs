---
slug: permissions
title: Permissions
tags: [permissions]
---
# Permissions

LandGuard uses a permission-based system to control access to its commands and features. This allows server administrators to fine-tune which players or groups have access to specific actions, commands, and GUI interactions.

Permissions can be managed using any permissions plugin that supports Bukkit/Spigot API, such as:

- [LuckPerms](https://luckperms.net/)
- PermissionsEx
- GroupManager

---

### 🔧 How Permissions Work

Each command or feature in LandGuard is associated with a permission node. By default, all permissions are restricted to **Operators (OPs)** unless explicitly granted via a permissions plugin.

If a player lacks the necessary permission, they will receive a message indicating they don't have access to the command or feature.

### 🧾 Protection Features

These permissions usually apply to players. They can limit access to commands as well as GUI interactions.

| Permission Node                            | Description                                      
|--------------------------------------------|------------------------------------------------------------------------|
| `landguard.land.create`                    | Allows the player to create lands                                      |
| `landguard.land.delete`                    | Allows the player to delete one of his lands                           |
| `landguard.land.expand`                    | Allows the player to expand one of his lands                           |
| `landguard.land.info`                      | Allows checking information about a land                               |
| `landguard.land.info.all`                  | Allows checking a list of all lands                                    |
| `landguard.land.rename`                    | Allows renaming a land                                                 |
| `landguard.land.teleport`                  | Allows teleporting to a land                                           |
| `landguard.land.description`               | Allows updating the land's description                                 |
| `landguard.permissions.add`                | Allows adding permissions to the access group of a certain land        |
| `landguard.permissions.remove`             | Allows removing permissions from the access group of a certain land    |
| `landguard.members.add`                    | Allows adding members to a land                                        |
| `landguard.members.remove`                 | Allows removing members from a land                                    |
| `landguard.members.promote`                | Allows promoting members within a land                                 |
| `landguard.members.demote`                 | Allows demoting members within a land                                  |
| `landguard.flags.toggle`                   | Allows toggling protection flags                                       |


### 🧾 GUIs

These permissions apply to regular players and can prevent them from opening specific GUIs (depending on the permission). 

| Permission Node                            | Description                                      
|--------------------------------------------|------------------------------------------------------------------------|
| `landguard.gui.use`                        | Allows accessing the LandGuard GUI                                     |
| `landguard.gui.access_groups`              | Allows access to the access groups GUI                                 |
| `landguard.gui.flags`                      | Allows access to the flags GUI                                         |
| `landguard.gui.land`                       | Allows access to the land management GUI                               |
| `landguard.gui.lands`                      | Allows access to the lands GUI                                         |
| `landguard.gui.members`                    | Allows access to the members GUI                                       |  
| `landguard.gui.permissions`                | Allows access to the permissions GUI                                   | 

### 🧾 General Features

Usually apply to players and can limit access to commands as well as GUI interactions.

| Permission Node                            | Description                                      
|--------------------------------------------|------------------------------------------------------------------------|
| `landguard.confirm`                        | Allows confirming actions (e.g. land creation)                         | 
| `landguard.cancel`                         | Allows canceling land creation                                         | 
| `landguard.help`                           | Allows viewing help information                                        | 

### 🧾 Admin Features

These permissions are usually reserved for server administrators or trusted players. They allow access to commands that affect the entire server and other players' lands.

| Permission Node                            | Description                                      
|--------------------------------------------|------------------------------------------------------------------------|
| `landguard.admin.reload`                   | Allows reloading the plugin configuration                              |

### 🧪 Tips

- Use wildcard nodes like `landguard.admin.*` for moderators or admins.
- For servers with multiple roles, create permission groups (e.g., “builder,” “trusted,” “admin”) using LuckPerms or another permissions plugin.
- Combine with economy pricing for more granular control.