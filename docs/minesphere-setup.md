---
slug: minesphere-setup
title: MineSphere Integration
tags: [minesphere, config]
sidebar_position: 2
---

# Enabling MineSphere Integration

**MineSphere** is a powerful web-based platform that works seamlessly with LandGuard to provide players and server admins with an enhanced land management experience outside of Minecraft. Through MineSphere, users can view, organize, and manage their lands via an intuitive online dashboard — and even benefit from automatic cloud backups.

---

### 🌐 What is MineSphere?

MineSphere offers the following features:

- **Web Access to Lands:** Players can view their own lands and explore other players’ lands via a modern web UI.
- **Cloud Backups:** All land data is automatically backed up to the cloud, protecting against data loss in case of server failure.

### 🔐 Getting Started

To enable MineSphere on your server, follow these steps:

1. **Purchase LandGuard**  
   Only verified buyers can activate MineSphere integration.

2. **Join the [LandGuard Discord](https://discord.gg/ezxQGPpGGN)**  
   Write a message in the [#claim-offer](https://discord.com/channels/1288476967842218015/1368588484192768060) channel to request your **MineSphere credentials** (`serverId` and `serverSecret`). Here's an example message you can use:

   ```
   @Hugo1307 I have purchased LandGuard and would like to activate MineSphere. 
   
   Username: [YourUsername]
   Server Name: [Your Server's Name]
   Server Address: [The IP or domain of your server]
   ```

   > ℹ️ Make sure to replace the username by the one you used to purchase LandGuard in the BuiltByBit store.

3. **Receive your Credentials**  
   You will receive a private message with your **serverId** and **serverSecret**. These are unique identifiers for your server and are required to connect to MineSphere. Keep them safe and do not share them with anyone else!

4. **Update the Configuration File**  
   Open your `config.yml` and locate the `cloud` section. Fill in the credentials you received:

   ```yaml
   cloud:
     serverId: "your-server-id"
     serverSecret: "your-server-secret"
   ```

5. **Restart Your Server**  
   After saving the config, restart the server to apply the changes and activate cloud sync.

### 📌 Notes

- Your `serverSecret` should be kept **private**. Do not share it with others.
- If the server cannot connect to MineSphere, land data will still be managed locally — but cloud-based features will be disabled.
- MineSphere is included **for free** with your purchase of LandGuard.