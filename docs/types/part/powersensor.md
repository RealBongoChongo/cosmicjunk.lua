---
layout: default
title: PowerSensor
rank: 1
---

# PowerSensor
### Inherited from [BaseType](https://realbongochongo.github.io/cosmicjunk.lua/docs/types/base/basetype)

***

The base class for all power sensors

## Overview

| Methods                 |
| ----------------------- |
| `GetReading()` : number |

<br />
<br />

## Methods

### `GetReading()` : number

Gets the power reading from the power sensor

| Returns       | Type   |
| ------------- | ------ |
| PowerOutput   | number |

#### Code Example

```lua
local powerSensor = GetPartFromPort(1, "PowerSensor")

print(powerSensor:GetReading())
>>> 449.10000000000000003
```