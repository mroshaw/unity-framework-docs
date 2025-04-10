---
title: Package Overview
nav_order: 1
parent: Building Tools Introduction
---

# Package Overview

Building Tools is in active development, completely free, and open source. I'm always adding new tools and functions, so keep coming back here to see what's new!

## Core Functions

The latest version of Building Tools provides these functions:

- **Initialise Building**
  - Adds a new `Building` component, providing core component functionality to your building.
  - Shifts the anchor of the building so that it is easier to place on an uneven surface, such as a terrain.
- **Configure Meshes**
  - Applies configurable `MeshRenderer` preset properties to all Exterior, Interior and Props meshes.
    - For example, presets can be created for "Lightmapped Meshes" with properties set for consistent lighting to be applied to all "Outdoor Props"
- **Configure Props**
  - Adds any missing `Colliders` to props, such as barrels, crates, carpets, chairs, tables, etc.
  - Aligns any outdoor props to the terrain, such as barrels, stables, and fences.
- **Configure Doors**
  - Adds a `Door Controller` component and configures `Door` components on all door mesh games objects, giving you lots of control over the state of doors within a building.
  - Adds `Door Trigger` components that open and close doors when a player enters the trigger, plays audio effects, and provides `Unity Events` to hook in your own functionality.
- **Configure Lighting**
  - Adds a `Lighting Controller` component and configures `BuildingLight` components on all lights within your building Game Object. This gives you loads of control over light states, with specific public methods for turning on and off candles, fires, and outdoor lights.
  - Preconfigure light properties, allowing you to apply consistent preset light properties (think intensity, range, temperature etc), across all similar light types.
  - Replaces `Lens Flare` components with `SRP Lens Flare` components. (**URP and HDRP only**)
  - Optionally adds a `OnDemandShadowMapUpdate` component, allowing you to fine tune shadow updates on individual lights, offering significant performance gains. (**URP and HDRP only**)
  - Samples include very simple `TimeOfDay` component, demonstrating how lights can be turned on and off as time progresses.
- **Configure Volumes**
  - Adds a lighting `Volume` with an "interior volume profile", allowing you to fine tune lighting within the bounds of your building. (**URP and HDRP only**)
  - Adds an `Interior Audio Filter` component that allows you to "muffle" ambient / outdoor audio when the player is in your building.
  - Components provide `UnityEvents` that you can hook into to trigger your own functionality when a player or character enters and leaves the building.
- **Mesh Optimisation**
  - Combines exterior, interior and prop meshes into merge meshes within your building. Greatly reduces draw calls and shadow casters and can offer huge performance gains.

## Samples

The package comes with options samples, with preconfigured settings and sample assets to get you started. Included are some presets for working with 3D Forge Village Interiors and Exteriors assets, which is my primary use case when developing these tools.
