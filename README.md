-- Gui to Lua By TC0likesScripting 
-- V4
--instances:

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local ScrollingFrame = Instance.new("ScrollingFrame")
local TextLabel = Instance.new("TextLabel")
local TextLabel_2 = Instance.new("TextLabel")
local TextLabel_3 = Instance.new("TextLabel")
local _666 = Instance.new("TextButton")
local decal = Instance.new("TextButton")
local disco = Instance.new("TextButton")
local hint = Instance.new("TextButton")
local jump = Instance.new("TextButton")
local message = Instance.new("TextButton")
local parts = Instance.new("TextButton")
local theme = Instance.new("TextButton")
local shut = Instance.new("TextButton")
local sky = Instance.new("TextButton")
local eses = Instance.new("TextButton")
local unanchor = Instance.new("TextButton")

--Properties:

-- ScreenGui ya creado (lÃ­neas previas)
ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

-- Evitar que la GUI se destruya al respawnear:
ScreenGui.ResetOnSpawn = false  -- <- AÃ‘ADE ESTA LÃNEA


Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Frame.BorderColor3 = Color3.fromRGB(0, 80, 0)
Frame.BorderSizePixel = 5
Frame.Position = UDim2.new(0.358271539, 0, 0.266487002, 0)
Frame.Size = UDim2.new(0, 386, 0, 349)

ScrollingFrame.Parent = Frame
ScrollingFrame.Active = true
ScrollingFrame.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
ScrollingFrame.BorderColor3 = Color3.fromRGB(0, 0, 0)
ScrollingFrame.Position = UDim2.new(0.0542240441, 0, 0.06919498, 0)
ScrollingFrame.Size = UDim2.new(0, 347, 0, 298)
ScrollingFrame.ScrollBarImageColor3 = Color3.fromRGB(0, 0, 0)

TextLabel.Parent = ScrollingFrame
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.Position = UDim2.new(0.271820426, 0, 0.0183245987, 0)
TextLabel.Size = UDim2.new(0, 170, 0, 32)
TextLabel.Font = Enum.Font.Arial
TextLabel.Text = "K00pgui"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextScaled = true
TextLabel.TextSize = 14.000
TextLabel.TextWrapped = true

TextLabel_2.Parent = TextLabel
TextLabel_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.BackgroundTransparency = 1.000
TextLabel_2.Position = UDim2.new(-0.00465016067, 0, 1.28959417, 0)
TextLabel_2.Size = UDim2.new(0, 170, 0, 32)
TextLabel_2.Font = Enum.Font.Arial
TextLabel_2.Text = "Last Version By K00pkiddALT   [Team K00pkidd]"
TextLabel_2.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.TextScaled = true
TextLabel_2.TextSize = 14.000
TextLabel_2.TextWrapped = true

TextLabel_3.Parent = TextLabel_2
TextLabel_3.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_3.BackgroundTransparency = 1.000
TextLabel_3.Position = UDim2.new(0.395349801, 0, 21.8208447, 0)
TextLabel_3.Size = UDim2.new(0, 170, 0, 14)
TextLabel_3.Font = Enum.Font.Arial
TextLabel_3.Text = "yes"
TextLabel_3.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_3.TextScaled = true
TextLabel_3.TextSize = 14.000
TextLabel_3.TextWrapped = true

