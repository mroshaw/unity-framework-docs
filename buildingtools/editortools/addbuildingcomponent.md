---
title: Add Building Tool
nav_order: 2
parent: Building Editor Tool Window
---

# Add Building Tool

This tool gets your selected Game Object ready for use by other tools in the package.

## Quick Overview

The Add Building Component tool:

- Adds a "Building" component to your selected Game Object, if such a component does not already exist.

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

## Detailed Usage

There's nothing more to this tool. Simply click to add the component and configure using the instructions above.
