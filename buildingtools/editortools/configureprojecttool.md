---
title: Configure Project Tool
nav_order: 1
parent: Tools User Guide
---

# Configure Project Tool

This tool simply sets up various required properties in your project, required by some of the other tools.

## Quick Overview

The Set Up tool:

- Adds 4 new "Layers" into your project, which are used to configure discrete "buckets" to manage interior and exterior building meshes, and interior and exterior props.
- Renames the existing "Rendering Layers", in index locations 1 and 2, used by the "Lighting Tools" to give you more control over how lighting effects various meshes in your building model.

## Parameters

These parameters can be configured on an instance of this tool:

| Parameter                    | Purpose                                                      |
| ---------------------------- | ------------------------------------------------------------ |
| Exterior Layer Name          | Name of the layer on which building exteriors (think outer walls, etc) will sit. |
| Interior Layer Name          | Name of the layer on which building interiors (think inner walls, etc) will sit. |
| Interior Props Layer Name    | Name of the layer on which interior props (think tables, chairs, rugs, etc) will sit. |
| Exterior Props Layer Name    | Name of the layer on which exterior props (think barrels, carts, stables, etc) will sit. |
| Exterior Renderer Layer Name | HDRP and URP Render Pipelines only. Name of Rendering Layer that will be influenced by Exterior lights. |
| Interior Renderer Layer Name | HDRP and URP Render Pipelines only. Name of Rendering Layer that will be influenced by Interior lights. |
