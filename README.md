--WTF_HUB

-- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local TextLabel = Instance.new("TextLabel")
local UICorner_2 = Instance.new("UICorner")
local TextLabel_2 = Instance.new("TextLabel")

--Properties:

ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(148, 148, 148)
Frame.BackgroundTransparency = 1.000
Frame.Position = UDim2.new(0.330715537, 0, 0.197879851, 0)
Frame.Size = UDim2.new(0, 368, 0, 58)

UICorner.Parent = Frame

TextLabel.Parent = Frame
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.Position = UDim2.new(-0.000235654414, 0, -0.763218403, 0)
TextLabel.Size = UDim2.new(0, 305, 0, 44)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = "GOlD : "
TextLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.TextSize = 39.000

UICorner_2.Parent = TextLabel

TextLabel_2.Parent = Frame
TextLabel_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.BackgroundTransparency = 1.000
TextLabel_2.Position = UDim2.new(0.412019819, 0, -0.779884934, 0)
TextLabel_2.Size = UDim2.new(0, 198, 0, 44)
TextLabel_2.Font = Enum.Font.SourceSans
TextLabel_2.Text = "Value"
TextLabel_2.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel_2.TextSize = 39.000

-- Scripts:

local function NIEMA_fake_script() -- Frame.LocalScript 
	local script = Instance.new('LocalScript', Frame)

	print("Hello world!")
	
end
coroutine.wrap(NIEMA_fake_script)()
local function EZLTF_fake_script() -- Frame.LocalScript 
	local script = Instance.new('LocalScript', Frame)

	frame = script.Parent.Parent.Frame
	frame.Draggable = true
	frame.Selectable = true
	frame.Active = true
end
coroutine.wrap(EZLTF_fake_script)()
local function HOKHKM_fake_script() -- TextLabel_2.LocalScript 
	local script = Instance.new('LocalScript', TextLabel_2)

	while wait() do
		script.Parent.Text = game:GetService("Players").LocalPlayer.Data.Gold.Value 
	end
end
coroutine.wrap(HOKHKM_fake_script)()
local function UBWAS_fake_script() -- ScreenGui.LocalScript 
	local script = Instance.new('LocalScript', ScreenGui)

	while wait() do
		if _G.Gold_Value then
			script.Parent.Frame.Visible = true
		else
			script.Parent.Frame.Visible = false
		end
	end
