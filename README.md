
local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local UIAspectRatioConstraint = Instance.new("UIAspectRatioConstraint")
local UICorner = Instance.new("UICorner")
local TextBox = Instance.new("TextBox")
local UICorner_2 = Instance.new("UICorner")
local TC = Instance.new("TextButton")
local UICorner_3 = Instance.new("UICorner")
local TB = Instance.new("TextButton")
local UICorner_4 = Instance.new("UICorner")
local TextButton = Instance.new("TextButton")
local UICorner_5 = Instance.new("UICorner")
local UIAspectRatioConstraint_2 = Instance.new("UIAspectRatioConstraint")

--Properties:

ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Frame.Parent = ScreenGui
Frame.AnchorPoint = Vector2.new(0.5, 0.5)
Frame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Frame.BackgroundTransparency = 0.500
Frame.BorderColor3 = Color3.fromRGB(0, 0, 0)
Frame.BorderSizePixel = 0
Frame.Position = UDim2.new(0.5, 0, 0.5, 0)
Frame.Size = UDim2.new(0.319999993, 0, 0.447093904, 0)
Frame.Visible = false

UIAspectRatioConstraint.Parent = Frame
UIAspectRatioConstraint.AspectRatio = 1.333

UICorner.CornerRadius = UDim.new(0.0250000004, 0)
UICorner.Parent = Frame

TextBox.Parent = Frame
TextBox.AnchorPoint = Vector2.new(0.5, 0.5)
TextBox.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
TextBox.BackgroundTransparency = 0.750
TextBox.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextBox.BorderSizePixel = 0
TextBox.Position = UDim2.new(0.5, 0, 0.200000003, 0)
TextBox.Size = UDim2.new(0.699999988, 0, 0.150000006, 0)
TextBox.Font = Enum.Font.SourceSans
TextBox.Text = "100"
TextBox.TextColor3 = Color3.fromRGB(255, 255, 255)
TextBox.TextScaled = true
TextBox.TextSize = 14.000
TextBox.TextWrapped = true

UICorner_2.CornerRadius = UDim.new(1, 0)
UICorner_2.Parent = TextBox

TC.Name = "TC"
TC.Parent = Frame
TC.AnchorPoint = Vector2.new(0.5, 0.5)
TC.BackgroundColor3 = Color3.fromRGB(85, 255, 0)
TC.BorderColor3 = Color3.fromRGB(0, 0, 0)
TC.BorderSizePixel = 0
TC.Position = UDim2.new(0.300000012, 0, 0.800000012, 0)
TC.Size = UDim2.new(0.25, 0, 0.0833333358, 0)
TC.Font = Enum.Font.SourceSans
TC.Text = ""
TC.TextColor3 = Color3.fromRGB(0, 0, 0)
TC.TextSize = 14.000

UICorner_3.CornerRadius = UDim.new(1, 0)
UICorner_3.Parent = TC

TB.Name = "TB"
TB.Parent = Frame
TB.AnchorPoint = Vector2.new(0.5, 0.5)
TB.BackgroundColor3 = Color3.fromRGB(255, 0, 0)
TB.BorderColor3 = Color3.fromRGB(0, 0, 0)
TB.BorderSizePixel = 0
TB.Position = UDim2.new(0.699999988, 0, 0.800000012, 0)
TB.Size = UDim2.new(0.25, 0, 0.0833333358, 0)
TB.Font = Enum.Font.SourceSans
TB.Text = ""
TB.TextColor3 = Color3.fromRGB(0, 0, 0)
TB.TextSize = 14.000

UICorner_4.CornerRadius = UDim.new(1, 0)
UICorner_4.Parent = TB

TextButton.Parent = ScreenGui
TextButton.AnchorPoint = Vector2.new(0.5, 0.5)
TextButton.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
TextButton.BackgroundTransparency = 0.500
TextButton.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextButton.BorderSizePixel = 0
TextButton.Position = UDim2.new(0.0983999968, 0, 0.369597614, 0)
TextButton.Size = UDim2.new(0, 45, 0, 45)
TextButton.Font = Enum.Font.SourceSans
TextButton.Text = "G"
TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton.TextScaled = true
TextButton.TextSize = 14.000
TextButton.TextWrapped = true

UICorner_5.CornerRadius = UDim.new(0.100000001, 0)
UICorner_5.Parent = TextButton

UIAspectRatioConstraint_2.Parent = TextButton

-- Scripts:

local function MBBIGRW_fake_script() -- Frame.LocalScript 
	local script = Instance.new('LocalScript', Frame)

	local player = game:GetService("Players").LocalPlayer
	
	local Humanoid =  player.Character:WaitForChild("Humanoid")
	
	local tb = script.Parent.TB
	local tc = script.Parent.TC
	local textbox = script.Parent.TextBox
	
	tc.MouseButton1Click:Connect(function()
		Humanoid.WalkSpeed = textbox.ContentText
		
	end)
	
	tb.MouseButton1Click:Connect(function()
		Humanoid.WalkSpeed = 16
	
	end)
	
	
end
coroutine.wrap(MBBIGRW_fake_script)()
local function VHTYKB_fake_script() -- TextButton.LocalScript 
	local script = Instance.new('LocalScript', TextButton)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.Frame.Visible = not script.Parent.Parent.Frame.Visible
	end)
end
coroutine.wrap(VHTYKB_fake_script)()
