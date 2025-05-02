---
slug: what-are-flags
title: What Are Flags?
tags: [access, access-group]
sidebar_position: 1
---

**Flags** define the rules and behaviors within a land. They control what can or cannot happen in a specific land area, such as whether blocks can be broken, mobs can spawn, or players can interact with objects. 

Flags are highly customizable, allowing land owners to fine-tune protection and gameplay mechanics on their land. They can be toggled individually via commands or GUIs. Some flags affect environmental behavior (e.g., fire spreading, explosions), while others define access (e.g., chest access, entering, item pickup).

### 🛡️ Flags vs. Access Groups

Flags may seem similar to Access Groups however, they serve a **different purpose**. While Access Groups manage permissions for players who are part of the land, Flags apply to the players who are not part of the land.

Flags can also control environmental events that may not be directly tied to player actions, such as fire spreading or explosions, for example, while Access Groups are focused on managing player interactions and permissions within the land.

> 📌 Access groups can override flags. For example, if a player is in the **Visitor** group and the `BLOCK_BREAK` flag is set to `true`, they will be able to break blocks even if the flag is set to `false`. 

