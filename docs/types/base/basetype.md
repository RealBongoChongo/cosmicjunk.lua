---
layout: default
title: BaseType
rank: 1
---

# BaseType

The base class for every part

## Overview

| Events                                                |
| :---------------------------------------------------- |
|`AttributeChanged` : string                            |

| Methods                                                 |
| :------------------------------------------------------ |
|`GetConfigurations()` : Object                           |
|`GetConfiguration(Attribute)` : any                      |
|`SetConfiguration(Attribute, Value)` : void              |
|`ConnectEvent(EventName, Callback)` : RBXConnectionEvent |
|`OnceEvent(EventName, Callback)` : RBXConnectionEvent    |





## Events

### `AttributeChanged` : string

Fires whenever an attribute was changed on the object

<blockquote style="border-left: 1px solid #f52;">
    <strong style="color: #0ad;">WARNING</strong><br>
    <strong>This fires on all attributes, meaning that it will not matter if it is not a configuration attribute</strong>
</blockquote><br>

|**Arguments**  | Type   |
| :------------ | ------ |
| Attribute     | string |





## Methods

### `GetConfigurations()` : Object

Gathers the configurations for the part

|**Returns**    | Type   |
| :------------ | ------ |
| Attributes    | Object |

#### Code Example

```lua
local light = GetPartFromPort(1, "Light")

print(light:GetConfigurations())
>>> { ["Brightness"] = 1; ["Range"] = 16; }
```





### `GetConfiguration(Attribute)` : any

Gathers a specific configuration from a part

|**Parameters** | Type   |
| :------------ | ------ |
| Attribute     | string |

|**Returns**    | Type   |
| :------------ | ------ |
| Attributes    | any    |

#### Code Example

```lua
local light = GetPartFromPort(1, "Light")

print(light:GetConfiguration("Brightness"))
>>> 1

print(light:GetConfiguration("Owner"))
>>> nil
```





### `SetConfiguration(Attribute, NewValue)` : void

Sets a configuration for a part

|**Parameters** | Type   |
| :------------ | ------ |
| Attribute     | string |
| NewValue      | any    |

#### Code Example

```lua
local light = GetPartFromPort(1, "Light")

light:SetConfiguration("Range", 60)
```






### `ConnectEvent(EventName, Callback)` : RBXConnectionEvent

Connects to an event that a part has

*Similar behavior to `Event:Connect()` in luau*

|**Parameters** | Type     |
| :------------ | -------- |
| EventName     | string   |
| Callback      | function |

#### Code Example

```lua
local TriggerWire = GetPartFromPort(1, "TriggerWire")

local function OnTrigger()
    print("Detected Trigger")
end

local Event = TriggerWire:ConnectEvent("Triggered", OnTrigger)

Event:Disconnect()
```





### `OnceEvent(EventName, Callback)` : RBXConnectionEvent

Connects to an event that a part has and destroys after being fired once

*Similar behavior to `Event:Once()` in luau*


|**Parameters** | Type     |
| :------------ | -------- |
| EventName     | string   |
| Callback      | function |

#### Code Example

```lua
local TriggerWire = GetPartFromPort(1, "TriggerWire")

local function OnTrigger()
    print("Detected Trigger Once")
end

local Event = TriggerWire:OnceEvent("Triggered", OnTrigger)
```
