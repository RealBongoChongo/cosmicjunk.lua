---
layout: default
title: Reactor
rank: 4
---

# Reactor
### Inherited from [Triggerable](https://realbongochongo.github.io/cosmicjunk.lua/docs/types/base/triggerable)

The class for reactors- can be very useful for automating them

## Overview

| Methods               |
| --------------------- |
| `GetHeat()` : number  |
| `GetLevels()` : Array |

<br />
<br />

## Methods

### `GetHeat()` : number

Gets the heat that the reactor is producing

| Returns   | Type   |
| --------- | ------ |
| Temp      | number |

#### Code Example

```lua
local Reactor = GetPartFromPort(1, "Reactor")

print(Reactor:GetHeat())
>>> 3245
```

<br />
<br />

### `GetLevels()` : Array

Gets the heat that the reactor is producing

| Returns   | Type   |
| --------- | ------ |
| Uraniums  | Array  |

#### Code Example

```lua
local Reactor = GetPartFromPort(1, "Reactor")

print(Reactor:GetLevels())
>>> { [1] = 40.25; [2] = 40.5; [3] = 0; [4] = 0; [5] = 0; }
```
