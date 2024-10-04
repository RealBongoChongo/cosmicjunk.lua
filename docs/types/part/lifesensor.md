---
layout: default
title: LifeSensor
---

# LifeSensor
### Inherited from [BaseType](https://realbongochongo.github.io/cosmicjunk.lua/docs/types/base/basetype)

The class that encompasses the lifesensor component

<blockquote style="border-left: 1px solid #f52;">
    <strong style="color: #0ad;">WARNING</strong><br>
    This component is currently only in the unstable version.
</blockquote><br>

## Overview

| Methods                            |
| ---------------------------------- |
| `GetPlayers( Relative )` : Array   |

<br />
<br />

## Methods

### `GetPlayers( Relative )` : Array

Gets all players in the world

The relative parameter refers to the position and rotation that is relative to the life sensor

| Parameters    | Type     |
| ------------- | -------- |
| Relative      | boolean  |

| Returns       | Type   |
| ------------- | ------ |
| Players       | Array  |

#### Code Example

```lua
local LifeSensor = GetPartFromPort(1, "LifeSensor")

print(LifeSensor:GetPlayers())
>>> { [1] = {Name = "gogo_man2341", DisplayName = "Bungo", UserId = 1328749, Position = 0, 100, 0, CFrame = <insert cframe>} }
```
