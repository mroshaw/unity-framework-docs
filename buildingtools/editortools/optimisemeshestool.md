---
title: Optimise Meshes Tool
nav_order: 8
parent: Building Editor Tool Window
---

# Optimise Meshes Tool

This tool helps to reduce the number of draw calls and shadow casters on your selected building Game Object. This can greatly improve the performance of your project.

## Quick Overview

The Optimise Meshes Tool:

- Combines meshes from interior, exterior, interior prop and exterior prop layers respectively, generating one mesh for each group.
- Ignores meshes that have been flagged by the "Ignore Mesh Combine" component, where dynamic behaviour is required. For example, moving doors.
- Saves the combined meshes as assets and reconfigures the Game Object to use the new meshes.

## Detailed Usage
