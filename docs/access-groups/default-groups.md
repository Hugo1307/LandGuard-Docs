---
slug: default-groups
title: Default Groups
tags: [access, access-group]
sidebar_position: 2
---

When a land is created, it automatically includes the three default Access Groups: **Visitor**, **Member**, and **Admin**. 
These provide a basic hierarchy for access control and permissions, and correspond to the default groups configured in the `config.yml` file.

> 📝 The default groups can be changed by server administrators. See [Create Custom Groups](custom-access-groups) for more details.

### 🟢 Visitor

The **Visitor** group is the most restricted, designed for players who are not entirely trustable but should be allowed to interact with the land in limited ways. It has an access level of `0`, the lowest in the hierarchy - it is the default group for players who got recently added to the land.

Visitors are allowed to:

- Enter the land
- Interact with elements (such as buttons or doors)
- Use beds
- Pick up items

This group provides basic interaction without granting privileges that could affect the land's structure or other players.

### 🔵 Member

The **Member** group is intended for trusted players who actively participate in the land's development or upkeep. It has an access level of `1`.

Members inherit all permissions from the Visitor group, and additionally, they can:

- Break and place blocks
- Damage both friendly and hostile mobs
- Access chests
- Teleport within the land

This group is well-suited for builders, farmers, or any collaborator with moderate access needs.

### 🔴 Admin

The **Admin** group is the highest default group, with an access level of `2`. It is meant for players who manage the land and require full administrative control.

Admins inherit all permissions from the Member group, and also gain the ability to:

- Ignite blocks
- Ride and manage vehicles
- Use fertilizer
- Manage land members and their roles
- Adjust group permissions
- Toggle land flags
- Expand the land

Admins are responsible for configuring protection, managing teams, and making important land-related decisions.

> ⚠️ Be cautious when assigning players to the Admin group, as they have full control over the land and its members. Only trusted players should be given this level of access.

> 📝 By default, the owner of the land is the only one with permission to delete it.