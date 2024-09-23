---
layout: default
title: Dispensable
rank: 4
---

# PowerStorage
### Inherited from [BaseType](https://realbongochongo.github.io/cosmicjunk.lua/docs/types/base/basetype)

The base class for Dispensers and Faucets

## Overview

| Methods               |
| --------------------- |
| `Dispense()` : void   |

<br />
<br />

## Methods

### `Dispense()` : void

Dispenses an object from the part with no cooldown (Abides by microcontroller throttling)

#### Code Example

```lua
local Dispenser = GetPartFromPort(1, "Dispenser")

Dispenser:Dispense()
```
