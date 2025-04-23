---
title: Set Up Scene Tool
nav_order: 2
parent: Tools User Guide
---

# Set Up Scene Tool

This tool sets up dependent objects and components that are active in your currently open scene or scenes.

## Quick Overview

The Set Up Scene tool:

- Looks for a single "Directional" light in your scene and configures the "Lighting Layers", "Rendering Layers", or "Culling Layers", depending on which render pipeline is currently in use for the open project.

What this does is tells the main scene `Light` (for example, the sun), exactly what meshes are influenced by it's light.

## Parameters

These parameters can be configured on an instance of this tool:

| Parameter                                                  | Purpose                                                      |
| ---------------------------------------------------------- | ------------------------------------------------------------ |
| Directional Light Rendering Layer Mask (URP and HDRP only) | Determines which meshes are influence by the main directional light, driven by "Rendering Layers", which is a concept only supported in the "Scriptable" rendering pipelines. |
| Directional Light Culling Layer Mask (BIRP only)           | Determines which meshes are influence by the main directional light, driven by the mesh renderer Game Object layers. |

