---
title: Set Up Lighting Tool
nav_order: 8
parent: Tools User Guide
---

# Set Up Lighting Tool

This tool configures lights within your selecting building Game Object and adds components to give you control over their function.

## Quick Overview

The Set Up Lighting tool:

- Adds a `BuildingLight` component to each light within the building, giving more granular control over it's function.
- Adds a `BuildingLightController` to the building, allowing you to control groups of lights within the building structure.
- Configures lights for any one of three types, identified by the containing Game Object name:
  - Indoor candles
  - Indoor fires (cookers, fireplaces)
  - Outdoor lights
- Configures the range, intensity, and colour depending on the type of light.
- Adds a `BuildingLightManager` singleton component, which gives you complete control of all building lights in the scene.
- Removes unsupported "built in" Flare components when using URP or HDRP pipelines.
- Replaces "built in" Flare components with SRP Flare components, along with a preconfigured sample flare setup.
- Configures the `RenderingLayerMask` or `CullingLayerMask`, depending on the active render pipeline.
  - This gives you control over the influence of exterior, interior and lights based on where a mesh is located inside or outside your building.
- Adds an `OnDemandShadowMapUpdate` component, if configured to do so, that helps control the frequency of shadow updates triggered by the light. This can significantly improve the performance of shadow rendering in the scene.

There are two primary goals of this tool:

**Consistent Lighting** - apply consistent lighting settings across different types of light in your building. For example, you may want all candles within buildings to share intensity, range, and colour temperature. You may want all interior lights to only impact interior meshes. You can do this by applying "lighting presets" configured within the tools:

![](..\media\lightsettings.png)

**Granular Lighting Control** - provide components and methods to allow complete, and granular, control over the state of building lighting within open scenes. For example, using the sample `SimpleTimeOfDay` component in the samples, we can use events to turn all building lights on and off as the time of day changes:

![](..\media\timeofdayeventsexample.png)

## Building Light Components

There is a hierarchy of components, all optional, that can be added to your scene to give you control over lights in and around your buildings.

- Building Light Manager (scene wide control)
  - Building Light Controller (building wide control)
    - Building Light (individual light control)

The Building Light Manager is a singleton and so it's methods can be called from script anywhere using:

`BuildingLightManager.Instance` 

For example:

`BuildingLightManager.Instance.TurnOnCandleLights();`

This will turn on all indoor candle lights in all buildings in the current scene.

If you are using additive scenes, you can also add a `BuildingLightManagerMethods` component into any scene, and hook that into Unity events. So you can trigger an event in one scene, calling a `BuildingLightManagerMethod` method that calls the singleton method, even though the manager itself is in a different scene. Just ensure you load and activate the scene with the manager before calling the event methods.

> [!IMPORTANT]
>
> If you are loading scenes additively, remember to call the `BuildingLightManager.RefreshLightControllers()` method once all scenes have been loaded. This will cause the manager to find all controllers across all open scenes.

## Parameters

These parameters can be configured on an instance of this tool:

| Parameter                       | Purpose                                                      |
| ------------------------------- | ------------------------------------------------------------ |
| Indoor Candle Light Settings    | Pre-sets to be applied to all "indoor candle" lights within the building. |
| Indoor Fire Light Settings      | Pre-sets to be applied to all "indoor fire" lights (for example, cookers, hearth fires etc) within the building. |
| Outdoor Building Light Settings | Pre-sets to be applied to all "outdoor" lights within the building Game Object hierarchy. |
| Add Light Manager               | If checked, will add a Light Manager Game Object and singleton component if one does not already exist in the scene. |
| Light Manager Game Object Name  | If a new Light Manager is created, it will be created in a Game Object at the root of your active scene, and given this name. |

Each of these properties is itself an instance of a class with the following properties:

| Parameter                          | Purpose                                                      |
| ---------------------------------- | ------------------------------------------------------------ |
| Building Light Type                | The type of light to which these settings apply. You should only have one instance of each light type in a given tool configuration. |
| Mesh Names                         | Game Objects that contain any of these strings will be configured as Lights by the tool. |
| Flame Names                        | Game Objects that contain any of these strings will be configured as flames by the tool. This is then used to toggle flames on and off along with the light itself. |
| Use Lens Flare                     | Determines whether Lens Flare components should be added and configured for this light type. |
| Lens Flare Intensity               | The intensity of the lens flare, if one is added.            |
| Lens Flare Data                    | HDRP and URP Render Pipelines only. SRP Lens Flare configuration for the lens flare, if one is added. |
| Add On Demand Shadow Map Component | HDRP and URP Render Pipelines only. If true, an `OnDemandShadowMapUpdate` component will be added to the light. This can be configured to update the shadow on the light every n frames or m seconds. This can be a significant performance improvement if you are currently updating shadows every frame. |
| Shadow Refresh Rate                | HDRP and URP Render Pipelines only. Sets the number of frames to wait before refreshing the shadows of a light, driven by the new `OnDemandShadowUpdate` component. |
| Preset Settings                    | Light properties to be applied to each light. See the "Light Presets" section below. |

### Light Presets

Each of the "Preset Settings" properties of this tool are themselves Scriptable Object instances. Each instance has these parameters, which are derived directly from the "Light" component in Unity. Therefore, you can refer to the [Unity Light API page](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Light.html) for details of each of the properties.

Currently supported properties are:

| Parameter                      | Notes                               |
| ------------------------------ | ----------------------------------- |
| Range                          |                                     |
| Intensity                      |                                     |
| Radius                         | HDRP and URP Render Pipelines only. |
| Rendering Layer Mask           | HDRP and URP Render Pipelines only. |
| Culling Layer Mask (BIRP only) | Built In Render Pipeline only.      |
| Filter Color                   |                                     |
| Temperature                    |                                     |
| Lightmap Bake Type             |                                     |
