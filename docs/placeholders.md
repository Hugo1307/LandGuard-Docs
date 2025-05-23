---
slug: placeholders
title: Placeholders
tags: [placeholders]
sidebar_position: 5
---

LandGuard supports **PlaceholderAPI**, allowing server administrators to display dynamic land-related data in messages, scoreboards, GUIs, and more.

These placeholders can provide useful real-time information about players, their lands, and land-specific data—making them ideal for customizing your server experience.

---

## ✅ Requirements

To use these placeholders, you must have the [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/) plugin installed on your server. LandGuard will automatically register its placeholders if PlaceholderAPI is present.

## 📄 Placeholder List and Descriptions

Below is a list of all available placeholders provided by LandGuard:

| Placeholder | Description |
|------------|-------------|
| `%landguard_lands_count%` | Returns the **total number of lands** the player has access to (member or owner). |
| `%landguard_lands%` | Returns a **comma-separated list** of all lands the player has access to. |
| `%landguard_owned_count%` | Returns the **total number of lands** the player **owns**. |
| `%landguard_owned%` | Returns a **comma-separated list** of all lands **owned** by the player. |
| `%landguard_land_name%` | Returns the **name of the land** the player is currently in. |
| `%landguard_land_owner%` | Returns the **owner’s name** of the land the player is currently in. |
| `%landguard_land_accessible%` | Returns `"yes"` if the player **has access** to the land they are in, `"no"` otherwise. |
| `%landguard_land_group%` | Returns the **access group name** the player is in for the current land (e.g., Visitor, Member, Admin). |
| `%landguard_land_members_count%` | Returns the **total number of members** in the land the player is currently in. |
| `%landguard_land_members%` | Returns a **list of all members' names** in the land the player is currently in. |
| `%landguard_land_members_online_count%` | Returns the **number of online members** of the land the player is currently in. |
| `%landguard_land_members_online%` | Returns a **list of online member names** in the land the player is currently in. |

## 💡 Usage Tips

- You can use these placeholders with other compatible plugins such as:
  - Scoreboard managers (FeatherBoard, TAB, etc.)
  - GUI plugins (DeluxeMenus, ChestCommands, etc.)
  - Chat formatting plugins
- Some placeholders depend on the player’s **current location** — for example, `%landguard_land_name%` will only return a value if the player is standing inside a land.


## 🔧 Troubleshooting

- If placeholders are not working, try running `/papi reload`.
- Make sure LandGuard and PlaceholderAPI are both loaded without errors.
    - If you see the message `PlaceholderAPI not found. Placeholders will not be registered` in the console, it means PlaceholderAPI is not installed or not loaded correctly.
- You can test if the placeholders are recognized with `/papi parse <player> <placeholder>`.
