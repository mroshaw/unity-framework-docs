---
title: Installation
nav_order: 3
parent: Building Tools
---

# Installation

## Package dependencies

The package relies on a number of scripts and resources in the "daftapple-core" package. You must install this first through package manager:

1. Open the package manager window.
2. From the menu in the top left, pick "Install package from git URL..."
3. Copy and paste this URL: `https://github.com/mroshaw/daftapple-core.git`
4. Click install.

You can now install the "building-tools" package by following the same process with this URL:

`https://github.com/mroshaw/building-tools.git`

The package has these Unity dependencies, which you'll be prompted to install:

- Splines 2.7.2 (com.unity.splines)

## Project settings

In order to implement some of the functionality, the package requires specific `Layers` and `RenderingLayers` to be present in your project settings.

You can either add these manually, or using the "Set up" button in the main editor window. Note that this automated processed will look for available slots for tags and layers and won't overwrite what's there. Rendering Layer names are, however, overwritten.

To configure these manually, go to Edit > Project Settings > Tags and Layers...

Add the following `Layers` - it doesn't matter at what index they are added:

- BuildingExterior
- BuildingInterior
- ExteriorProps
- InteriorProps

Update the following `Rendering Layers`, setting the name for the given layer index:

- 1 - External
- 2 - Internal

## Install Samples

The package comes with a sample folder contain some example assets, such as door sounds and an AudioMixer, and presets for the "3D Forge" building assets. Due to the way lighting works in Unity, there are sample packages for each of the three render pipelines, and you should import the one relevant to your project. The render pipeline specific packages rely on shared assets from the "Sample Assets" package, so please install this first.

 You can install the samples via the Package Manager by selecting the "Daft Apple Building Tools" package, clicking "Samples" and clicking the "Import" button next to the packages you want to install:

![](.\media\importsamples.png)

