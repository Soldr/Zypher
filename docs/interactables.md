# Interactables

```
Button, Toggle, Slider, Textlabel, Textbox, Dropdown, Keybind, Colorpicker
```

## Creating Interactables

All interactables use the same function to make them.

```lua
Section:Create(
	"Button", -- Interactable type
	"Button", -- The name of the interactable
	function(v) -- Put v in if the interactable type returns a value
		-- Callback
	end,
	{
		-- Options
	}
)
```

### Button

A simple button

```lua
Section:Create(
	"Button",
	"Button", -- The name of the button
	function()
		-- Callback
		print('Button pressed!')
	end,
	{
		-- Optional
		animated = true -- Default: false
	}
)
```

### Toggle

A on/off switch

```lua
Section:Create(
	"Toggle",
	"Toggle", -- The name of the toggle
	function(v)
		-- Callback
		print(v) -- State of the toggle
	end,
	{
		-- Required
		default = true -- Default state
	}
)
```

### Slider

A slippery value selector

```lua
Section:Create(
	"Slider",
	"Slider", -- The name of the slider
	function(v)
		-- Callback
		print(v) -- Value of the slider
	end,
	{
		-- Required
		min = 0, -- Smallest value on the slider
		max = 128, -- Largest value on the slider
		
		-- Optional
		default = 2,
		precise = true, -- Whether to do decimal values
		changeablevalue = false -- Should the slider be changeable
	}
)
```

### Textbox

A text input

```lua
Section:Create(
	"Textbox",
	"Textbox", -- The name of the textbox
	function(v)
		-- Callback
		print(v) -- Text in the textbox
	end,
	{
		-- Optional
		text = "This is optional"
	}
)
```

### Keybind

Bind a function to a key. A list of keycodes can be found [here](https://developer.roblox.com/en-us/api-reference/enum/KeyCode)

```lua
Section:Create(
	"Keybind",
	"Keybind", -- The name of the keybind
	function()
		-- Callback
		print('Key pressed!')
	end,
	{
		-- Required
		min = 0, -- Smallest value on the slider
		max = 128, -- Largest value on the slider
		
		-- Optional
		default = Enum.KeyCode.X
	}
)
```

### Dropdown

For listing things that can be chosen from, or just listing things

```lua
Section:Create(
	"Dropdown",
	"Dropdown", -- The name of the dropdown
	function(v)
		-- Callback
		print(v) -- Option selected
	end,
	{
		-- Required
		options = {
			"Apples",
			"Bananas",
			"Pears"
		},

		-- Optional
		default = "Apples"
		search = true -- Allows for searching through the dropdown, useful for large arrays of values
	}
)
```

### Color Picker

Pick a color!

```lua
Section:Create(
	"Colorpicker",
	"Color picker", -- The name of the color picker
	function(color)
		-- Callback
		print(color) -- Color3 Value
	end,
	{
		-- Optional
		default = Color3.fromRGB(255, 255, 255)
	}
)
```

### Textlabel

Well, a label

```lua
Section:Create(
	"Textlabel",
	"Textlabel" -- The text for the label
)
```