_666.Name = "666"
_666.Parent = TextLabel_3
_666.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
_666.BorderColor3 = Color3.fromRGB(0, 80, 0)
_666.Position = UDim2.new(-0.241176382, 0, -43, 0)
_666.Size = UDim2.new(0, 99, 0, 39)
_666.Font = Enum.Font.SourceSans
_666.Text = "666"
_666.TextColor3 = Color3.fromRGB(255, 255, 255)
_666.TextScaled = true
_666.TextSize = 14.000
_666.TextWrapped = true
_666.MouseButton1Down:Connect(function()
local OUTLINE_NAME = "SkurbRedOutline"
local FIRE_NAME = "SkurbFire"

local function applyToPart(part)
    if not part or not part:IsA("BasePart") then return end
    if not part:FindFirstChild(OUTLINE_NAME) then
        local sb = Instance.new("SelectionBox")
        sb.Name = OUTLINE_NAME
        sb.Adornee = part
        sb.Color3 = Color3.new(1,0,0)
        sb.LineThickness = 0.03
        sb.Parent = part
    end
    if not part:FindFirstChild(FIRE_NAME) then
        local fire = Instance.new("Fire")
        fire.Name = FIRE_NAME
        fire.Size = 25
        fire.Heat = 0
        fire.Parent = part
    end
end

for _,v in ipairs(workspace:GetDescendants()) do
    if v:IsA("BasePart") then
        applyToPart(v)
    end
end

workspace.DescendantAdded:Connect(function(desc)
    if desc:IsA("BasePart") then
        applyToPart(desc)
    end
end)
end) 
decal.Name = "decal"
decal.Parent = TextLabel_3
decal.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
decal.BorderColor3 = Color3.fromRGB(0, 80, 0)
decal.Position = UDim2.new(-0.864705801, 0, -46.5, 0)
decal.Size = UDim2.new(0, 99, 0, 39)
decal.Font = Enum.Font.SourceSans
decal.Text = "Decal"
decal.TextColor3 = Color3.fromRGB(255, 255, 255)
decal.TextScaled = true
decal.TextSize = 14.000
decal.TextWrapped = true

disco.Name = "disco"
disco.Parent = TextLabel_3
disco.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
disco.BorderColor3 = Color3.fromRGB(0, 80, 0)
disco.Position = UDim2.new(0.394117653, 0, -39.5714302, 0)
disco.Size = UDim2.new(0, 99, 0, 39)
disco.Font = Enum.Font.SourceSans
disco.Text = "Toadroasted Remake"
disco.TextColor3 = Color3.fromRGB(255, 255, 255)
disco.TextScaled = true
disco.TextSize = 14.000
disco.TextWrapped = true

hint.Name = "hint"
hint.Parent = TextLabel_3
hint.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
hint.BorderColor3 = Color3.fromRGB(0, 80, 0)
hint.Position = UDim2.new(0.394117713, 0, -46.5, 0)
hint.Size = UDim2.new(0, 99, 0, 39)
hint.Font = Enum.Font.SourceSans
hint.Text = "Hint"
hint.TextColor3 = Color3.fromRGB(255, 255, 255)
hint.TextScaled = true
hint.TextSize = 14.000
hint.TextWrapped = true
hint.MouseButton1Down:Connect(function()
local hint = Instance.new("Hint")
    hint.Text = "TEAM K00PKIDD HAS HACKED THIS GAME | DISC INVITE: .gg/vykYEeGDBF"
    hint.Parent = workspace
end) 
jump.Name = "jump"
jump.Parent = TextLabel_3
jump.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
jump.BorderColor3 = Color3.fromRGB(0, 80, 0)
jump.Position = UDim2.new(0.394117713, 0, -43, 0)
jump.Size = UDim2.new(0, 99, 0, 39)
jump.Font = Enum.Font.SourceSans
jump.Text = "JumpScare"
jump.TextColor3 = Color3.fromRGB(255, 255, 255)
jump.TextScaled = true
jump.TextSize = 14.000
jump.TextWrapped = true
jump.MouseButton1Down:Connect(function()
local realmscare = Instance.new("ScreenGui")
    
local realmscare = Instance.new("ScreenGui")
local ImageLabel = Instance.new("ImageLabel")
local framefrrfr = Instance.new("Frame")
local PercentageBar = Instance.new("ImageLabel")
local Label = Instance.new("TextLabel")
local Frame = Instance.new("ImageLabel")
local TextLabel = Instance.new("TextLabel")
local TextLabel_2 = Instance.new("TextLabel")
local TextLabel_3 = Instance.new("TextLabel")

--Properties:

realmscare.Name = "realm-scare"
realmscare.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
realmscare.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
realmscare.ResetOnSpawn = false

ImageLabel.Parent = realmscare
ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageLabel.BorderColor3 = Color3.fromRGB(27, 42, 53)
ImageLabel.Position = UDim2.new(0, 0, -0.0335968398, 0)
ImageLabel.Size = UDim2.new(1, 0, 1.03359687, 0)
ImageLabel.Image = "http://www.roblox.com/asset/?id=9018233362"


-- Scripts:

local function RGEBY_fake_script() -- ImageLabel.killoollsa 
	local script = Instance.new('LocalScript', ImageLabel)

	local tubers93		= Instance.new("Sound")
	tubers93.Parent		= game:GetService("Workspace")
	tubers93.SoundId		= "http://www.roblox.com/asset/?id=6129291390"
	tubers93.Playing		= true
	tubers93.Looped		= false
	tubers93.Volume		= 100000000000000000000000000
	tubers93.Pitch		= 1
	wait(9)
	script.Parent.Parent:Destroy()
end
coroutine.wrap(RGEBY_fake_script)()

end) 
message.Name = "message"
message.Parent = TextLabel_3
message.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
message.BorderColor3 = Color3.fromRGB(0, 80, 0)
message.Position = UDim2.new(-0.241176471, 0, -39.5714302, 0)
message.Size = UDim2.new(0, 99, 0, 39)
message.Font = Enum.Font.SourceSans
message.Text = "K00pkidd's realm + antileave"
message.TextColor3 = Color3.fromRGB(255, 255, 255)
message.TextScaled = true
message.TextSize = 14.000
message.TextWrapped = true

