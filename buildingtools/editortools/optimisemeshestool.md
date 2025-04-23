---
title: Optimise Meshes Tool
nav_order: 9
parent: Tools User Guide
---

# Optimise Meshes Tool

This tool helps to reduce the number of draw calls and shadow casters on your selected building Game Object. This can greatly improve the performance of your project.

## Quick Overview

The Optimise Meshes Tool:

- Combines meshes from interior, exterior, interior prop and exterior prop layers respectively, generating one mesh for each group.
- Ignores meshes that have been flagged by the "Ignore Mesh Combine" component, where dynamic behaviour is required. For example, moving doors.
- Saves the combined meshes as assets and reconfigures the Game Object to use the new meshes.

## Parameters

These parameters can be configured on an instance of this tool:

| Parameter               | Purpose                                                      |
| ----------------------- | ------------------------------------------------------------ |
| Combine Meshes By Layer | If checked, meshes will be combined separately for each of the BuildngExterior, BuildingInterior, ExteriorProps and InteriorProps layers. If unchecked, the whole building will be merged as one. |
| Asset Output Folder     | Folder in the "Assets" folder where combined meshes and prefabs will be saved. |
| Asset File Name Prefix  | Prefix that will be added to each generated combined mesh and prefab. |
| Create Output Folder    | If the Asset Output Folder does not exist, checking this will cause the tool to create it. |
| Is 32Bit                | If checked, forces the created mesh to use a 32-bit index format. Otherwise, it will use a 16-bit index format. See [Mesh.indexFormat](https://docs.unity3d.com/6000.0/Documentation/ScriptReference/Mesh-indexFormat.html) for more details. |
| Generate Secondary UVs  | Forces the tool to generate the UVs for the new combined meshes. |
| Combined Mesh Presets   | This is an instance of the Apply Mesh Presets Tool, and is used to apply preset parameters to the newly created merged meshes. |
