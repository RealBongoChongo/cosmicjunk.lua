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
-- Fetching the objects on the first port
local Screen = GetPartFromPort(1, "Screen")
local PowerSensor = GetPartFromPort(1, "PowerSensor")
local LastPower = PowerSensor:GetReading()

-- Clear GUI objects to not hit GUI object
-- limit when the microcontroller restarts
Screen:ClearGUI()

-- Creating our text
local Power = Screen:CreateGUI("TextLabel", {
  Size = UDim2.new(1,0,0.5,0),
  Position = UDim2.new(0,0,0,0),
  Text = string.format("Power: %s", PowerSensor:GetReading()),
  TextScaled = true,
  BorderSizePixel = 0,
})

local PowerChange = Screen:CreateGUI("TextLabel", {
  Size = UDim2.new(1,0,0.5,0),
  Position = UDim2.new(0,0,0.5,0),
  Text = "Power Change: 0",
  TextScaled = true,
  BorderSizePixel = 0,
})

-- Regularly update power values each second
while true do
  task.wait(1)
  -- Getting the power
  local NowPower = PowerSensor:GetReading()

  -- Change text
  Power:ChangeProperties({
    Text = string.format("Power: %s", NowPower)
  })
  PowerChange:ChangeProperties({
    Text = string.format("Power Change: %s", NowPower - LastPower)
  })

  -- Set the power now to the last power
  LastPower = NowPower
end
```