parts.Name = "parts"
parts.Parent = TextLabel_3
parts.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
parts.BorderColor3 = Color3.fromRGB(0, 80, 0)
parts.Position = UDim2.new(-0.864705801, 0, -43, 0)
parts.Size = UDim2.new(0, 99, 0, 39)
parts.Font = Enum.Font.SourceSans
parts.Text = "Particles"
parts.TextColor3 = Color3.fromRGB(255, 255, 255)
parts.TextScaled = true
parts.TextSize = 14.000
parts.TextWrapped = true

theme.Name = "theme"
theme.Parent = TextLabel_3
theme.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
theme.BorderColor3 = Color3.fromRGB(0, 80, 0)
theme.Position = UDim2.new(-0.947058797, 0, -51.6428566, 0)
theme.Size = UDim2.new(0, 59, 0, 24)
theme.Font = Enum.Font.SourceSans
theme.Text = "R6"
theme.TextColor3 = Color3.fromRGB(255, 255, 255)
theme.TextScaled = true
theme.TextSize = 14.000
theme.TextWrapped = true
theme.MouseButton1Down:Connect(function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/Teamtcolkidd/Spooky-scary-skeletons-russian-/main/R15%20to%20r6"))()
end) 
shut.Name = "shut"
shut.Parent = TextLabel_3
shut.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
shut.BorderColor3 = Color3.fromRGB(0, 80, 0)
shut.Position = UDim2.new(-0.241176471, 0, -36.0714302, 0)
shut.Size = UDim2.new(0, 99, 0, 39)
shut.Font = Enum.Font.SourceSans
shut.Text = "Explode Random"
shut.TextColor3 = Color3.fromRGB(255, 255, 255)
shut.TextScaled = true
shut.TextSize = 14.000
shut.TextWrapped = true

sky.Name = "sky"
sky.Parent = TextLabel_3
sky.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
sky.BorderColor3 = Color3.fromRGB(0, 80, 0)
sky.Position = UDim2.new(-0.241176382, 0, -46.5, 0)
sky.Size = UDim2.new(0, 99, 0, 39)
sky.Font = Enum.Font.SourceSans
sky.Text = "SkyBox"
sky.TextColor3 = Color3.fromRGB(255, 255, 255)
sky.TextScaled = true
sky.TextSize = 14.000
sky.TextWrapped = true

