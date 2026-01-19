# Vero

````
local Vero_UI = loadstring(game:HttpGet("https://raw.githubusercontent.com/enzoastra30-debug/Debug/refs/heads/main/Vero_UI"))()

local UI = Vero_UI.window({
    Title = "My UI",
})

local tab1 = UI:tab("tab1")
local tab2 = UI:tab("tab2")
local tab3 = UI:tab("tab3")

--//Checkbox test
tab1:checkbox("Enable feature", false, function(state)
    print("Checkbox is now:", state)
end)

--//Button Test
tab1:button("test Button", function()
    print(("Button Pressed"))
end)

--//Keybind Test
tab1:keybind("Test Keybind", "Q", function()
    print(("keybind pressed"))
end)

--//Slider Test
tab1:slider("slider test", 0, 10, 0, function(value)
    print((value))
end)

--//Dropdown Test
tab1:dropdown("Dropdown Test", {"test1","test2","test3"},_, function(value)
    print((value))
end)

--//Gamebox Test
tab1:gamebox("14875978126", "Total Roblox Drama", function()
    print(("Load Game"))
end)
````
