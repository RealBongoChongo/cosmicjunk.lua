---
layout: default
title: Dispensable
rank: 4
---

# Dispensable
### Inherited from [BaseType](https://realbongochongo.github.io/cosmicjunk.lua/docs/types/base/basetype)

The base class for Dispensers and Faucets

## Overview

| Events                |
| --------------------- |
| `Dispensed` : void    |

| Methods               |
| --------------------- |
| `Dispense()` : void   |

<br />
<br />

## Events

### `Dispensed` : void

Fires when the part has dispensed something

#### Code Example

```lua
local Dispenser = GetPartFromPort(1, "Dispenser")

Dispenser:ConnectEvent("Dispensed", function()
  print("Dispensed")
end)
```

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
