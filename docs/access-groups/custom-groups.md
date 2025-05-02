---
slug: custom-access-groups
title: Create Custom Groups
tags: [access, access-group]
sidebar_position: 3
---

LandGuard allows server administrators to create custom Access Groups directly through the configuration file.

To add a new group, navigate to `config.yml` and locate the `defaultAccessGroups` section. You can define a new group by providing a unique name, access level, and a list of permissions.


**Example:**

```yaml
- name: "Moderator"
  accessLevel: 1
  permissions:
    - "BREAK_BLOCKS"
    - "PLACE_BLOCKS"
    - "INTERACT"
    - "ENTER"
    - "MANAGE_MEMBERS"
```

### 🔑 Available Permissions

You can assign various permissions to your custom groups. Here you can find a list of available permissions, along with their descriptions:

| Permission              | Description                                                                |
|-------------------------|----------------------------------------------------------------------------|
| `BREAK_BLOCKS`          | Allows breaking blocks within the land.                                    |
| `PLACE_BLOCKS`          | Allows placing blocks within the land.                                     |
| `INTERACT`              | Allows interacting with entities and blocks within the land.               |
| `DAMAGE_FRIENDLY_MOBS`  | Allows damaging friendly mobs within the land.                             |
| `DAMAGE_HOSTILE_MOBS`   | Allows damaging hostile mobs within the land.                              |
| `ENTER`                 | Allows entering the land.                                                  |
| `IGNITE`                | Allows igniting blocks within the land.                                    |
| `CHEST_ACCESS`          | Allows accessing chests within the land.                                   |
| `RIDE`                  | Allows riding vehicles within the land.                                    |
| `VEHICLE_DESTROY`       | Allows destroying vehicles within the land.                                |
| `VEHICLE_USE`           | Allows using vehicles within the land.                                     |
| `BED_USE`               | Allows using beds within the land.                                         |
| `ITEM_PICKUP`           | Allows picking up items within the land.                                   |
| `FERTILIZE`             | Allows fertilizing crops within the land.                                  |
| `TELEPORT`              | Allows teleporting within the land.                                        |
| `MANAGE_MEMBERS`        | Allows managing members within the land.                                   |
| `MANAGE_ROLES`          | Allows managing roles within the land.                                     |
| `MANAGE_PERMISSIONS`    | Allows managing permissions within the land.                               |
| `MANAGE_FLAGS`          | Allows managing flags within the land.                                     |
| `EXPAND`                | Allows expanding the land area.                                            |
| `RENAME`                | Allows renaming the land.                                                  |
| `UPDATE_DESCRIPTION`    | Allows updating the land's description.                                    |
| `DELETE`                | Allows deleting the land.                                                  |
