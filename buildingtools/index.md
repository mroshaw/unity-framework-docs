---
title: Building Tools Introduction
nav_order: 1
parent: Building Tools
---

# Daft Apple Building Tools

This package provides editor tools and run-time components to allow quick, consistent configuration of building assets in a Unity project. This includes setting up efficient and effective lighting, alignment of props with the terrain, automatically adding working doors, and mesh optimisation. The package comes with pre-sets and examples for configuring the excellent 3D Forge village assets. Third party assets are not required to use this package, however.

![](.\media\buildingtoolsbanner.png)

> [!IMPORTANT]
>
> This package is supported in Unity 6 LTS ONLY! A number of useful changes came into Unity 6 and I've made use of these where possible in this package. I have tested in Unity 6 ONLY and would expect compilation errors and general failures if used with an earlier version of Unity.

This package was designed to be as innocuous as possible:

- All Editor specific script is contained within "Editor Only" assembly definitions. So the package won't add unnecessary code to your game builds.
- All Run Time components are granular and optional. Nothing is enforced by the package - if you want to remove a particular component, then you can.
- Code is clean and as error and warning free as possible. I hate it when I install third party packages and am met by hundreds of compiler warnings! I've done my best to ensure this doesn't happen, and that the code is well structured, easy to follow, and easy to extend.

