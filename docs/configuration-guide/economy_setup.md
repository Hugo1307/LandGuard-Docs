---
slug: economy-setup
title: Economy Setup
tags: [economy, config]
sidebar_position: 2
---

# Setting Up Economy Options

LandGuard supports full integration with **Vault**, allowing you to charge players for various land-related operations using your server's economy system. This adds a valuable gameplay balance and monetization strategy for survival and semi-vanilla servers.

---

### ✅ Requirements

To enable economy support in LandGuard, make sure the following are installed:

- **Vault** plugin
- A supported economy plugin (such as EssentialsX Economy or others supported by Vault)

> ⚠️ If Vault or an economy plugin is missing, LandGuard will automatically disable its economy-related features. This means everything will be free for players!

### ⚙️ Enabling Economy in `config.yml`

Economy operations are configured under the `land.costs` section in the `config.yml` file. Each type of operation (e.g., creating lands, renaming, adding members) has its own settings to control cost and availability.

Here’s an example of how land creation costs are defined:

```yaml
land:
  costs:
    create:
      enabled: true        # Whether land creation costs are enabled
      onCreate: 100        # Flat fee for creating a land
      perBlock: 1          # Additional cost per block within the land area
```

You can similarly control the cost of:

- Deleting lands
- Expanding land size
- Renaming or updating land description
- Teleporting to land
- Managing members (add, remove, promote, demote)
- Modifying access groups
- Toggling protection flags

**Example:** Enabling and pricing member promotions

```yaml
members:
  promote:
    enabled: true
    cost: 100
```

### 🧮 Cost Calculation

Some operations support both a flat fee and a per-block cost. 
As an example, we have the process of land creation, which supports both a fee upon creation combined with a fee that increases with the size of the land being created.

```yaml
create:
    onCreate: 100    # Flat fee - cost charged when creating the land
    perBlock: 1      # Per-Block fee - Cost charged per block when creating a land
```

For example, if a player wants to create a land with an area of 100 blocks, it would result in a total cost of:

```ini
Total = 100 + (100 × 2) = 300
```

This allows you to scale pricing based on land size or complexity.

### 🪙 Customizing for Your Server
You are free to:

- Disable any operation by setting enabled: false
- Set costs to 0 if you want to allow free usage of specific features
- Adjust all prices to match your economy’s balance

> 📝 Tip: Combine LandGuard’s economy settings with rank permissions or quests to create more dynamic progression systems!