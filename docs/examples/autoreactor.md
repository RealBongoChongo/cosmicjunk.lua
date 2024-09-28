---
layout: default
title: Auto Reactor
rank: 1
---

# Auto Reactor

This is some very light code in order to create an automatic self-sustaining reactor

Classes Used:
- [Microcontroller](https://realbongochongo.github.io/cosmicjunk.lua/docs/basic/microcontroller)
- [Reactor](https://realbongochongo.github.io/cosmicjunk.lua/docs/types/part/reactor)
- [Dispensable](https://realbongochongo.github.io/cosmicjunk.lua/docs/types/part/dispensable)

```lua
-- Fetching the objects on the first port
local Reactor = GetPartFromPort(1, "Reactor")
local Dispenser = GetPartFromPort(1, "Dispenser")

-- Regularly checking the 
while true do
    task.wait(1)
    local Heat = Reactor:GetHeat()

    -- Keeping it within optimal ranges
    if Heat <= 3250 then
        Reactor:Trigger("Activate")
    elseif Heat >= 3650 then
        Reactor:Trigger("Deactivate")
    end

    -- Keeping reactor levels good
    for _, Level in Reactor:GetLevels() do
        if Level <= 25 then
            Dispenser:Dispense()
        end
    end
end
```
