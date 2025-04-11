---
title: Fix Props Tool
nav_order: 4
parent: Building Editor Tool Window
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

## Detailed Usage

This tool uses these properties of the `BuildingWizardEditorSettings`:

![](..\media\propstoolsettings.png)
