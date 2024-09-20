---
layout: default
title: PowerStorage
rank: 2
---

# PowerStorage
### Inherited from [BaseType](https://realbongochongo.github.io/cosmicjunk.lua/docs/types/base/basetype)

The base class for PowerCells and Batteries

## Overview

| Methods               |
| --------------------- |
| `GetPower()` : Object |





## Methods

### `GetPower()` : Object

Gathers the power stats from the part

| Returns       | Type   |
| ------------- | ------ |
| PowerValues   | Object |

#### Code Example

```lua
local powercell = GetPartFromPort(1, "PowerCell")

print(powercell:GetPower())
>>> { ["Power"] = 1; ["MaxPower"] = 50000; }
```