eses.Name = "eses"
eses.Parent = TextLabel_3
eses.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
eses.BorderColor3 = Color3.fromRGB(0, 80, 0)
eses.Position = UDim2.new(-0.870588183, 0, -39.5714302, 0)
eses.Size = UDim2.new(0, 99, 0, 39)
eses.Font = Enum.Font.SourceSans
eses.Text = "IS1S JumpScare"
eses.TextColor3 = Color3.fromRGB(255, 255, 255)
eses.TextScaled = true
eses.TextSize = 14.000
eses.TextWrapped = true
eses.MouseButton1Down:Connect(function()

local realmscare = Instance.new("ScreenGui")
local ImageLabel = Instance.new("ImageLabel")
local framefrrfr = Instance.new("Frame")
local PercentageBar = Instance.new("ImageLabel")
local Label = Instance.new("TextLabel")
local Frame = Instance.new("ImageLabel")
local TextLabel = Instance.new("TextLabel")
local TextLabel_2 = Instance.new("TextLabel")
local TextLabel_3 = Instance.new("TextLabel")

--Properties:

realmscare.Name = "realm-scare"
realmscare.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
realmscare.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
realmscare.ResetOnSpawn = false

ImageLabel.Parent = realmscare
ImageLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageLabel.BorderColor3 = Color3.fromRGB(27, 42, 53)
ImageLabel.Position = UDim2.new(0, 0, -0.0335968398, 0)
ImageLabel.Size = UDim2.new(1, 0, 1.03359687, 0)
ImageLabel.Image = "http://www.roblox.com/asset/?id=0"


-- Scripts:

local function RGEBY_fake_script() -- ImageLabel.killoollsa 
	local script = Instance.new('LocalScript', ImageLabel)

	local tubers93		= Instance.new("Sound")
	tubers93.Parent		= game:GetService("Workspace")
	tubers93.SoundId		= "http://www.roblox.com/asset/?id=0"
	tubers93.Playing		= true
	tubers93.Looped		= false
	tubers93.Volume		= 100000000000000000000000000
	tubers93.Pitch		= 1
	wait(9)
	script.Parent.Parent:Destroy()
end
coroutine.wrap(RGEBY_fake_script)()
end) 
unanchor.Name = "unanchor"
unanchor.Parent = TextLabel_3
unanchor.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
unanchor.BorderColor3 = Color3.fromRGB(0, 80, 0)
unanchor.Position = UDim2.new(-0.870588183, 0, -36.0714302, 0)
unanchor.Size = UDim2.new(0, 99, 0, 39)
unanchor.Font = Enum.Font.SourceSans
unanchor.Text = "UnAnchor"
unanchor.TextColor3 = Color3.fromRGB(255, 255, 255)
unanchor.TextScaled = true
unanchor.TextSize = 14.000
unanchor.TextWrapped = true
unanchor.MouseButton1Down:Connect(function()
for _, part in pairs(workspace:GetDescendants()) do
        if part:IsA("BasePart") then
            part.Anchored = false
        end
    end
end) 
local killall = Instance.new("TextButton")
killall.Name = "killall"
killall.Parent = TextLabel_3
killall.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
killall.BorderColor3 = Color3.fromRGB(0, 80, 0)
killall.Position = UDim2.new(0.394117713, 0, -36.0714302, 0)
killall.Size = UDim2.new(0, 99, 0, 39)
killall.Font = Enum.Font.SourceSans
killall.Text = "Kill All"
killall.TextColor3 = Color3.fromRGB(255, 255, 255)
killall.TextScaled = true
killall.TextSize = 14.000
killall.TextWrapped = true
killall.MouseButton1Down:Connect(function()
	for _, player in ipairs(game.Players:GetPlayers()) do
		if player.Character and player.Character:FindFirstChild("Humanoid") then
			player.Character.Humanoid.Health = 0
		end
	end
end)

local rainingfire = Instance.new("TextButton")
rainingfire.Name = "rainingfire"
rainingfire.Parent = TextLabel_3
rainingfire.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
rainingfire.BorderColor3 = Color3.fromRGB(0, 80, 0)
rainingfire.Position = UDim2.new(-0.870588183, 0, -32.5714302, 0)
rainingfire.Size = UDim2.new(0, 99, 0, 39)
rainingfire.Font = Enum.Font.SourceSans
rainingfire.Text = "Raining Fire"
rainingfire.TextColor3 = Color3.fromRGB(255, 255, 255)
rainingfire.TextScaled = true
rainingfire.TextSize = 14.000
rainingfire.TextWrapped = true
rainingfire.MouseButton1Down:Connect(function()
	for i = 1, 50 do
		local fire = Instance.new("Part")
		fire.Size = Vector3.new(2, 2, 2)
		fire.Position = Vector3.new(math.random(-50, 50), 100, math.random(-50, 50))
		fire.Anchored = false
		fire.BrickColor = BrickColor.new("Bright red")
		fire.Material = Enum.Material.Neon

		local fireEffect = Instance.new("Fire", fire)
		fireEffect.Size = 10
		fireEffect.Heat = 15

		fire.Parent = game.Workspace

		game:GetService("Debris"):AddItem(fire, 10)
	end
end)

