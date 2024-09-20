---
layout: default
title: Microcontroller
rank: 1
---

# Microcontroller Class

This class does not require any reference and everything is considered a global variable or function

## Overview

| Functions                                                                                                                          |
| ---------------------------------------------------------------------------------------------------------------------------------- |
| `GetPartFromPort(PortNumber, ObjectName)` : [BaseType](https://realbongochongo.github.io/cosmicjunk.lua/docs/types/base/basetype)  |
| `GetPartsFromPort(PortNumber, ObjectName)` : Array                                                                                 |

## Functions

### `GetPartFromPort(PortNumber, ObjectName)` : [BaseType](https://realbongochongo.github.io/cosmicjunk.lua/docs/types/base/basetype)

Gets a part from a connected port to the microcontroller

| Arguments     | Type   |
| ------------- | ------ |
| PortNumber    | number |
| ObjectName    | string |

| Returns       | Type                                                                                  |
| ------------- | ------------------------------------------------------------------------------------- |
| PartObject    | [BaseType](https://realbongochongo.github.io/cosmicjunk.lua/docs/types/base/basetype) |

### Code Example

```lua
local Light = GetPartFromPort(1, "Light")
```

### `GetPartsFromPort(PortNumber, ObjectName)` : Array

Gets an array of parts from a connected port to the microcontroller

| Arguments     | Type   |
| ------------- | ------ |
| PortNumber    | number |
| ObjectName    | string |

| Returns       | Type  |
| ------------- | ----- |
| PartObjects   | Array |

### Code Example

```lua
local PowerCells = GetPartsFromPort(1, "PowerCell")

print(#PowerCells)
>>> 11
```