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

## Parameters

These parameters can be configured on an instance of this tool:

| Parameter                                   | Purpose                                                      |
| ------------------------------------------- | ------------------------------------------------------------ |
| Mesh Size Ignore Names                      | When determining the "bounds" of a building, any mesh renderers on Game Objects containing these names are ignored by the calculation. Can be used to remove "invisible" meshes (such as those under the ground) from the calculation. |
| Interior Volume Game Object Name            | Name of the Game Object created, if not there already, that contains the various volume components. |
| Interior Volume Profile (HDRP and URP only) | Selected Volume Profile that will be applied when the player/camera enters the building. |
| Indoor Snapshot                             | AudioMixer Snapshot corresponding to the AudioMixer profile that is applied when the player/camera enters the building. Typically contains "Lowbypass/Highbypass" filters to "muffle" the audio. |
| Outdoor Snapshot                            | AudioMixer Snapshot corresponding to the AudioMixer profile that is applied when the player/camera exists the building. Typically a "clean" snapshot profile. |

