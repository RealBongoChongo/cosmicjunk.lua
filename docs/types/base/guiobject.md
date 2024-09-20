---
layout: default
title: GUIObject
rank: 3
---

# GUIObject

The base class for every GUI object, used for screens

## Overview

|**Methods**                                              |
| :------------------------------------------------------ |
|`Destroy()` : void                                       |
|`ChangeProperties(Properties)` : void                    |

$~$

## Methods

### `Destroy()` : void

Destroys the GUI object

$~$

### `ChangeProperties(Properties)` : void

Changes the properties of a GUI object

|**Parameters** | Type   |
| :------------ | ------ |
| Properties    | Object |

#### Code Example

```lua
local screen = GetPartFromPort(1, "Screen")

local textLabel = screen:CreateGUI("TextLabel", {
  Size = UDim2.new(0, 100, 0, 100);
  Position = UDim2.new(0, 100, 0, 100);
  BackgroundColor3 = Color3.new(1,0,0);
  TextColor3 = Color3.new(1,1,1);
})

textLabel:ChangeProperties({Text = "White text"})
```
