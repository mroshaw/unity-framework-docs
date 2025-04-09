---
title: Installation
nav_order: 4
parent: Building Tools
---

# Uninstalling

A small number of steps are required to completely uninstall the Building Tools package.

## Remove the packages

You can uninstall the packages by selecting the package in Package Manager, under "In Project", and clicking the "Remove" button. You should remove the Building Tools package first, then the Core package:

![](E:\Dev\DAG\DAG Unity Framework Docs\buildingtools\media\uninstallpackages.png)

## Delete any installed samples

You can very easily remove the samples by simply deleting the folder that is automatically created by the package manager:

![](E:\Dev\DAG\DAG Unity Framework Docs\buildingtools\media\deletesamples.png)

## Restore Layers and Rendering Layers

### Layers

If you clicked the "Set Up" button, a number of Layers are created. You can undo this by going to your "Project Settings > Tags and Layers" and removing / updating the entries:

![](E:\Dev\DAG\DAG Unity Framework Docs\buildingtools\media\createdlayers.png)

### Rendering Layers

Again, only if you clicked "Set Up", two of the Rendering Layers have been renamed. You can undo this via "Project Settings > Tags and Layers":

![](E:\Dev\DAG\DAG Unity Framework Docs\buildingtools\media\renamedrenderlayers.png)

## Script Define Symbols

When first installing the "Daft Apple Core" package, it sets a Script Define Symbol to allow compilation of code specific to your render pipeline. To remove this, go to "Project Settings > Player" and simply delete the script define symbol with the prefix "DAG":

![](E:\Dev\DAG\DAG Unity Framework Docs\buildingtools\media\scriptdefines.png)