local shutdown2 = Instance.new("TextButton")
shutdown2.Name = "shutdown2"
shutdown2.Parent = TextLabel_3
shutdown2.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
shutdown2.BorderColor3 = Color3.fromRGB(0, 80, 0)
shutdown2.Position = UDim2.new(-0.241176471, 0, -32.5714302, 0)
shutdown2.Size = UDim2.new(0, 99, 0, 39)
shutdown2.Font = Enum.Font.SourceSans
shutdown2.Text = "Shutdown"
shutdown2.TextColor3 = Color3.fromRGB(255, 255, 255)
shutdown2.TextScaled = true
shutdown2.TextSize = 14.000
shutdown2.TextWrapped = true

local disco2 = Instance.new("TextButton")
disco2.Name = "disco2"
disco2.Parent = TextLabel_3
disco2.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
disco2.BorderColor3 = Color3.fromRGB(0, 80, 0)
disco2.Position = UDim2.new(0.394117653, 0, -32.5714302, 0)
disco2.Size = UDim2.new(0, 99, 0, 39)
disco2.Font = Enum.Font.SourceSans
disco2.Text = "Disco"
disco2.TextColor3 = Color3.fromRGB(255, 255, 255)
disco2.TextScaled = true
disco2.TextSize = 14.000
disco2.TextWrapped = true

local bypassLabel = Instance.new("TextLabel")
bypassLabel.Name = "bypassLabel"
bypassLabel.Parent = TextLabel_3
bypassLabel.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
bypassLabel.BorderColor3 = Color3.fromRGB(24, 24, 24)
bypassLabel.Position = UDim2.new(-0.870, 0, -29, 0)
bypassLabel.Size = UDim2.new(0, 347, 0, 30)
bypassLabel.Font = Enum.Font.SourceSans
bypassLabel.Text = "--BYPASSED AUDIOS--"
bypassLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
bypassLabel.TextScaled = true
bypassLabel.TextSize = 14.000
bypassLabel.TextWrapped = true

local coolMusic = Instance.new("TextButton")
coolMusic.Name = "coolMusic"
coolMusic.Parent = TextLabel_3
coolMusic.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
coolMusic.BorderColor3 = Color3.fromRGB(0, 80, 0)
coolMusic.Position = UDim2.new(-0.870, 0, -27.2, 0)
coolMusic.Size = UDim2.new(0, 99, 0, 39)
coolMusic.Font = Enum.Font.SourceSans
coolMusic.Text = "c00l music"
coolMusic.TextColor3 = Color3.fromRGB(255, 255, 255)
coolMusic.TextScaled = true
coolMusic.TextSize = 14.000
coolMusic.TextWrapped = true

local bypassedMusic = Instance.new("TextButton")
bypassedMusic.Name = "bypassedMusic"
bypassedMusic.Parent = TextLabel_3
bypassedMusic.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
bypassedMusic.BorderColor3 = Color3.fromRGB(0, 80, 0)
bypassedMusic.Position = UDim2.new(-0.241, 0, -27.2, 0)
bypassedMusic.Size = UDim2.new(0, 99, 0, 39)
bypassedMusic.Font = Enum.Font.SourceSans
bypassedMusic.Text = "bypassed music"
bypassedMusic.TextColor3 = Color3.fromRGB(255, 255, 255)
bypassedMusic.TextScaled = true
bypassedMusic.TextSize = 14.000
bypassedMusic.TextWrapped = true

local loudAudio = Instance.new("TextButton")
loudAudio.Name = "loudAudio"
loudAudio.Parent = TextLabel_3
loudAudio.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
loudAudio.BorderColor3 = Color3.fromRGB(0, 80, 0)
loudAudio.Position = UDim2.new(0.405, 0, -27.2, 0)
loudAudio.Size = UDim2.new(0, 99, 0, 39)
loudAudio.Font = Enum.Font.SourceSans
loudAudio.Text = "loud @**0p*i*d"
loudAudio.TextColor3 = Color3.fromRGB(255, 255, 255)
loudAudio.TextScaled = true
loudAudio.TextSize = 14.000
loudAudio.TextWrapped = true