end
coroutine.wrap(UBWAS_fake_script)()
local function GZYXOPJ_fake_script() -- ScreenGui.LocalScript 
	local script = Instance.new('LocalScript', ScreenGui)

	local Config = {
		WindowName = "WTF HUB Premium Scripts",
		Color = Color3.fromRGB(255,128,64),
		Keybind = Enum.KeyCode.RightControl
	}
	
	local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/AlexR32/Roblox/main/BracketV3.lua"))()
	local Window = Library:CreateWindow(Config, game:GetService("CoreGui"))
	
	local Tab1 = Window:CreateTab("Main")
	local Tab3 = Window:CreateTab("Auto Farm")
	local Tab4 = Window:CreateTab("Team")
	local Tab5 = Window:CreateTab("Save\open")
	local Tab6 = Window:CreateTab("Settings")
	local Tab7 = Window:CreateTab("Shop Chest")
	local Tab8 = Window:CreateTab("SHOP Normal")
	local Tab2 = Window:CreateTab("UI Settings")
	
	
	local Section1 = Tab1:CreateSection("Menu ALL")
	local que = Tab5:CreateSection("Save\\Open")
	local SHC = Tab7:CreateSection("Shop Chest")
	local SS5 = Tab3:CreateSection("Auto Farm")
	local STL = Tab6:CreateSection("settings-All")
	local SHN = Tab8:CreateSection("Shop Normal")
	local AUB = Tab7:CreateSection("Auto Buy Chest")
	local SS6 = Tab4:CreateSection("zone Team")
	local SS6V2 =  Tab4:CreateSection("Tpleport")
	local Section3 = Tab2:CreateSection("Menu")
	local Section4 = Tab2:CreateSection("Background")
	
	local Label1 = Section1:CreateLabel("Label 1")
	Label1:UpdateText("Build A Boat For Treasure ")
	-------------
	local Slider1 = Section1:CreateSlider("JumpPower", 0,560,nil,true, function(Value)
		game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
	end)
	Slider1:AddToolTip("Set JumpPower")
	Slider1:SetValue(50)
	--------------------------
	local Slider1 = Section1:CreateSlider("WalkSpeed", 0,560,nil,true, function(Value)
		game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
	end)
	Slider1:AddToolTip("Set WalkSpeed")
	Slider1:SetValue(25)
	-------------
	local Slider1 = Section1:CreateSlider("Gravity", 0,196,nil,true, function(Value)
		workspace.Gravity = Value
	end)
	Slider1:AddToolTip("Set Gravity")
	Slider1:SetValue(196)
	-------------
	local Dropdown2 = Section1:CreateDropdown("Characterl", {"FoxCharacter","PenguinCharacter","ChickenCharacter","human",}, function(Mod)
		local args = {
			[1] = Mod
		}
	
		workspace.ChangeCharacter:FireServer(unpack(args))
		if Mod == "human" then
			game.Players.LocalPlayer.Character.Humanoid.Health = "0"
		end
	end)
	Dropdown2:AddToolTip("Characterl MOD in Game")
	Dropdown2:SetOption("human")
	-----------------------------------
	local Toggle1 = Section1:CreateToggle("infjump", nil, function(State)
		if State  then
			_G.infinjump = true
	
			local Player = game:GetService("Players").LocalPlayer
			local Mouse = Player:GetMouse()
			Mouse.KeyDown:connect(function(k)
				if _G.infinjump then
					if k:byte() == 32 then
						Humanoid = game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
						Humanoid:ChangeState("Jumping")
						wait(0.1)
						Humanoid:ChangeState("Seated")
					end
				end
			end)
	
			local Player = game:GetService("Players").LocalPlayer
			local Mouse = Player:GetMouse()
			Mouse.KeyDown:connect(function(k)
				k = k:lower()
				if k == "f" then
					if _G.infinjump == true then
						_G.infinjump = false
					else
						_G.infinjump = true
					end
				end
			end)
		else
			_G.infinjump = false
		end
	end)
	local Toggle = Section1:CreateToggle("Anchored", nil, function(State)
		if State  then
			game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true
		else
			game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = false
		end
	end)
	local Button2 = Section1:CreateButton("Unlock FPS", function()
		loadstring(game:HttpGet("https://pastebin.com/raw/ywFjby1i"))()
	end)
	Button2:AddToolTip("lol FPS")
	
	-------------
	local Button3 = Section1:CreateButton("RTX ON", function()
		loadstring(game:HttpGet("https://pastebin.com/raw/HYcR0Jaq"))()
	end)
	Button3:AddToolTip("WOW RTX ON")
	local Button3 = Section1:CreateButton("RemoveWater", function()
		local credit='guardscripts'
		local url=('https://raw.githubusercontent.com/%s/myscripts/main/scriptinit.lua'):format(credit)
		init=loadstring(game:HttpGet(url,true))
		getgenv().xscriptId='MzMyODJy'
		init()
	end)
	Button3:AddToolTip("WOW RTX ON")
	-----------------------------------
	local Toggle1 = SS5:CreateToggle("Auto Farm", _G.AutoFarm, function(State)
		_G.AutoFarm = State
		if State  then
			loadstring(game:HttpGet("https://pastebin.com/raw/9DJ63vr2"))()
		else
			local G = false
		end
	end)
	--------------------------------------------
	local Toggle1 = SS5:CreateToggle("Auto Farm", _G.Gold_Value, function(State)
	_G.Gold_Value = State
	end)
	--------------------------------------------------------------
	local Button4 = SS5:CreateButton("Kill Roblox", function()
		while wait() do
			for i,v in pairs(game.Players:GetPlayers()) do
				v:Kick("Kill Roblox")
			end
		end
	end)
	Button4:AddToolTip("Kick Me")
	----------------------------------------
	
	local Button5 = SS6:CreateButton("Team Yellow", function()
	
		local args = {
			[1] = game:GetService("Teams").yellow
		}
		workspace.ChangeTeam:FireServer(unpack(args))
	end)
	Button5:AddToolTip("Team yellow")
	-------------------------------
	local Button5 = SS6:CreateButton("Team Red", function()
	
		local args = {
			[1] = game:GetService("Teams").red
		}
		workspace.ChangeTeam:FireServer(unpack(args))
	end)
	Button5:AddToolTip("Team Red")
	-------------------------------
	local Button5 = SS6:CreateButton("Team pink", function()
	
		local args = {
			[1] = game:GetService("Teams").magenta
		}
		workspace.ChangeTeam:FireServer(unpack(args))
	end)
	Button5:AddToolTip("Team pink")
	-------------------------------
	local Button5 = SS6:CreateButton("Team Green", function()
	
		local args = {
			[1] = game:GetService("Teams").green
		}
		workspace.ChangeTeam:FireServer(unpack(args))
	end)
	Button5:AddToolTip("Team Green")
	-------------------------------
	local Button5 = SS6:CreateButton("Team blue", function()
	
		local args = {
			[1] = game:GetService("Teams").blue
		}
		workspace.ChangeTeam:FireServer(unpack(args))
	end)
	Button5:AddToolTip("Team blue")
	-------------------------------
	local Button5 = SS6:CreateButton("Team While", function()
	
		local args = {
			[1] = game:GetService("Teams").white
		}
		workspace.ChangeTeam:FireServer(unpack(args))
	end)
	Button5:AddToolTip("Team white")
	----------------------------------
	local Button5 = SS6:CreateButton("Team Black", function()
	
		local args = {
			[1] = game:GetService("Teams").black
		}
		workspace.ChangeTeam:FireServer(unpack(args))
	end)
	Button5:AddToolTip("Team white")
	------------------------------- SS6V2
	local Button5 = SS6V2:CreateButton("Team yellow", function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-480.86981201172, -9.7000036239624, 640.38543701172)
	end)
	Button5:AddToolTip("Tpleport yellow")
	---------------------------------------
	local Button5 = SS6V2:CreateButton("Team Red", function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(373.34173583984, -9.7000036239624, -64.98299407959)
	end)
	Button5:AddToolTip("Tpleport Red")
	---------------------------------------
	local Button5 = SS6V2:CreateButton("Team pink", function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(372.62808227539, -9.7000036239624, 647.02209472656)
	end)
	Button5:AddToolTip("Tpleport pink")
	---------------------------------------
	local Button5 = SS6V2:CreateButton("Team green", function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-480.51907348633, -9.700005531311, 293.95031738281)
	end)
	Button5:AddToolTip("Tpleport Green")
	---------------------------------------
	local Button5 = SS6V2:CreateButton("Team blue", function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(375.1591796875, -9.7000036239624, 300.55682373047)
	end)
	Button5:AddToolTip("Tpleport blue")
	---------------------------------------
	local Button5 = SS6V2:CreateButton("Team While", function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-50.008567810059, -9.7000036239624, -497.34994506836)
	end)
	Button5:AddToolTip("Tpleport While")
	---------------------------------------
	local Button5 = SS6V2:CreateButton("Team black", function()
		game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-51.260215759277, -360.40417480469, 9503.462890625)
	end)
	Button5:AddToolTip("Tpleport black")
	---------------------------------------
	---------------7777777777777------------
	-------------
	
	
	local Dropdown2 = que:CreateDropdown("Open", {1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,}, function(open)
		local args = {
			[1] = open
		}
	
		workspace.ChangeCharacter:FireServer(unpack(args))
	end)
	
	local Dropdown2 = que:CreateDropdown("Save", {1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,}, function(Save)
		local args = {
			[1] =  Save
		}
	
		workspace.SaveBoatData:InvokeServer(unpack(args))
	end)
	
	local Button5 = que:CreateButton("Buy new save", function()
	
		local args = {
			[1] = "newSlotGold"
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	Button5:AddToolTip("Buy new save")
	
	local Button5 = que:CreateButton("Clear all in land", function()
		workspace.ClearAllPlayersBoatParts:FireServer()
	end)
	Button5:AddToolTip("Clear all in land")
	-------------------------------------
	
	local Toggle1 = STL:CreateToggle("Background-Music", nil, function(State)
		if state then
	
			workspace.MuteMusicRemote:InvokeServer()
	
		else
			workspace.MuteMusicRemote:InvokeServer()
		end
	end)
	
	
	local Toggle1 = STL:CreateToggle("lsolation mode", nil, function(State)
		if state then
			-- Script generated by SimpleSpy - credits to exx#9394
	
			local args = {
				[1] = true
			}
	
			workspace.RefreshLocks:FireServer(unpack(args))
	
		else
			-- Script generated by SimpleSpy - credits to exx#9394
	
			local args = {
				[1] = false
			}
	
			workspace.RefreshLocks:FireServer(unpack(args))
	
		end
	end)
	
	local Toggle1 = STL:CreateToggle("BlockRequests", nil, function(State)
		if state then
			-- Script generated by SimpleSpy - credits to exx#9394
	
			local args = {
				[1] = "BlockRequests",
				[2] = true
			}
	
			workspace.SettingFunction:InvokeServer(unpack(args))
	
	
		else
			-- Script generated by SimpleSpy - credits to exx#9394
	
			local args = {
				[1] = "BlockRequests",
				[2] = false
			}
	
			workspace.SettingFunction:InvokeServer(unpack(args))
		end
	end)
	
	local Toggle1 = STL:CreateToggle("PVP mode", nil, function(State)
		if state then
			-- Script generated by SimpleSpy - credits to exx#9394
	
			local args = {
				[1] = "BlockRequests",
				[2] = true
			}
	
			workspace.SettingFunction:InvokeServer(unpack(args))
		else
			-- Script generated by SimpleSpy - credits to exx#9394
	
			local args = {
				[1] = "BlockRequests",
				[2] = false
			}
	
			workspace.SettingFunction:InvokeServer(unpack(args))
		end
	end)
	
	local Toggle1 = STL:CreateToggle("Share mode", nil, function(State)
		if state then
			game:GetService("Players").LocalPlayer.Settings.PVP.Value = true
		else
			game:GetService("Players").LocalPlayer.Settings.PVP.Value = false
		end
	end)
	
	
	---------------------------------
	local Button5 = SHC:CreateButton("Common", function()
		local args = {
			[1] = "Common Chest",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	
	local Button5 = SHC:CreateButton("UnCommon", function()
		local args = {
			[1] = "Uncommon Chest",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	local Button5 = SHC:CreateButton("Rare", function()
	
		local args = {
			[1] = "Rare Chest",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	local Button5 = SHC:CreateButton("Epic", function()
		local args = {
			[1] = "Epic Chest",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	
	local Button5 = SHC:CreateButton("Legendary", function()
		local args = {
			[1] = "Legendary Chest",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	
	local Toggle1 = AUB:CreateToggle("Auto Buy", _G.AutoBuy, function(State)
		_G.AutoBuy = State
	end)
	
	local Dropdown2 = AUB:CreateDropdown("Auto Buy Chest", {"Common Chest","Uncommon Chest","Rare Chest","Epic Chest","Legendary Chest"}, function(Chest)
		if _G.AutoBuy then
			while wait() do
				local args = {
					[1] = Chest,
					[2] = 1
				}
	
				workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
			end
		end
	end)
	-----------------------------------
	
	local Button5 = SHN:CreateButton("Sign", function()
		local args = {
			[1] = "Sign",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	
	local Button5 = SHN:CreateButton("BoatMotor", function()
		local args = {
			[1] = "BoatMotor",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	
	local Button5 = SHN:CreateButton("Car Parts", function()
		local args = {
			[1] = "Car Parts",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	
	local Button5 = SHN:CreateButton("Parachutes", function()
		local args = {
			[1] = "Locked Doors",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	
	local Button5 = SHN:CreateButton("Magnets", function()
		local args = {
			[1] = "Magnets",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	
	local Button5 = SHN:CreateButton("PVP Pack", function()
		local args = {
			[1] = "PVP Pack",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	
	local Button5 = SHN:CreateButton("LegacyCarPack", function()
		local args = {
			[1] = "LegacyCarPack",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	
	local Button5 = SHN:CreateButton("Switch", function()
		local args = {
			[1] = "Switch",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	
	local Button5 = SHN:CreateButton("lightbulbs", function()
		local args = {
			[1] = "lightbulbs",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	
	local Button5 = SHN:CreateButton("Button", function()
		local args = {
			[1] = "Button",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	
	local Button5 = SHN:CreateButton("camera", function()
		local args = {
			[1] = "camera",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	
	local Button5 = SHN:CreateButton("dome camera", function()
		local args = {
			[1] = "dome camera",
			[2] = 1
		}
	
		workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
	end)
	
	------------------------------------
	local Toggle3 = Section3:CreateToggle("UI Toggle", nil, function(State)
		Window:Toggle(State)
	end)
	Toggle3:CreateKeybind(tostring(Config.Keybind):gsub("Enum.KeyCode.", ""), function(Key)
		Config.Keybind = Enum.KeyCode[Key]
	end)
	Toggle3:SetState(true)
	local Button5 = Section3:CreateButton("Rejoin", function()
		local ts = game:GetService("TeleportService")
	
		local p = game:GetService("Players").LocalPlayer
	ts:Teleport(game.PlaceId, p)
	end)
	
	local Colorpicker3 = Section3:CreateColorpicker("UI Color", function(Color)
		Window:ChangeColor(Color)
	end)
	Colorpicker3:UpdateColor(Config.Color)
	
	-- credits to jan for patterns
	local Dropdown3 = Section4:CreateDropdown("Image", {"Default","Hearts","Abstract","Hexagon","Circles","Lace With Flowers","Floral"}, function(Name)
		if Name == "Default" then
			Window:SetBackground("2151741365")
		elseif Name == "Hearts" then
			Window:SetBackground("6073763717")
		elseif Name == "Abstract" then
			Window:SetBackground("6073743871")
		elseif Name == "Hexagon" then
			Window:SetBackground("6073628839")
		elseif Name == "Circles" then
			Window:SetBackground("6071579801")
		elseif Name == "Lace With Flowers" then
			Window:SetBackground("6071575925")
		elseif Name == "Floral" then
			Window:SetBackground("5553946656")
		end
	end)
	Dropdown3:SetOption("Hexagon")
	
	local Colorpicker4 = Section4:CreateColorpicker("Color", function(Color)
		Window:SetBackgroundColor(Color)
	end)
	Colorpicker4:UpdateColor(Color3.new(1,1,1))
	
	local Slider3 = Section4:CreateSlider("Transparency",0,1,nil,false, function(Value)
		Window:SetBackgroundTransparency(Value)
	end)
	Slider3:SetValue(0.88)
	
	local Slider4 = Section4:CreateSlider("Tile Scale",0,1,nil,false, function(Value)
		Window:SetTileScale(Value)
	end)
	Slider4:SetValue(0.61)
	
	
	spawn(function ()
		while wait() do
			if _G.AutoFarm then
				local G = false
			end
		end
	end)
end
coroutine.wrap(GZYXOPJ_fake_script)()
