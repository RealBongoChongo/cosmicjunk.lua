---
layout: default
title: Screen
rank: 3
---

# Screen
### Inherited from [BaseType](/cosmicjunk.lua/docs/types/BaseType)

A screen can be a powerful part when used correctly, allowing for custom statuses, interfaces, or even games to be displayed on them.

## Overview

| Properties         |
| ------------------ |
| `Objects` : Object |

| Methods                                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------------------- |
| `CreateGUI(GUIName : string, Properties : Object)` : [GUIObject](https://github.com/RealBongoChongo/cosmicjunk.lua/wiki/GUIObject) |
| `ClearGUI()` : void                                                                                                                |

<br />
<br />

## Properties

### `Screen.Objects` : Object

Returns a table of all the gui objects on the screen

<br />
<br />

## Methods

### `CreateGUI(GUIName : string, Properties : Object)` : [GUIObject](https://github.com/RealBongoChongo/cosmicjunk.lua/wiki/GUIObject)

Creates an element with a given gui object name and the properties of that gui object.

| Returns       | Type                                                                          |
| ------------- | ----------------------------------------------------------------------------- |
| GUIObject     | [GUIObject](https://github.com/RealBongoChongo/cosmicjunk.lua/wiki/GUIObject) |

#### Code Example

```lua
local screen = GetPartFromPort(1, "Screen")

local frame = screen:CreateGUI("Frame", {
  Size = UDim2.new(0, 100, 0, 100);
  Position = UDim2.new(0, 100, 0, 100);
  BackgroundColor3 = Color3.new(1,0,0);
})
```

<br />
<br />

### `ClearGUI()` : void

Clears the screen of all objects