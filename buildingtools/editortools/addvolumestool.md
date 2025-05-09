---
title: Add Volumes Tool
nav_order: 7
parent: Tools User Guide
---

# Add Volumes Tool

This tool sets up "Volumes", which are areas that encompass your selected building Game Object, allowing you to configure various functions that trigger as a player moves up and out of the building.

## Quick Overview

The Add Volumes tool:

- Adds an "Interior Volume" (HDRP and URP only) that gives you control over lighting when the player enters the building.
- Adds an "Interior Audio Filter" component, that allows you to create a "muffled" sound for outdoor/ambient audio when the player enters the building.

The "bounds" of the building are calculated by combining the bound extends of all meshes within a configurable layer - this is the "BuildingExterior" layer by default. You can fine tune this by excluding specific mesh renderer in Game Object names containing any number of strings, all using the parameters described below. The tool uses this to create a `BoxCollider`, set as a trigger, that is used to control components that do different things when a collider (e.g. the player) enters and leaves this collider. 

![](..\media\addvolumes.png)

Due to certain mesh renderers, such as over-hangs on ceilings, you may have to tweak the final collider size manually, to contain only the "interior" areas of your building.

The layers of colliders checked, and tags that will cause the triggers to fire, are configurable via the parameters described below. They can also be modified directly on the corresponding components that are attached to the "Interior Volume" Game Object that is created by this tool.

> [!IMPORTANT]
>
> You should add and configure volumes before optimising the building meshes. Otherwise, the calculation of the building bounds will not be able to consider smaller meshes for exclusion, and the result may be that the volume encompasses a larger area than desired. You can manually re-size the collider after it has been created.

## Parameters

These parameters can be configured on an instance of this tool:

| Parameter                                   | Purpose                                                      |
| ------------------------------------------- | ------------------------------------------------------------ |
| Mesh Size Ignore Names                      | When determining the "bounds" of a building, any mesh renderer Game Objects containing these names are ignored by the calculation, as are any of their children. Can be used to remove "invisible" meshes, such as those under the ground or that "overhang" the interior space, from the calculation. |
| Interior Volume Game Object Name            | Name of the Game Object created, if not there already, that contains the various volume components. |
| Interior Volume Profile (HDRP and URP only) | Selected Volume Profile that will be applied when the player/camera enters the building. |
| Indoor Snapshot                             | AudioMixer Snapshot corresponding to the AudioMixer profile that is applied when the player/camera enters the building. Typically contains "Lowbypass/Highbypass" filters to "muffle" the audio. |
| Outdoor Snapshot                            | AudioMixer Snapshot corresponding to the AudioMixer profile that is applied when the player/camera exists the building. Typically a "clean" snapshot profile. |

