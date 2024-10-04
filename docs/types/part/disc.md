---
layout: default
title: Disc
---

# Disc
### Inherited from [BaseType](https://realbongochongo.github.io/cosmicjunk.lua/docs/types/base/basetype)

A rather powerful class that can write on the Disc compoenent

<blockquote style="border-left: 1px solid #f52;">
    <strong style="color: #0ad;">WARNING</strong><br>
    This component is currently only in the unstable version.
</blockquote><br>

## Overview

| Methods                            |
| ---------------------------------- |
| `Read()` : table                   |
| `Write( table )` : void            |
| `ReadKey( string )` : any          |
| `WriteKey( string, any )` : void   |

<br />
<br />

## Methods

### `Read()` : table

Reads the whole data on the disc

| Returns       | Type   |
| ------------- | ------ |
| Disc Data     | table  |

#### Code Example

```lua
local Disc = GetPartFromPort(1, "Disc")

print(Disc:Read())
>>> { ["TestKey"] = "WOOOOOOOOOOOOOOOOOO" }
```

<br />
<br />

### `Write( table )` : void

Writes the whole data on the disc

| Parameters    | Type   |
| ------------- | ------ |
| Disc Data     | table  |

#### Code Example

```lua
local Disc = GetPartFromPort(1, "Disc")

Disc:Write({["AGuy"] = "gogo_man2341"})

print(Disc:Read())
>>> { ["AGuy"] = "gogo_man2341" }
```

<br />
<br />

### `ReadKey( string )` : any

Reads from a certain key on the disc

| Parameters    | Type    |
| ------------- | ------- |
| Disc Key      | string  |

| Returns       | Type    |
| ------------- | ------- |
| Key Data      | any     |

#### Code Example

```lua
local Disc = GetPartFromPort(1, "Disc")

print(Disc:ReadKey("AGuy"))
>>> "gogo_man2341"
```

<br />
<br />

### `WriteKey( string, any )` : void

Writes to the key on a disc

| Parameters    | Type    |
| ------------- | ------- |
| Disc Key      | string  |
| Disc Data     | any     |

#### Code Example

```lua
local Disc = GetPartFromPort(1, "Disc")

Disc:WriteKey("AGuy", "gogo_man2341")

print(Disc:Read())
>>> { ["AGuy"] = "gogo_man2341" }
```
