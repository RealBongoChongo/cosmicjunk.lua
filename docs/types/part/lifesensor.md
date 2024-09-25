---
layout: default
---

# LifeSensor
### Inherited from [BaseType](https://realbongochongo.github.io/cosmicjunk.lua/docs/types/base/basetype)

The class that encompasses the lifesensor component

## Overview

| Methods                            |
| ---------------------------------- |
| `GetPlayers( Relative )` : Array   |

<br />
<br />

## Methods

### `GetPlayers( Relative )` : Array

Dispenses an object from the part with no cooldown (Abides by microcontroller throttling)

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
