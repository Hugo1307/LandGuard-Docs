---
slug: member-management
title: Member Management
tags: [access, access-group]
sidebar_position: 4
---

Land owners and land admins can promote or demote other members within their lands using the LandGuard GUI or commands. When a player is promoted, they gain access to more permissions and capabilities within the land. Conversely, demoting a player restricts their permissions.

This feature is particularly useful for managing the roles and responsibilities of players within a land, allowing for a flexible and dynamic member management system.

> 📝 The destination group when promoting or demoting players is calculated using the groups' access level. See [Access Levels](overview#-access-levels) for more details.

## ⬆️ Promotion and Demotion

When a player is promoted, their access group changes to a higher-level group (e.g., from Visitor to Member). Demotion works the same way but in reverse.

### Promoting a Member

Promoting moves a player to a group with a higher access level:

```bash
/land member promote <player>
```

### Demoting a Member

Demoting moves a player to a group with a lower access level:

```bash
/land member demote <player>
```

> ⚠️ Only players in an Admin-level group (or with `MANAGE_MEMBERS` permission) can promote or demote others (including themselves).
