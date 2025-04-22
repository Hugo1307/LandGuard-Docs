---
slug: config-overview
title: Configuration Overview
tags: [config]
sidebar_position: 1
---
The `config.yml` file is the central configuration point for LandGuard. It allows server administrators to customize everything from database settings and land behavior to permissions, protection flags, and economy integration. Below is an overview of each section in the configuration file:

---

### ☁️ Cloud Integration (`cloud`)
This section configures the integration with **MineSphere**, a web interface and cloud backup system for player lands.

```yaml
cloud:
  serverId: "your-server-id"
  serverSecret: "your-auth-key"
```

- **serverId**: Unique ID provided upon purchase for MineSphere.
- **serverSecret**: Auth key to securely connect your server to the cloud.

### 🗄️ Database Configuration (`database`)
LandGuard supports multiple database backends for storing land data.

```yaml
database:
  dbms: "sqlite"
  address: "localhost"
  port: 3306
  name: "land_guard"
  user: "root"
  password: "admin"
```

- **dbms**: Supported options: sqlite, mysql, postgresql, mariadb.
- **address**: The address of the database (not rquired for SQLite).
- **port**: The port of the database (not required for SQLite).
- **name**: The name of the database.
- **user**: The user to connect to the database.
- **password**: The password to connect to the database.

> ℹ️ SQLite is not recommended for production servers. Use on your own risk!

### ⚙️ General Settings (`general`)
Configure basic behavior and restrictions.

```yaml
general:
  defaultDescription: "A new land created using LandGuard"
  maxLandsPerPlayer: 5
```

- **defaultDescription**: Default description for new lands.
- **maxLandsPerPlayer**: Maximum lands a single player can own.

### 🌍 Land Settings (`land`)
Control land size limits, geometry, economy pricing, access permissions, and protection rules.

#### Land Area and Members

```yaml
minLandArea: 25
maxLandArea: 5000
maxMembers: 20
```

- **minLandArea**: Set the smallest allowed land area.
- **maxLandArea** Set the largest allowed land area.
- **maxMembers**: Limit how many players can be part of a land.

#### Geometry

```yaml
geometry:
  biDimensional: false
  minHeight: -64
  maxHeight: 320
```

- **biDimensional**: Set `true` for 2D lands (ignores Y), `false` for full 3D land.
- **minHeight** and **maxHeight**: Y-coordinate bounds for land if 2D.

### 💰 Economy Integration (`costs`)
Enable and configure pricing for player actions (requires Vault and an economy plugin).
Each sub-action can be toggled on/off and priced individually.

**Example:**
```yaml
create:
  enabled: true
  onCreate: 100
  perBlock: 1
```

- **onCreate**: Flat cost to create a land.
- **perBlock**: Additional cost per block of land area.

Some other priced operations are:

- **delete**, **expand**, **rename**, **description**, **teleport**
- **members** (add, remove, promote, demote)
- **groups** (add/remove permissions)
- **flags** (toggle protection rules)

### 🔐 Access Groups (`defaultAccessGroups`)
Define the default permission groups that are created when a new land is created. 

Each group has a set of permissions that determine what players can do within the land, and an `accessLevel` that defines the rank of each group. This `accessLevel` is used to determine the order of the groups when promoting or demoting members. Higher `accessLevel` values indicate access groups with more permissions.

- **Visitor**, **Member**, and **Admin** each have specific accessLevel and permissions.
- You can fully customize these or add new groups in the config.

**Example:**
```yaml
- name: "Admin"
  accessLevel: 2
  permissions:
    - "BREAK_BLOCKS"
    - "PLACE_BLOCKS"
    ...
```

> 💡 You can add custom access groups by defining them in the `defaultAccessGroups` section. Each group can have its own set of permissions.

> ⚠️ Changing the default access groups will only affect new lands. Existing lands will retain their current access groups and permissions.

### 🚫 Default Protection Flags (`defaultFlagValues`)
Flags define passive land protections against non-player events (e.g., explosions, fire spread, PVP).

**Example:**
```yaml
- flag: "TNT_EXPLOSIONS"
  enabled: false
- flag: "PVP"
  enabled: true
```

By editing these configurations you can customize the default values of the flags that are set when a land is created.
Players may still be able to change the flags on their own lands (if they have permission).

> ⚠️ Changing the default flag values will only affect new lands. Existing lands will retain their current flag values.

> 💡 You can use the command `lg reload` after editing your `config.yml` to apply your changes!
