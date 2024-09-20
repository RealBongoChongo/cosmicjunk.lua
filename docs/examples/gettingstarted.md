---
layout: default
title: Getting Started
rank: 1
---

# Getting Started

Here is some sample code that creates a display that regularly updates some text to show the total power received by the PowerSensor

Classes Used:
- [Microcontroller](https://realbongochongo.github.io/cosmicjunk.lua/docs/basic/microcontroller)
- [Screen](https://realbongochongo.github.io/cosmicjunk.lua/docs/types/part/screen)
- [PowerSensor](https://realbongochongo.github.io/cosmicjunk.lua/docs/types/part/screen)

```lua
local Screen = GetPartFromPort(1, "Screen")
local PowerSensor = GetPartFromPort(1, "PowerSensor")
local LastPower = PowerSensor:GetReading()

Screen:ClearGUI()

local Power = Screen:CreateGUI("TextLabel", {
  Size = UDim2.new(1,0,0.5,0),
  Position = UDim2.new(0,0,0,0),
  Text = `Power: {PowerSensor:GetReading()}`,
})

local PowerChange = Screen:CreateGUI("TextLabel", {
  Size = UDim2.new(1,0,0.5,0),
  Position = UDim2.new(0,0,0.5,0),
  Text = `Power: {PowerSensor:GetReading()}`,
})

while true do
  task.wait(1)
  local NowPower = PowerSensor:GetReading()

  Power:ChangeProperties({Text = `Power: {NowPower}`})
  PowerChange:ChangeProperties({Text = `Power Change: {NowPower - LastPower}`})

  LastPower = NowPower
end
```
