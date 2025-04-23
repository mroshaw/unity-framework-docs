---
title: Add Doors Tool
nav_order: 6
parent: Tools User Guide
---

# Add Doors Tool

This tool helps you to quickly add functioning doors to your building Game Object.

## Quick Overview

The Add Doors tool:

- Adds a "Door" component to mesh Game Objects found by searching for particular name patterns.
- Adds "Door Triggers" to the door, allow it to open and close as the player approaches and leaves the area of the door.
- Adds Audio Clips that play when the door is opening and closing.
- Ensures the "Static Flags" are set to allow the door to move.

## Parameters

These parameters can be configured on an instance of this tool:

| Parameter                  | Purpose                                                      |
| -------------------------- | ------------------------------------------------------------ |
| Door Names                 | Game Objects that contain any of these strings will be configured as doors. |
| Door Opening Clips         | Optional audio clip(s) that play when the door starts opening. If multiple clips are added, a random clip will be played. |
| Door Open Clips            | Optional audio clip(s) that play when the door completes opening. If multiple clips are added, a random clip will be played. |
| Door Closing Clips         | Optional audio clip(s) that play when the door starts closing. If multiple clips are added, a random clip will be played. |
| Door Closed Clips          | Optional audio clip(s) that play when the door completes closing. If multiple clips are added, a random clip will be played. |
| Door SFX Group             | The AudioMixerGroup used to play the door audio sounds.      |
| Door Trigger Layer Mask    | When a collider enters the door trigger, only colliders on any of the identified layers will be considered for triggering the door. |
| Door Trigger Tags          | When a collider enters the door trigger, only colliders with any of the identified tags will be considered for triggering the door. |
| Door Collider Height       | The height of the colliders created on either side of the door. |
| Door Collider Depth        | The depth (distance from the door) of the colliders created on either side of the door. |
| Override Collider Width    | By default, the trigger width is calculated based on the width of the door. Tick this to override that with a fixed value. |
| Door Collider Width        | The override width of the colliders, if the override flag is set. |
| Moveable Mesh Static Flags | Static flags to be applied to the door. Generally "Nothing" to allow the door to be animated. |