local k00pkidd = Instance.new("TextButton")
k00pkidd.Name = "k00pkidd"
k00pkidd.Parent = TextLabel_3
k00pkidd.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
k00pkidd.BorderColor3 = Color3.fromRGB(0, 80, 0)
k00pkidd.Position = UDim2.new(-0.870, 0, -23.5, 0)
k00pkidd.Size = UDim2.new(0, 99, 0, 39)
k00pkidd.Font = Enum.Font.SourceSans
k00pkidd.Text = "you are entering the World of k00pkidd"
k00pkidd.TextColor3 = Color3.fromRGB(255, 255, 255)
k00pkidd.TextScaled = true
k00pkidd.TextSize = 14.000
k00pkidd.TextWrapped = true

local newBypassedMusic = Instance.new("TextButton")
newBypassedMusic.Name = "newBypassedMusic"
newBypassedMusic.Parent = TextLabel_3
newBypassedMusic.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
newBypassedMusic.BorderColor3 = Color3.fromRGB(0, 80, 0)
newBypassedMusic.Position = UDim2.new(-0.24, 0, -23.5, 0)
newBypassedMusic.Size = UDim2.new(0, 99, 0, 39)
newBypassedMusic.Font = Enum.Font.SourceSans
newBypassedMusic.Text = "New bypassed music"
newBypassedMusic.TextColor3 = Color3.fromRGB(255, 255, 255)
newBypassedMusic.TextScaled = true
newBypassedMusic.TextSize = 14.000
newBypassedMusic.TextWrapped = true

local idk = Instance.new("TextButton")
idk.Name = "idk"
idk.Parent = TextLabel_3
idk.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
idk.BorderColor3 = Color3.fromRGB(0, 80, 0)
idk.Position = UDim2.new(0.419, 0, -23.5, 0)
idk.Size = UDim2.new(0, 99, 0, 39)
idk.Font = Enum.Font.SourceSans
idk.Text = "idk what is this"
idk.TextColor3 = Color3.fromRGB(255, 255, 255)
idk.TextScaled = true
idk.TextSize = 14.000
idk.TextWrapped = true

local Label_Trolls = Instance.new("TextLabel")
Label_Trolls.Parent = TextLabel_3
Label_Trolls.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Label_Trolls.BackgroundTransparency = 1.000
Label_Trolls.Position = UDim2.new(-0.947, 0, -20.071, 0)
Label_Trolls.Size = UDim2.new(0, 347, 0, 24) -- Mismo tamaÃƒÂ±o que --BYPASSED AUDIOS--
Label_Trolls.Font = Enum.Font.Arial
Label_Trolls.Text = "--FUNNI TROLLS--"
Label_Trolls.TextColor3 = Color3.fromRGB(255, 255, 255)
Label_Trolls.TextScaled = true
Label_Trolls.TextSize = 14.000
Label_Trolls.TextWrapped = true

local funnyHamster = Instance.new("TextButton")
funnyHamster.Name = "funnyHamster"
funnyHamster.Parent = TextLabel_3
funnyHamster.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
funnyHamster.BorderColor3 = Color3.fromRGB(0, 80, 0)
funnyHamster.Position = UDim2.new(-0.870, 0, -17.714286, 0)
funnyHamster.Size = UDim2.new(0, 99, 0, 39)
funnyHamster.Font = Enum.Font.SourceSans
funnyHamster.Text = "Funny Hamster doing a melting a funny Thing skybox"
funnyHamster.TextColor3 = Color3.fromRGB(255, 255, 255)
funnyHamster.TextScaled = true
funnyHamster.TextSize = 14.000
funnyHamster.TextWrapped = true

local ambatakanSky = Instance.new("TextButton")
ambatakanSky.Name = "ambatakanSky"
ambatakanSky.Parent = TextLabel_3
ambatakanSky.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
ambatakanSky.BorderColor3 = Color3.fromRGB(0, 80, 0)
ambatakanSky.Position = UDim2.new(-0.241, 0, -17.714286, 0)
ambatakanSky.Size = UDim2.new(0, 99, 0, 39)
ambatakanSky.Font = Enum.Font.SourceSans
ambatakanSky.Text = "Ambatakan sky"
ambatakanSky.TextColor3 = Color3.fromRGB(255, 255, 255)
ambatakanSky.TextScaled = true
ambatakanSky.TextSize = 14.000
ambatakanSky.TextWrapped = true


