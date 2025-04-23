---
title: Set Up Lighting Tool
nav_order: 8
parent: Tools User Guide
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

## Parameters

These parameters can be configured on an instance of this tool:

| Parameter                       | Purpose                                                      |
| ------------------------------- | ------------------------------------------------------------ |
| Indoor Candle Light Settings    | Pre-sets to be applied to all "indoor candle" lights within the building. |
| Indoor Fire Light Settings      | Pre-sets to be applied to all "indoor fire" lights (for example, cookers, hearth fires etc) within the building. |
| Outdoor Building Light Settings | Pre-sets to be applied to all "outdoor" lights within the building Game Object hierarchy. |

Each of these properties is itself an instance of a class with the following properties:

| Parameter                               | Purpose                                                      |
| --------------------------------------- | ------------------------------------------------------------ |
| Building Light Type                     | The type of light to which these settings apply. You should only have one instance of each light type in a given tool configuration. |
| Mesh Names                              | Game Objects that contain any of these strings will be configured as Lights by the tool. |
| Flame Names                             | Game Objects that contain any of these strings will be configured as flames by the tool. This is then used to toggle flames on and off along with the light itself. |
| Use Lens Flare                          | Determines whether Lens Flare components should be added and configured for this light type. |
| Lens Flare Intensity                    | The intensity of the lens flare, if one is added.            |
| Lens Flare Data (HDRP and URP only)     | SRP Lens Flare configuration for the lens flare, if one is added. |
| Shadow Refresh Rate (HDRP and URP only) | Sets the number of frames to wait before refreshing the shadows of a light, driven by the new `OnDemandShadowUpdate` component. |
| Preset Settings                         | Light properties to be applied to each light. See the "Ligh Pre-sets" section below. |

### Light Pre-sets

Each of the "Preset Settings" properties of this tool are themselves Scriptable Object instances. Each instance has these parameters, which are derived directly from the "Light" component in Unity. Therefore, you can refer to the [Unity Light API page](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Light.html) for details of each of the properties.

Currently supported properties are:

| Parameter                                | Notes |
| ---------------------------------------- | ----- |
| Range                                    |       |
| Intensity                                |       |
| Radius (HDRP and URP only)               |       |
| Rendering Layer Mask (HDRP and URP only) |       |
| Culling Layer Mask (BIRP only)           |       |
| Filter Color                             |       |
| Temperature                              |       |
| Lightmap Bake Type                       |       |
