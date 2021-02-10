# Zypher UI Library Documentation

## Authors

- xTheAlex14

## Source Code

If you want the source code, it is [here.](https://zypher.wtf/UI-Lib)

## Basic Usage

```lua
local library = loadstring(game:HttpGet("https://zypher.wtf/UI-Lib"))()
```

## Create The GUI Window

```lua
local Main = library:CreateMain({
	-- Required
    projName = "UILib", -- The name for the UI in game.CoreGui, not the GUI itself.
    -- Optional
    Resizable = true, -- Requires MinSize and MaxSize
    MinSize = UDim2.new(0, 400, 0, 400),
    MaxSize = UDim2.new(0, 750, 0, 500)
})
```

## Categories and Sections

```lua
-- A category is a tab
local Category = Main:CreateCategory("Category")

-- Self explanatory
local Section = Category:CreateSection("Section")
```