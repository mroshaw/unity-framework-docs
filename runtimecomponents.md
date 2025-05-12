---
title: Core Runtime Components
nav_order: 6
---

# Core Runtime Components Overview

The following components are provided for use by the "core" package.

## Lighting

Generic components used to enhance lighting in Unity projects.

### OnDemandShadowUpdate

Controls the frequency at which shadows are updated on `Light` components in the scriptable render pipelines.

## Gameplay

Generic components used to provide gameplay features.

### ActionTrigger

Works with a `Collider` to trigger events based on collisions with configurable tags and layers.

## Pooling

Generic components that provide abstract methods over the Unity pooling functionality.

### PrefabPool

Provides configurable pools of prefab instances for use in spawning. For example, this is very useful when spawning footprints, bullets, or blood spatters.

## Scenes

Components used to control and manage scene loading, including loading multiple additive scenes in a project.

### AdditiveSceneLoader

Provides a mechanism to configure and load multiple scenes. Includes a number of `UnityEvents` that can be used to trigger additional code over the duration of loading and activating multiple scenes.

### ProgressSlider

Works with the `AdditiveSceneLoader` to display a progress bar as multiple scenes are loaded additively.

### SceneFader

Can be used to fade in and out a black canvas as part of the scene loading process.

### SceneLoaderEvents

Allows hooking into `AdditiveSceneLoad` Unity Events from scenes outside of the one hosting the main component singleton.

### SceneLoaderManager

A singleton component class that gives control of scene loading from anywhere in code.
