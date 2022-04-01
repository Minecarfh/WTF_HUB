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

local function SXBEIN_fake_script() -- Frame.LocalScript 
	local script = Instance.new('LocalScript', Frame)

	print("Hello world!")
	
end
coroutine.wrap(SXBEIN_fake_script)()
local function TZUND_fake_script() -- Frame.LocalScript 
	local script = Instance.new('LocalScript', Frame)

	frame = script.Parent.Parent.Frame
	frame.Draggable = true
	frame.Selectable = true
	frame.Active = true
end
coroutine.wrap(TZUND_fake_script)()
local function VZJRT_fake_script() -- TextLabel_2.LocalScript 
	local script = Instance.new('LocalScript', TextLabel_2)

	while wait() do
		script.Parent.Text = game:GetService("Players").LocalPlayer.Data.Gold.Value 
	end
end
coroutine.wrap(VZJRT_fake_script)()
