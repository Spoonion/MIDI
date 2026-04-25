# GIF

```lua
local PortFrame = script.Parent:WaitForChild("PortFrame")

local img = PortFrame:FindFirstChildOfClass("ImageLabel")

local frames = {
    "https://github.com/Spoonion/MIDI/raw/main/pixel.jpeg",
    "https://github.com/Spoonion/MIDI/raw/main/pixel.jpeg",
    "https://github.com/Spoonion/MIDI/raw/main/pixel.jpeg"
}

local i = 1

while true do
    if img then
        img.Image = frames[i]
        img.Rotation = img.Rotation + 2
    end

    i = i + 1
    if i > #frames then
        i = 1
    end

    task.wait(0.05)
end
```
