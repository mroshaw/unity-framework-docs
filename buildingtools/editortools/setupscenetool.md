---
title: Set Up Scene Tool
nav_order: 2
parent: Tools User Guide
---

# Set Up Scene Tool

This tool sets up dependent objects and components that are active in your currently open scene or scenes.

## Quick Overview

The Set Up Scene tool:

- Looks for a single "Directional" light in your scene and configures the "Lighting Layers", "Rendering Layers", or "Culling Layers", depending on which render pipeline is currently in use for the open project. This effectively tells the main scene `Light` (for example, the sun), exactly what meshes are influenced by it's light.
- Adds an `OnDemandShadowMapUpdate` component, if configured to do so, that helps control the frequency of shadow updates triggered by the directional light. This can significantly improve the performance of shadow rendering in the scene. 

## Parameters

These parameters can be configured on an instance of this tool:

| Parameter                              | Purpose                                                      |
| -------------------------------------- | ------------------------------------------------------------ |
| Directional Light Rendering Layer Mask | HDRP and URP Render Pipelines only. Determines which meshes are influence by the main directional light, driven by "Rendering Layers", which is a concept only supported in the "Scriptable" rendering pipelines. |
| Directional Light Culling Layer Mask   | Built In Render Pipeline only. Determines which meshes are influence by the main directional light, driven by the mesh renderer Game Object layers. |
| Add On Demand Shadow Map Component     | HDRP and URP Render Pipelines only. If true, an `OnDemandShadowMapUpdate` component will be added to your main Directional Light. This can be configured to update the shadow on the light every n frames or m seconds. This can be a significant performance improvement if you are currently updating shadows every frame. |
| Shadow Refresh Rate                    | HDRP and URP Render Pipelines only. Sets the number of frames to wait before refreshing the shadows of a light, driven by the new `OnDemandShadowUpdate` component. |

