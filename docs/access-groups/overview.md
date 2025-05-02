---
slug: overview
title: Overview
tags: [access, access-group]
sidebar_position: 1
---

Access Groups in LandGuard are a core feature that determines what each player **who was added to the land** can or cannot do. Every land is protected based on the group a player belongs to. Groups define a set of permissions and access levels that control interactions such as block breaking, mob damage, chest access, and more.

There are three built-in groups by default — **Visitor**, **Member**, and **Admin** — but server administrators can customize or create new groups as needed. Land owners can assign members to these groups to control what they can do inside the land.

> 📝 Access groups can only control permissions for players that were added to the land. To control actions performed by players who are not part of the land you should use Flags.

### 🧍 Access Levels

The **Access Level** of a group determines the hierarchy of the group, where a higher number indicates more permissions. 

It is also used to determine the order of the groups when promoting or demoting members. For example, if a player in the **Visitor** group (access level 0) is promoted, it will land in the **Member** group (access level 1), and, if promoted again, it will be added to the **Admin** group (access level 2).

On the other hand, if a player in the **Admin** group (access level 2) is demoted, it will be moved to the **Member** group (access level 1), and, if demoted again, it will be moved to the **Visitor** group (access level 0).

