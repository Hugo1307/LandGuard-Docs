---
slug: minesphere-setup
title: MineSphere Integration
tags: [minesphere, config]
sidebar_position: 3
---

# Enabling MineSphere Integration

**MineSphere** is a powerful web-based platform that works seamlessly with LandGuard to provide players and server admins with an enhanced land management experience outside of Minecraft. Through MineSphere, users can view, organize, and manage their lands via an intuitive online dashboard — and even benefit from automatic cloud backups.

---

### 🌐 What Are MineSphere Core Features?

MineSphere offers the following features:

- **Web Access to Lands:** Players can view their own lands and explore other players’ lands via a modern web UI.
- **Cloud Backups:** All land data is automatically backed up to the cloud, protecting against data loss in case of server failure.

### 🔐 Getting Started with Integration

To enable MineSphere on your server, follow these steps:

1. **Purchase LandGuard**  
   Only verified buyers can activate MineSphere integration.

2. **Join the LandGuard Discord**  
   Write a message in the ***#landguard-minesphere*** channel to request your **MineSphere credentials** (`serverId` and `serverSecret`).

3. **Update the Configuration File**  
   Open your `config.yml` and locate the `cloud` section. Fill in the credentials you received:

   ```yaml
   cloud:
     serverId: "your-server-id"
     serverSecret: "your-server-secret"
   ```

4. **Restart Your Server**  
   After saving the config, restart the server to apply the changes and activate cloud sync.

### 📌 Notes

- Your `serverSecret` should be kept **private**. Do not share it with others.
- If the server cannot connect to MineSphere, land data will still be managed locally — but cloud-based features will be disabled.
- MineSphere is included **for free** with your purchase of LandGuard.