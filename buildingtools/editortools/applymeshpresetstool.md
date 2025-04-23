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

## Parameters

These parameters can be configured on an instance of this tool:

| Parameter                   | Purpose                                                      |
| --------------------------- | ------------------------------------------------------------ |
| Interior Mesh Settings      | Mesh pre-sets to be applied to all interior building mesh renderers. |
| Exterior Mesh Settings      | Mesh pre-sets to be applied to all exterior building mesh renderers. |
| Interior Prop Mesh Settings | Mesh pre-sets to be applied to all interior prop mesh renderers. |
| Exterior Prop Mesh Settings | Mesh pre-sets to be applied to all exterior prop mesh renderers. |

### Mesh Pre-sets

Each of the "Mesh Settings" properties of this tool are themselves Scriptable Object instances. Each instance has these parameters, which are derived directly from the "Mesh Renderer" component in Unity. Therefore, you can refer to the [Unity Mesh API page](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/MeshRenderer.html) for details of each of the properties.

Currently supported properties are:

| Parameter                                | Notes |
| ---------------------------------------- | ----- |
| Layer Name                               |       |
| Static Editor Flags                      |       |
| Shadow Casting Mode                      |       |
| Static Shadow Caster                     |       |
| Receive GI                               |       |
| Contribute GI                            |       |
| Light Probe Usage                        |       |
| Scale in Lightmap                        |       |
| Motion Vectors                           |       |
| Dynamic Occlusion                        |       |
| Rendering Layer Mask (HDRP and URP only) |       |
| Priority                                 |       |
