---
title: Fix Props Tool
nav_order: 4
parent: Tools User Guide
---

# Fix Props Tool

This tool configures props, like barrels, crates, etc, within your building structures.

## Quick Overview

The Fix Props tool:

- Searches for mesh game objects by name and adds any missing Colliders.
  - For example:
    - Crates, chairs and tables get a `BoxCollider`
    - Barrells get a `CapsuleCollider`
    - Rugs and carpets get a `MeshCollider`
- Where exterior props sit directly on a Terrain in your scene, the props are aligned correctly to the terrain.

Props are identified by comparing Game Object names against the list provided in the configuration. The process does a `Contains` check, so the full Game Object name need only a partial match. For example, the name string 'crate' will match a Game Object called 'fe_vill_crate_11'. Unity automatically scales the collider to fit the mesh, but some minor adjustments may be required.

![](..\media\fixpropsbefore.png)

You'll see above that there are no colliders highlighted on the visible props, and some of the exterior props are hovering above the terrain. This is almost always going to be the case for assets, as the authors have to assume alignment to a flat surface. A click of a button on the fix props tool results in this:

![](..\media\fixpropsafter.png)

You'll see the colliders have been added and are highlighted in green by Unity. The barrels have been aligned to the terrain, not just matching the y axis, but aligned also to the slope of the terrain. The axis used in alignment can be modified by setting parameters, as described below.

## Parameters

These parameters can be configured on an instance of this tool:

| Parameter              | Purpose                                                      |
| ---------------------- | ------------------------------------------------------------ |
| Box Collider Names     | Game Objects with this string in their name, that contain a Mesh Renderer, will have a `BoxCollider` added, if one does not exist. |
| Sphere Collider Names  | Game Objects with this string in their name, that contain a Mesh Renderer, will have a `SphereCollider` added, if one does not exist. |
| Capsule Collider Names | Game Objects with this string in their name, that contain a Mesh Renderer, will have a `CapsuleCollider` added, if one does not exist. |
| Mesh Collider Names    | Game Objects with this string in their name, that contain a Mesh Renderer, will have a `MeshCollider` added, if one does not exist. |
| Terrain Align Position | If ticked, Game Objects on the terrain will be lowered to sit flush on the terrain. |
| Terrain Align Rotation | If ticked, Game Objects will be rotated to align with the contact point on the terrain. |
| Terrain Align X        | If ticked, align rotation will affect this axis. Untick to preserve the axis as is. |
| Terrain Align Y        | If ticked, align rotation will affect this axis. Untick to preserve the axis as is. |
| Terrain Align Z        | If ticked, align rotation will affect this axis. Untick to preserve the axis as is. |
