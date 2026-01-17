# Vero

local vero_UI = loadstring(game:HttpGet("https://raw.githubusercontent.com/enzoastra30-debug/Debug/refs/heads/main/Vero_UI"))

local UI = vero_UI.window({
    Title = "My UI",
    Width = 320,
    MaxPanelHeight = 240,
    Tabs = {
        "Menu",
        "Player",
        "Games"
    }
})
