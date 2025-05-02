---
slug: default-flags
title: Default Flags
tags: [flags, default]
sidebar_position: 2
---

There are many different flags available in LandGuard, each controlling a specific aspect of land protection and gameplay. These flags can be toggled on or off to customize the behavior of lands according to the needs of the players.

## 📋 Flag Types

Here you can find a list of the available flags and their default states. The default state indicates whether the flag is enabled or disabled when a new land is created.

| Flag                   | Default State  | Description                                                |
|------------------------|----------------|------------------------------------------------------------|
| `BLOCK_BREAK`          | `false`        | Allows or denies breaking blocks                           |
| `BLOCK_PLACE`          | `false`        | Allows or denies placing blocks                            |
| `INTERACT`             | `false`        | Controls interactions with objects (e.g., buttons, levers) |
| `DAMAGE_FRIENDLY_MOBS` | `false`        | Allows attacking passive mobs                              |
| `DAMAGE_HOSTILE_MOBS`  | `true`         | Allows attacking hostile mobs                              |
| `RECEIVE_DAMAGE`       | `false`        | Whether entities receive damage                            |
| `MOB_SPAWNING`         | `true`         | Controls natural mob spawning                              |
| `TNT_EXPLOSIONS`       | `false`        | Enables or disables TNT explosions                         |
| `CREEPER_EXPLOSIONS`   | `false`        | Controls damage from creepers                              |
| `OTHER_EXPLOSIONS`     | `false`        | Covers other types of explosions (e.g., beds, end crystals)|
| `ENTER`                | `true`         | Controls whether players can enter the land                |
| `IGNITE`               | `false`        | Allows or denies ignition (e.g., flint and steel)          |
| `FIRE_SPREADING`       | `false`        | Enables fire to spread                                     |
| `BLOCK_SPREADING`      | `true`         | Controls natural spreading like grass or vines             |
| `WATER_FLOW`           | `true`         | Allows water to flow into or within the land               |
| `LAVA_FLOW`            | `true`         | Allows lava flow                                           |
| `PVP`                  | `true`         | Enables or disables player versus player combat            |
| `CHEST_ACCESS`         | `false`        | Controls access to containers                              |
| `PISTON_USE`           | `false`        | Allows pistons to function                                 |
| `LEAVE_DECAY`          | `true`         | Controls whether leaves decay naturally                    |
| `RIDE`                 | `false`        | Whether players can ride entities                          |
| `VEHICLE_PLACE`        | `false`        | Allows placing boats or minecarts                          |
| `VEHICLE_DESTROY`      | `false`        | Allows destroying vehicles                                 |
| `VEHICLE_USE`          | `false`        | Allows use of minecarts and boats                          |
| `BED_USE`              | `false`        | Allows sleeping in beds                                    |
| `ITEM_PICKUP`          | `false`        | Controls whether items can be picked up                    |
| `FERTILIZE`            | `false`        | Allows use of bone meal or similar items                   |

Each of these flags can be toggled individually for each land.

## ⚙️ Configuring Flag Defaults

You can configure the default state of flags for all new lands using the `config.yml` file. This allows server administrators to define baseline behavior for newly created lands.

Example section in `config.yml`:

```yaml
  defaultFlagValues:
    - flag: "BLOCK_BREAK"
      enabled: false
    - flag: "MOB_SPAWNING"
      enabled: true
```

This configuration ensures that, for example, block breaking is disabled by default and mobs are allowed to spawn. Server administrators can also customize which flags players can manage using [permissions](/docs/permissions.md#-flags--access-permissions) and set costs for changing them.

> 📝 To change flags for an existing land, use the in-game `/land flag` command.