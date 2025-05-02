---
slug: getting-started
title: Getting Started
tags: [api, getting-started]
sidebar_position: 1
---

The LandGuard API allows developers to build extensions and custom functionality on top of LandGuard. Whether you want to create new land-related mechanics or hook into the protection system to develop advanced integrations, the API gives you full programmatic access to LandGuard’s core features.

The API is published on Maven Central via Sonatype, making it easy to add to any Java project.

## 📦 Maven Dependency

To include the API in your own plugin, simply add the following Maven dependency to your `pom.xml`:

```xml
<dependency>
    <groupId>io.github.hugo1307</groupId>
    <artifactId>landguard-api</artifactId>
    <version>1.0.0</version>
</dependency>
```

And, if you haven't already, add the Sonatype repository to your `pom.xml`:

```xml
<repositories>
    <repository>
        <id>sonatype</id>
        <url>https://oss.sonatype.org/content/groups/public/</url>
    </repository>
</repositories>
```

## 📦 Gradle Dependency

To include the API in your own plugin, simply add the following Gradle dependency to your `build.gradle`:

```groovy
dependencies {
    implementation 'io.github.hugo1307:landguard-api:1.0.0'
}
```

And, if you haven't already, add the Sonatype repository to your `build.gradle`:

```groovy
repositories {
    mavenCentral()
}
```

## 🛠️ What You Can Do with the API

With the LandGuard API, developers can:

- **Query and manage lands:** Fetch land information, check ownership, and interact with access groups.
- **Create custom flags or permission logic:** Add new types of protection or automation.
- **Listen for events:** React to changes in land status, flags, or membership through the API’s event system.
- **Create custom commands or GUIs:** Extend LandGuard’s capabilities with your own player-facing tools.
- **Integrate with other plugins:** Sync LandGuard with economy plugins, GUI tools, world-editing tools, and more.


## 🔌 Creating Add-ons

LandGuard was built with extensibility in mind. You can develop add-ons (separate plugins) that depend on LandGuard and tap into its API to enhance or alter the experience.

**Example Use Cases:**

- A plugin that prevents land actions during certain server events
- An improved GUI-based land management tool
- Integration with Discord for land notifications
- Create rich economy features like rentals or land auctions
