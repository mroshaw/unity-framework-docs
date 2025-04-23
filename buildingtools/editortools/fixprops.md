---
title: Fix Props Tool
nav_order: 4
parent: Tools User Guide
---

# Fix Props Tool

This tool configures props, like barrells, crates, etc, within your building structures.

## Quick Overview

The Fix Props tool:

- Searches for mesh game objects by name and adds any missing Colliders.
  - For example:
    - Crates get a Box Collider
    - Barrells get a Capsule Collider
- Where props sit directly on a Terrain in your scene, the props are aligned correctly to the terrain.

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
