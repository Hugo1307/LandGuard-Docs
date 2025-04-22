---
slug: core-features
title: Core Features
tags: [features]
sidebar_position: 2
---

LandGuard is packed with features designed to give players and server administrators complete control over land protection and player interaction. Below is a breakdown of the core functionality that makes LandGuard a powerful and user-friendly plugin.

---

### 🧱 Land Claiming (2D and 3D)

Players can define their own protected regions (called **lands**) using a simple command and stick-based corner selection. The shape can be either 2D (flat land) or 3D (volumetric), based on server configuration.

### 🛡️ Grief Protection

Lands are automatically protected from unauthorized modifications by other players. This includes block breaking, placing, interaction, and other forms of griefing—whether direct or indirect.

### 👥 Role-Based Access Control

Each land has **access groups** that determine what players can and cannot do. Players can be added as **Visitors**, promoted to **Members**, or given full administrative rights as **Admins**.

Server administrators can use the plugin configuration (`config.yml`) to: 
- Create and customize groups
- Assign permissions per group
- Promote/demote players via GUI or commands

### 🚩 Flag System

Use **flags** to control environmental and server-side events that aren't tied to a specific player. This includes:

- Mob spawning
- Fire and lava spread
- Explosion protection
- PVP toggle
- Water flow, piston use, and more

Flags can be adjusted per land and are fully configurable.

### 💰 Economy Integration (Vault)

LandGuard supports **Vault** to charge players for actions like:

- Creating or expanding a land
- Deleting or renaming a land
- Managing members and access groups
- Toggling flags or teleporting

All costs and actions are optional and configurable.

### 🖱️ Intuitive GUI Interface

A built-in GUI allows players to manage all aspects of their lands without needing to memorize commands.

- Manage members
- Set or update land name/description
- Toggle flags
- Edit permissions for groups
- Teleport to the land
- Delete land

Command to open: `/lg`

### ☁️ MineSphere Integration

LandGuard connects to **MineSphere**, a web-based dashboard where players can view and manage their lands online. It also includes:

- Cloud backup of all land data
- Resilience in case of server crashes or world resets
- Web access to personal and public lands

### ⚙️ Fully Configurable

Every aspect of LandGuard can be tailored to your server’s needs:

- Change default permissions
- Create or rename access groups
- Enable or disable flags
- Set prices for all economy actions
- Choose between 2D or 3D land claims

Whether you're running a small SMP or a massive network, LandGuard adapts to your rules.