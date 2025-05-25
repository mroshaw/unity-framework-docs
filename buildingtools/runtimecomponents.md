---
title: Building Runtime Components
nav_order: 10
parent: Building Tools
---

# Building Runtime Components Overview

Components are provided for use both in the "core" package, to be shared and used across all Daft Apple Unity Framework packages, and within the package itself.

## Building Components

The following runtime components are contained in the package, some of which are demonstrated in the sample scenes.

### Building

Mainly provides data storage for persistent properties of a building.

### BuildingLight

Controls a single `Light` component within a building.

### BuildingLightController

Controls all instances of `BuildingLights` within a building.

### BuildingLightManager

Controls all instances of `BuildingLightController` across all open scenes.

### BuildingLightManagerMethods

Provides access to methods on the `BuildingLightManager` singleton from event handlers in any open scenes.

### Door

Provides methods and properties for opening and closing doors.

### DoorController

Controls all doors within a building

### DoorTrigger

Uses a `BoxCollider` to trigger the opening and closing of doors.

### DynamicMeshRenderer

A simple "placeholder" component used to prevent merging of dynamic meshes and to ensure appropriate static flags are applied.

### InteriorAudioFilter

Uses a `BoxCollider` to apply a "muffled" sound to a given `AudioMixerGroup` when the collider is triggered.

### MeshCombineRollBack

Provides data storage and functions to rollback combined mesh changes.

### WindMill

Provides a simple component to rotate the blades of a windmill at a configurable speed.

## Core Components

A number of "core" components are provided in the core package that provide useful functions outside of the building tools package.

Documentation for those components can be found on the [Core Runtime Components](../runtimecomponents) page.
