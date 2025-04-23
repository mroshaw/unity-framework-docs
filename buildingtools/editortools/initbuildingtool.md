---
title: Initialize Building Tool
nav_order: 3
parent: Tools User Guide
---

# Initialize Building Tool

This tool gets your selected Game Object ready for use by other tools in the package, and makes positioning the building easier.

## Quick Overview

The Add Building Component tool:

- Adds a "Building" component to your selected Game Object, if such a component does not already exist.
- Moves the children of the Game Object so that the effective building anchor allows for an amount of plinth to be shown. This makes positioning the building on an uneven surface, such as a Terrain, much easier.

> [!IMPORTANT]
>
> Having run the tool, there is a manual step you must complete before using any of the other tools!

You must configure the component by dragging child Game Objects from your building into the slots to define:

- Groups of meshes representing the "Exterior" of your building.
- Groups of meshes representing the "Interior" of your building.
- Groups of meshes representing any "Indoor Props" that existing within your building.
- Groups of meshes representing any "Outdoor Props" that existing within your building instance or prefab.

> [!IMPORTANT]
>
> If your "Props" meshes sit within the "Exterior" or "Interior" of your building, from a hierarchy perspective, then you must move them outside of those game objects.

## Parameters

These parameters can be configured on an instance of this tool:

| Parameter            | Purpose                                                      |
| -------------------- | ------------------------------------------------------------ |
| Adjust Anchor Height | How far "up" all Mesh Renderers are raised above the current anchor position of the main building Game Object. |
