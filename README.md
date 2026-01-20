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
tab1:dropdown("Dropdown Test", {"error","success","info", "warning"},_, function(value)
    print((value))
    if value == "error" then
        UI:notify(value, "error", 2)
    end
    if value == "success" then
        UI:notify(value, "success", 2)
    end
    if value == "info" then
        UI:notify(value, "info", 2)
    end
    if value == "warning" then
        UI:notify(value, "warning", 2)
    end
end)

--//Gamebox Test
local gameBoxTest = tab2:gamebox("14875978126", "Total Roblox Drama")
local testFrame = Instance.new("TextButton")
testFrame.Size = UDim2.new(1, 0, 0, 30)
testFrame.Text = "Total Drama"
testFrame.Parent = gameBoxTest
testFrame.MouseButton1Click:Connect(function()
    UI:confirm("Confirmation Test", "This is obviously a confirmation test", {
        ShowDecline = true,
        confirm = function() UI:notify("Confirmed", "", 2) end,
        decline = function() UI:notify("Declined", "", 2) end,
    })
end)

--//Sectionbox Test
local section = tab3:section("test", 90)
local testFrame = Instance.new("TextButton")
testFrame.Size = UDim2.new(1, 0, 0, 30)
testFrame.Text = "Speed Boost"
testFrame.Parent = section.Content
testFrame.MouseButton1Click:Connect(function()
    UI:confirm("Confirmation Test", "This is obviously a confirmation test", {
        ShowDecline = true,
        confirm = function() UI:notify("Confirmed", "", 2) end,
        decline = function() UI:notify("Declined", "", 2) end,
    })
end)


--//Searchbar test
tab2:search("Find feature...")
````
