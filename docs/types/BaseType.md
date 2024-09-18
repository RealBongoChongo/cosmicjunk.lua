---
layout: default
title: BaseType
rank: 1
---

# BaseType

The base class for every part

## Properties

## Events

- AttributeChanged : `(AttributeName)`

## Methods

### `GetConfigurations()` : Object

Gathers the configurations for the part

Example from getting a configuration from a light:

```lua
local light = GetPartFromPort(1, "Light")

print(light:GetConfigurations())
>>> { ["Brightness"] = 1; ["Range"] = 16; }
```

***

### `GetConfiguration(Attribute)` : any

Gathers a specific configuration from a part

Example from getting a configuration from a light:

```lua
local light = GetPartFromPort(1, "Light")

print(light:GetConfiguration("Brightness"))
>>> 1

print(light:GetConfiguration("Owner"))
>>> nil
```

***

### `SetConfiguration(Attribute, NewValue)` : void

Sets a configuration for a part

Example:

```lua
local light = GetPartFromPort(1, "Light")

light:SetConfiguration("Range", 60)
```

***

### `ConnectEvent(EventName, Callback)` : RBXConnectionEvent

Connects to an event that a part has

Example:

```lua
local TriggerWire = GetPartFromPort(1, "TriggerWire")

local function OnTrigger()
    print("Detected Trigger")
end

local Event = TriggerWire:ConnectEvent("Triggered", OnTrigger)

Event:Disconnect()
```

***

### `OnceEvent(EventName, Callback)` : RBXConnectionEvent

Connects to an event that a part has and destroys after being fired once

Example:

```lua
local TriggerWire = GetPartFromPort(1, "TriggerWire")

local function OnTrigger()
    print("Detected Trigger Once")
end

local Event = TriggerWire:OnceEvent("Triggered", OnTrigger)
```
