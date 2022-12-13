local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Player = game.Players.LocalPlayer
local Window = OrionLib:MakeWindow({Name = "Key system", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})

OrionLib:MakeNotification({
	Name = "Logged in!",
	Content = "You are logged in as "..Player.Name..".",
	Image = "rbxassetid://4483345998",
	Time = 5
})

_G.Key = "LXUCPynI21"
_G.KeyInput = "string"

function MakeScriptHub()
     loadstring(game:HttpGet('https://raw.githubusercontent.com/dupescriptforpopit/d/main/README.md'))()
end

function CorrectKeyNotification()
OrionLib:MakeNotification({
	Name = "Correct Key!",
	Content = "You have entered the correct key!",
	Image = "rbxassetid://4483345998",
	Time = 5
})
end

function IncorrectKeyNotification()
OrionLib:MakeNotification({
	Name = "Incorrect Key!",
	Content = "You have entered the incorrect key!",
	Image = "rbxassetid://4483345998",
	Time = 5
})
end

local Tab = Window:MakeTab({
	Name = "Key",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddTextbox({
	Name = "Enter Key",
	Default = "",
	TextDisappear = true,
	Callback = function(Value)
		_G.KeyInput = Value
	end	  
})

Tab:AddButton({
	Name = "Check Key!",
	Callback = function()
      		if _G.KeyInput == _G.Key then
      		MakeScriptHub()
            CorrectKeyNotification()
            else
                IncorrectKeyNotification()
      		end
  	end    
})

Tab:AddButton({
	Name = "Copy Key Link",
	Callback = function()
      		setclipboard("https://link-center.net/536069/etiam-ultricies-nisi")
OrionLib:MakeNotification({
	Name = "Key",
	Content = "Link copyed in clipboard",
	Image = "rbxassetid://4483345998",
	Time = 5
})

  	end    
})