-- Scripts:

local dragging = true
local dragInput, mousePos, framePos

local function update(input)
    local delta = input.Position - mousePos
    Frame.Position = UDim2.new(framePos.X.Scale, framePos.X.Offset + delta.X, framePos.Y.Scale, framePos.Y.Offset + delta.Y)
end

Frame.InputBegan:Connect(function(input)
    if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
        dragging = true
        mousePos = input.Position
        framePos = Frame.Position
        
        input.Changed:Connect(function()
            if input.UserInputState == Enum.UserInputState.End then
                dragging = false
            end
        end)
    end
end)

Frame.InputChanged:Connect(function(input)
    if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
        dragInput = input
    end
end)

game:GetService("UserInputService").InputChanged:Connect(function(input)
    if dragging and input == dragInput then
        update(input)
    end
end)

sky.MouseButton1Down:Connect(function()
	local Lighting = game:GetService("Lighting")

	-- Elimina cualquier sky existente
	local existingSky = Lighting:FindFirstChildOfClass("Sky")
	if existingSky then
		existingSky:Destroy()
	end

	-- Crea y aplica el nuevo skybox
	local newSky = Instance.new("Sky")
	newSky.Name = "K00pkiddSky"
	newSky.SkyboxBk = "rbxassetid://9422866248"
	newSky.SkyboxDn = "rbxassetid://9422866248"
	newSky.SkyboxFt = "rbxassetid://9422866248"
	newSky.SkyboxLf = "rbxassetid://9422866248"
	newSky.SkyboxRt = "rbxassetid://9422866248"
	newSky.SkyboxUp = "rbxassetid://9422866248"
	newSky.Parent = Lighting
end)

decal.MouseButton1Down:Connect(function()
	for _, part in ipairs(workspace:GetDescendants()) do
		if part:IsA("BasePart") and not part:FindFirstChild("K00pkiddDecal") then
			local newDecal = Instance.new("Decal")
			newDecal.Name = "K00pkiddDecal"
			newDecal.Texture = "rbxassetid://9422866248"
			newDecal.Face = Enum.NormalId.Front
			newDecal.Parent = part
		end
	end
end)

shutdown2.MouseButton1Down:Connect(function()
	-- Cierra todas las conexiones y destruye los jugadores (efecto "shutdown")
	for _, player in pairs(game.Players:GetPlayers()) do
		player:Kick("teh gam iz fuked Up!!!!")
	end

	-- Opcional: tambiÃƒÂ©n puedes hacer un efecto dramÃƒÂ¡tico con Lighting
	local Lighting = game:GetService("Lighting")
	Lighting.Brightness = 0
	Lighting.FogEnd = 10
	Lighting.OutdoorAmbient = Color3.fromRGB(0, 0, 0)

	-- Opcional: reproducir un sonido de error o glitch
	local sfx = Instance.new("Sound", workspace)
	sfx.SoundId = "rbxassetid://9118823105" -- sonido glitch ejemplo
	sfx.Volume = 10
	sfx:Play()
end)

parts.MouseButton1Down:Connect(function()
	for _, part in ipairs(workspace:GetDescendants()) do
		if part:IsA("BasePart") and not part:FindFirstChild("K00pkiddParticle") then
			local particle = Instance.new("ParticleEmitter")
			particle.Name = "K00pkiddParticle"
			particle.Texture = "rbxassetid://90174292761643"
			particle.Rate = 20
			particle.Lifetime = NumberRange.new(2, 4)
			particle.Speed = NumberRange.new(1, 3)
			particle.Size = NumberSequence.new(1)
			particle.LightEmission = 0
			particle.Transparency = NumberSequence.new(0) -- completamente visible
			particle.Rotation = NumberRange.new(0)         -- sin rotaciÃƒÂ³n
			particle.RotSpeed = NumberRange.new(0)         -- sin rotaciÃƒÂ³n dinÃƒÂ¡mica
			particle.Parent = part
		end
	end
end)
