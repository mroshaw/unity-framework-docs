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
Tools > Daft Apple Games > Building Tools > Building Editor
```

The window looks like this:

![](.\media\buildingeditorwindow.png)

Each button represents a specific "Tool" in the package and will apply it's changes to the Game Object that is currently selected in the scene hierarchy. You can click the cog icon to select the tools configuration Scriptable Object instance in the project. You can find details of each of the tools using the navigation links on this page. All actions are applied to a single building Game Object that you select in the scene hierarchy. Support for applying changes directly to prefab assets is in the works.

> [!TIP]
>
> All of the tools use the "Undo" feature of the Unity editor. Having run any one of the tools, you can completely undo any changes made via the "Undo History" menu item.

> [!NOTE]
>
> Generally, the tools will work fine with prefab variants in the scene. In some cases, such as where you need to move prop Game Objects within the parent Game Object structure, you may need to unpack the prefab.

