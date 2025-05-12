---
title: Apply Mesh Pre-sets Tool
nav_order: 6
parent: Tools User Guide
---

# Apply Mesh Pre-sets Tool

This tool configures meshes within your selected building Game Object, giving you control over various aspects of the building.

## Quick Overview

The Apply Mesh Pre-sets tool:

- Takes a set of preconfigured `MeshRenderer` parameter settings and applies them to all Interior, Exterior and Prop meshes in the selected game object.
  - All `MeshRenderer` properties can be configured, and support for pipeline specific properties is in the works.

The principle behind this tool is that you can configure a number of mesh "presets", for a number of use cases, and apply those presets consistently across all of the `MeshRenderer` components in a building. The main use case that I've catered for is how the meshes respond to lighting. For example, I can create pre-sets for "lightmap baked" mesh renderers, with specific shadow casting properties, and than apply those settings to all of the exterior meshes of my building. Doing this manually is painstaking, especially when you want to try different variations of settings on buildings with a large number of mesh renderers.

![](..\media\meshpresetsbefore.png)

In the screenshot above, you'll see that all of the exterior meshes are configured to receive light from the "Default" render layer. Light probes are off, and there are some other settings applied to the meshes. Clicking the mesh tool button results in some changes:

![](..\media\meshpresetsafter.png)

As you can see, all of the exterior meshes are now receiving light from the "Exterior" layer, which happens to be the layer that the directional light is influencing. All meshes are now configured to cast static shadows and receive indirect light from light probes.

## Parameters

These parameters can be configured on an instance of this tool:

| Parameter                   | Purpose                                                      |
| --------------------------- | ------------------------------------------------------------ |
| Interior Mesh Settings      | Mesh presets to be applied to all interior building mesh renderers. |
| Exterior Mesh Settings      | Mesh presets to be applied to all exterior building mesh renderers. |
| Interior Prop Mesh Settings | Mesh presets to be applied to all interior prop mesh renderers. |
| Exterior Prop Mesh Settings | Mesh presets to be applied to all exterior prop mesh renderers. |

### Mesh Pre-sets

Each of the "Mesh Settings" properties of this tool are themselves Scriptable Object instances. Each instance has these parameters, which are derived directly from the "Mesh Renderer" component in Unity. Therefore, you can refer to the [Unity Mesh API page](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/MeshRenderer.html) for details of each of the properties.

Currently supported properties are:

| Parameter              | Notes                                                        |
| ---------------------- | ------------------------------------------------------------ |
| Layer Name             |                                                              |
| Static Editor Flags    | Includes what is surfaced as "Contribute GI" in the Unity Inspector. |
| Shadow Casting Mode    |                                                              |
| Static Shadow Caster   |                                                              |
| Receive GI             |                                                              |
| Light Probe Usage      |                                                              |
| Reflection Probe Usage | Built In Render Pipeline only.                               |
| Scale in Lightmap      | HDRP and URP only.                                           |
| Motion Vectors         |                                                              |
| Dynamic Occlusion      |                                                              |
| Rendering Layer Mask   | HDRP and URP only.                                           |
| Priority               | HDRP and URP only.                                           |
