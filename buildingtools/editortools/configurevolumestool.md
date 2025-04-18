---
title: Add Volumes Tool
nav_order: 7
parent: Building Editor Tool Window
---

# Add Volumes Tool

This tool sets up "Volumes", which are areas that encompass your selected building Game Object, allowing you to configure various functions that trigger as a player moves up and out of the building.

## Quick Overview

The Add Volumes tool:

- Adds an "Interior Volume" (HDRP and URP only) that gives you control over lighting when the player enters the building.
- Adds an "Interior Audio Filter" component, that allows you to create a "muffled" sound for outdoor/ambient audio when the player enters the building.

## Detailed Usage

This tool uses these properties of the `BuildingWizardEditorSettings`:

![](..\media\volumetoolsettings.png)
