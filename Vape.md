# Vape Library Documentation (unofficial)

### Getting Loadstring
```lua
local lib = loadstring(game:HttpGet"https://raw.githubusercontent.com/dawid-scripts/UI-Libs/main/Vape.txt")()
```

### Creating a Window
```lua
local win = lib:Window("PREVIEW",Color3.fromRGB(44, 120, 224), Enum.KeyCode.RightControl)
```

### Creating a Tab
```lua
local tab = win:Tab("Tab 1")
```
### Creating a Button
```lua
tab:Button("Button", function()
lib:Notification("Notification", "Hello!", "Hi!")
end)
```

### Creating a Toggle
```lua
tab:Toggle("Toggle",false, function(Value)
print(Value)
end)
```

### Creating a Slider
```lua
tab:Slider("Slider",0,100,30, function(Value)
print(Value)
end)
```

### Creating a Dropdown
```lua
tab:Dropdown("Dropdown",{"Option 1","Option 2","Option 3"}, function(Value)
print(Value)
end)
```

### Creating a Colorpicker
```lua
tab:Colorpicker("Colorpicker",Color3.fromRGB(255,0,0), function(Value)
print(Value)
end)
```

### Creating a Textbox
```lua
tab:Textbox("Textbox",true, function(Value)
print(Value)
end)
```

### Creating a Bind
```lua
tab:Bind("Bind",Enum.KeyCode.RightShift, function()
print("Pressed!")
end)
```

### Creating a Label
```lua
tab:Label("Label")
```

### Change UI Color
```lua
local changeclr = win:Tab("Change UI Color")

changeclr:Colorpicker("Change UI Color",Color3.fromRGB(44, 120, 224), function(t)
lib:ChangePresetColor(Color3.fromRGB(t.R * 255, t.G * 255, t.B * 255))
end)
```
