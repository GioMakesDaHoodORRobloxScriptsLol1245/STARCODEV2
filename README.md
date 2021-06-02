
local ScreenGui = Instance.new("ScreenGui")
local STARCODE = Instance.new("Frame")
local Label = Instance.new("TextLabel")
local Label_2 = Instance.new("TextLabel")
local Made = Instance.new("TextLabel")
local Label_3 = Instance.new("TextLabel")
local Label_4 = Instance.new("TextLabel")
local KID = Instance.new("TextLabel")
local FLY = Instance.new("TextButton")


ScreenGui.Parent = game.CoreGui
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

STARCODE.Name = "STARCODE"
STARCODE.Parent = ScreenGui
STARCODE.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
STARCODE.BorderColor3 = Color3.fromRGB(53, 53, 53)
STARCODE.BorderSizePixel = 0
STARCODE.Position = UDim2.new(0.127533644, 0, 0.231075704, 0)
STARCODE.Size = UDim2.new(0, 769, 0, 333)
STARCODE.Active = true
STARCODE.Draggable = true

Label.Name = "Label"
Label.Parent = STARCODE
Label.BackgroundColor3 = Color3.fromRGB(255, 206, 206)
Label.BackgroundTransparency = 1.000
Label.BorderSizePixel = 0
Label.Position = UDim2.new(0.018205462, 0, 0.0630630627, 0)
Label.Size = UDim2.new(0, 175, 0, 50)
Label.Font = Enum.Font.SourceSans
Label.Text = "STARCODE"
Label.TextColor3 = Color3.fromRGB(255, 230, 84)
Label.TextScaled = true
Label.TextSize = 14.000
Label.TextWrapped = true

Label_2.Name = "Label"
Label_2.Parent = STARCODE
Label_2.BackgroundColor3 = Color3.fromRGB(0, 4, 255)
Label_2.Position = UDim2.new(0.018205462, 0, 0.195195198, 0)
Label_2.Size = UDim2.new(0, 187, 0, 6)
Label_2.Font = Enum.Font.SourceSans
Label_2.Text = ""
Label_2.TextColor3 = Color3.fromRGB(0, 0, 0)
Label_2.TextSize = 14.000

Made.Name = "Made"
Made.Parent = STARCODE
Made.BackgroundColor3 = Color3.fromRGB(0, 255, 21)
Made.BackgroundTransparency = 1.000
Made.BorderSizePixel = 0
Made.Position = UDim2.new(0.80624187, 0, 0.828828871, 0)
Made.Size = UDim2.new(0, 149, 0, 49)
Made.Font = Enum.Font.SourceSansSemibold
Made.Text = "Made by Deadlygio#7805"
Made.TextColor3 = Color3.fromRGB(255, 255, 255)
Made.TextScaled = true
Made.TextSize = 14.000
Made.TextStrokeColor3 = Color3.fromRGB(115, 255, 1)
Made.TextStrokeTransparency = -1.000
Made.TextWrapped = true

Label_3.Name = "Label"
Label_3.Parent = STARCODE
Label_3.BackgroundColor3 = Color3.fromRGB(4, 3, 2)
Label_3.BorderSizePixel = 0
Label_3.Position = UDim2.new(0.00910273101, 0, 0.270270288, 0)
Label_3.Size = UDim2.new(0, 200, 0, 43)
Label_3.Font = Enum.Font.Cartoon
Label_3.Text = "BODY"
Label_3.TextColor3 = Color3.fromRGB(255, 0, 0)
Label_3.TextScaled = true
Label_3.TextSize = 14.000
Label_3.TextStrokeColor3 = Color3.fromRGB(12, 32, 214)
Label_3.TextStrokeTransparency = 0.000
Label_3.TextWrapped = true

Label_4.Name = "Label"
Label_4.Parent = STARCODE
Label_4.BackgroundColor3 = Color3.fromRGB(255, 64, 0)
Label_4.BorderColor3 = Color3.fromRGB(97, 6, 92)
Label_4.BorderSizePixel = 0
Label_4.Position = UDim2.new(0.00910273101, 0, 0.3993994, 0)
Label_4.Size = UDim2.new(0, 200, 0, 8)
Label_4.Font = Enum.Font.SourceSans
Label_4.Text = ""
Label_4.TextColor3 = Color3.fromRGB(0, 0, 0)
Label_4.TextSize = 14.000

KID.Name = "KID"
KID.Parent = STARCODE
KID.BackgroundColor3 = Color3.fromRGB(221, 255, 0)
KID.BorderSizePixel = 0
KID.Position = UDim2.new(0.302990884, 0, 0.0630630627, 0)
KID.Size = UDim2.new(0, 477, 0, 255)
KID.Font = Enum.Font.Cartoon
KID.Text = "MORE SOON KIDDOS"
KID.TextColor3 = Color3.fromRGB(0, 0, 0)
KID.TextScaled = true
KID.TextSize = 14.000
KID.TextWrapped = true

