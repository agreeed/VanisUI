# Compatible VanisUI
A Fork of Vanis UI Library that is more compatible!

## Example

```lua
local Library = loadstring(game:HttpGet('https://raw.githubusercontent.com/DarkNetworks/VanisUI/main/Source.lua'))()

local Window = Library:CreateWindow("Name", "Version", 10044538000)

local Tab = Window:CreateTab("Scripts")
local Page = Tab:CreateFrame("Page 1")

local Button = Page:CreateButton("Button", "Description", function()
   CreateNotification("Title", "Description", function(value)
      if value == true then
         print(true)
      else
         print(false)
      end
   end)
end)

local Toggle = Page:CreateToggle("Toggle", "Description", function(arg)
   Toggle:UpdateToggle("New Title", "New Description")
   print(arg)
end)

local Bind = Page:CreateBind("KeyBind", "F", function(arg)
   Bind:UpdateBind("New Title")
   print(arg)
end)

local TextBox = Page:CreateBox("TextBox", 10044538000, function(arg)
   TextBox:UpdateBox("New Title")
   print(arg)
end)

local Slider = Page:CreateSlider("Slider", 16, 500,function(arg)
   print(arg)
end)
```
