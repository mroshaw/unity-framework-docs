---
title: Initialize Building Tool
nav_order: 3
parent: Tools User Guide
---

# Initialize Building Tool

This tool gets your selected Game Object ready for use by other tools in the package, and makes positioning the building on uneven surfaces a little easier.

## Quick Overview

The Add Building Component tool:

- Adds a "Building" component to your selected Game Object, if such a component does not already exist.
- Moves the children of the Game Object so that the effective building pivot allows for an amount of plinth to be shown. This makes positioning the building on an uneven surface, such as a Terrain, a little easier.

> [!IMPORTANT]
>
> Having run the tool, there is a manual step you must complete before using any of the other tools!

You must configure the component by dragging child Game Objects from your building into the slots to define:

- Groups of meshes representing the "Exterior" of your building.
- Groups of meshes representing the "Interior" of your building.
- Groups of meshes representing any "Indoor Props" that exist within your building.
- Groups of meshes representing any "Outdoor Props" that exist within your building instance or prefab.

## Parameters

These parameters can be configured on an instance of this tool:

| Parameter           | Purpose                                                      |
| ------------------- | ------------------------------------------------------------ |
| Adjust Pivot Height | How far "up" all direct child Game Objects  are raised above the current pivot position of the main building Game Object. Set this to "0" if you don't want to apply any change to the pivot position. |