FLY.Name = "FLY"
FLY.Parent = STARCODE
FLY.BackgroundColor3 = Color3.fromRGB(136, 0, 255)
FLY.Position = UDim2.new(0.0174893495, 0, 0.505706906, 0)
FLY.Size = UDim2.new(0, 200, 0, 59)
FLY.Font = Enum.Font.SciFi
FLY.Text = "FLY"
FLY.TextColor3 = Color3.fromRGB(0, 0, 0)
FLY.TextScaled = true
FLY.TextSize = 14.000
FLY.TextWrapped = true
repeat wait() 
until game.Players.LocalPlayer and game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:findFirstChild("Head") and game.Players.LocalPlayer.Character:findFirstChild("Humanoid") 
local mouse = game.Players.LocalPlayer:GetMouse() 
repeat wait() until mouse
local plr = game.Players.LocalPlayer 
local torso = plr.Character.Head 
local flying = false
local deb = true 
local ctrl = {f = 0, b = 0, l = 0, r = 0} 
local lastctrl = {f = 0, b = 0, l = 0, r = 0} 
local maxspeed = 400 
local speed = 5000 

function Fly() 
	local bg = Instance.new("BodyGyro", torso) 
	bg.P = 9e4 
	bg.maxTorque = Vector3.new(9e9, 9e9, 9e9) 
	bg.cframe = torso.CFrame 
	local bv = Instance.new("BodyVelocity", torso) 
	bv.velocity = Vector3.new(0,0.1,0) 
	bv.maxForce = Vector3.new(9e9, 9e9, 9e9) 
	repeat wait() 
		plr.Character.Humanoid.PlatformStand = true 
		if ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0 then 
			speed = speed+.10+(speed/maxspeed) 
			if speed > maxspeed then 
				speed = maxspeed 
			end 
		elseif not (ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0) and speed ~= 0 then 
			speed = speed-1 
			if speed < 0 then 
				speed = 0 
			end 
		end 
		if (ctrl.l + ctrl.r) ~= 0 or (ctrl.f + ctrl.b) ~= 0 then 
			bv.velocity = ((game.Workspace.CurrentCamera.CoordinateFrame.lookVector * (ctrl.f+ctrl.b)) + ((game.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(ctrl.l+ctrl.r,(ctrl.f+ctrl.b)*.2,0).p) - game.Workspace.CurrentCamera.CoordinateFrame.p))*speed 
			lastctrl = {f = ctrl.f, b = ctrl.b, l = ctrl.l, r = ctrl.r} 
		elseif (ctrl.l + ctrl.r) == 0 and (ctrl.f + ctrl.b) == 0 and speed ~= 0 then 
			bv.velocity = ((game.Workspace.CurrentCamera.CoordinateFrame.lookVector * (lastctrl.f+lastctrl.b)) + ((game.Workspace.CurrentCamera.CoordinateFrame * CFrame.new(lastctrl.l+lastctrl.r,(lastctrl.f+lastctrl.b)*.2,0).p) - game.Workspace.CurrentCamera.CoordinateFrame.p))*speed 
		else 
			bv.velocity = Vector3.new(0,0.1,0) 
		end 
		bg.cframe = game.Workspace.CurrentCamera.CoordinateFrame * CFrame.Angles(-math.rad((ctrl.f+ctrl.b)*50*speed/maxspeed),0,0) 
	until not flying 
	ctrl = {f = 0, b = 0, l = 0, r = 0} 
	lastctrl = {f = 0, b = 0, l = 0, r = 0} 
	speed = 0 
	bg:Destroy() 
	bv:Destroy() 
	plr.Character.Humanoid.PlatformStand = false 
end 
mouse.KeyDown:connect(function(key) 
	if key:lower() == "f" then 
		if flying then flying = false 
		else 
			flying = true 
			Fly() 
		end 
	elseif key:lower() == "w" then 
		ctrl.f = 1 
	elseif key:lower() == "s" then 
		ctrl.b = -1 
	elseif key:lower() == "a" then 
		ctrl.l = -1 
	elseif key:lower() == "d" then 
		ctrl.r = 1 
	end 
end) 
mouse.KeyUp:connect(function(key) 
	if key:lower() == "w" then 
		ctrl.f = 0 
	elseif key:lower() == "s" then 
		ctrl.b = 0 
	elseif key:lower() == "a" then 
		ctrl.l = 0 
	elseif key:lower() == "d" then 
		ctrl.r = 0 
	end 
end)
Fly()
