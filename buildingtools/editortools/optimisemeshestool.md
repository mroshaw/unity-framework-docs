---
title: Optimise Meshes Tool
nav_order: 9
parent: Tools User Guide
---

# Optimise Meshes Tool

This tool helps to reduce the number of draw calls and shadow casters on your selected building Game Object. This can greatly improve the performance of your project.

## Quick Overview

The Optimise Meshes Tool:

- Combines meshes from interior, exterior, interior prop and exterior prop layers respectively, generating one mesh per material for each group.
- Ignores meshes that have been flagged by the "Ignore Mesh Combine" component, where dynamic behaviour is required. For example, moving doors.
- Saves the combined meshes as assets and reconfigures the Game Object to use the new meshes.

You can also opt to merge the whole building, by unticking the "Combine Meshes by Layer" parameter. This means meshes that share materials across interior, exterior and prop layers will be merged, giving you less control over the behaviour of light on the resulting mesh renderers.

The resulting merge meshes are saved as assets, to be folder specified in the parameters - the folder is created in the "Assets" directory in your project, if it doesn't already exist.

![](..\media\optimisemeshes.png)

In the image above, you can see that all of the exterior meshes have been combined into a small number of larger meshes, one mesh for each unique material.

Once you've run the tool against a building, you'll notice a new component has been added to the Game Object, called `MeshCombineRollBack`. The purpose of this component is, unsurprisingly, to allow you to undo the process and restore the Game Object. It does this by storing an "Audit" of the changes made by the optimisation process to that specific building Game Object, and provides a button that allows you to undo those changes. Specifically, this component will:

1. Re-enable all of the original Mesh Renderers that it deactivated.
2. Delete the merge mesh Game Objects from your building.
3. Delete the mesh and Game Object prefab assets that were created.
4. Delete the `MeshCombineRollBack` component itself.

You can optionally retain any or all of the deleted objects by unchecking the corresponding checkbox in the component inspector, prior to clicking the button. You can also remove the audit altogether, if it's starting to take up too much space in your scene asset for example, by simply removing the component from the Game Object. You will, of course, then lose the ability to easily roll back.

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
| Combined Mesh Presets   | This is an instance of the Apply Mesh Presets Tool, and is used to apply pre-set parameters to the newly created merged meshes. Note that in the case of a "whole building" merge (if "Combine Meshes By Layer" is unchecked), then the resulting meshing will have the "Building Exterior" mesh pre-sets applied. |
