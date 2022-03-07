# SLF UI Library

Thank you for using SALFIN's UI library, there is how to use it.

## Loader

```lua
local Library = loadstring(game:HttpGetAsync('https://raw.githubusercontent.com/MirroxGame/SLFLibrary/main/library.lua'))()
```

## Functions

### Creating Window
____
```lua
local Main = Library:Window("TITLE","KeyBind")
```

### Adding Tab
____
```lua
local Tab = Main:Folder("TabName")
```

### Adding Button
____
```lua
local Button = Tab:Button("ButtonText",function()
  print("Clicked")
end)
```

### Adding Toggles
____
```lua
local Toggle = Tab:Toggle("ToggleText",function(state)
  if state then
    print("Toggle On")
  else
    print("Toggle Off")
  end
end,false) -- false is state by default. This means toggle will be on or off when u execute the gui.
```

### Adding Slider
____
```lua
local Slider = Tab:Slider("SliderText",0,100,"SliderSuffix",function(value)  -- 0 (MinValue) | 100 (MaxValue)
  print(value)
end)
```

### Adding Dropdown

```lua
local Dropdown = Tab:Dropdown("DropdownText",{"TableWithValues"},150,function(Choosen) -- 150 (Y Size of the dropdown)
  print(Choosen) -- TableWithValues
end)
### Adding TextBox
____
```lua
local TextBox = Tab:Box("TextBoxText",function(text)
  print(text)
end)
```
