---
title: Building Editor Tool Window
nav_order: 6
parent: Building Tools
---

# Building Editor Tool

## Introduction

The Building Editor Tool is designed as a "one stop shop" for applying a number of changes to a building model or prefab instance.


You'll find specific details and instructions for each of the core tools in the links on the left.

## The Building Editor Window

The main editor window can be accessed via the Unity editor menu:

```
Daft Apple Games > Building Tools > Building Editor
```

The window looks like this:

![](.\media\buildingeditorwindow.png)

Each button represents a specific "Tool" in the package. You can find details of each of the tools using the navigation links on the left.

> [!TIP]
>
> All of the tools use the "Undo" feature of the Unity editor. Having run any one of the tools, you can completely undo any changes made via the "Undo History" menu item.

All actions are applied to a single building Game Object that you select in the scene hierarchy.

> [!NOTE]
>
> Generally, the tools will work fine with prefab variants in the scene. In some cases, such as where you need to move prop Game Objects within the parent Game Object structure, you may need to unpack the prefab. Support for applying changes directly to prefab assets is in the works.

## Building Wizard Editor Settings

The specific presets and properties applied by each tool is driven by an instance of a Scriptable Object of type `BuildingWizardEditorSettings`. When you install the sample packages, you'll see a number of instances of this object installed, each containing preconfigured values that drive all of the tools.

Within the description of each tool in the pages that follow, you'll see how each feature and function uses these values. You can create your own presets by either copying an existing preset instance or using this menu item:

`Assets > Create > Daft Apple Games > Building Tools > Building Wizard Editor Settings`

![](.\media\createnewsettings.png)
