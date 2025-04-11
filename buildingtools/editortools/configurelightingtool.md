---
title: Set Up Lighting Tool
nav_order: 6
parent: Building Editor Tool Window
---

# Set Up Lighting Tool

This tool configures lights within your selecting building Game Object and adds components to give you control over their function.

## Quick Overview

The Set Up Lighting tool:

- Adds a "Lighting Controller" to the building, allowing you to control groups of lights within the building structure.
- Adds a "Building Light" component to each light within the building, giving more granular control over it's function.
- Configures lights for as one of three types, depending on the name:
  - Indoor candles
  - Indoor fires (cookers, fireplaces)
  - Outdoor lights

- Configures the range, intensity, color depending on the type of light.
- Removes unsupported "built in" Flare components when using URP or HDRP pipelines.
- Replaces "built in" Flare components with SRP Flare components, along with a preconfigured sample flare setup.
- Configures the interior, exterior and prop meshes based on their location, enabling "Probe" lighting support and associating meshes with interior, exterior or both Rendering Layers.
  - This gives you control over the influence of exterior, interior and directional lights based on where a mesh is located inside or outside your building.


## Detailed Usage

This tool uses these properties of the `BuildingWizardEditorSettings`:

![](..\media\lightingtoolsettings.png)
