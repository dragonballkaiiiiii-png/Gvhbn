--[[
💀 Team Black: Founder Script (Atualizado) 💀
- Hack Vision agora é um ESP (destaca outros jogadores)
- Nova habilidade: Fade Square (quadrado com degradê que some gradualmente)
100% LocalScript — compatível Mobile/PC
--]]

local Players = game:GetService("Players")
local TweenService = game:GetService("TweenService")
local Debris = game:GetService("Debris")
local player = Players.LocalPlayer

-- ---------- GUI ----------
local gui = Instance.new("ScreenGui")
gui.Name = "TeamBlackBase"
gui.ResetOnSpawn = false
gui.Parent = player:WaitForChild("PlayerGui")

local mainFrame = Instance.new("Frame")
mainFrame.Name = "Main"
mainFrame.Size = UDim2.new(0, 360, 0, 260)
mainFrame.Position = UDim2.new(0.32, 0, 0.27, 0)
mainFrame.BackgroundColor3 = Color3.fromRGB(6,6,10)
mainFrame.BorderSizePixel = 0
mainFrame.Active = true
mainFrame.Draggable = true
mainFrame.Parent = gui

local uiStroke = Instance.new("UIStroke", mainFrame)
uiStroke.Thickness = 2
uiStroke.Color = Color3.fromRGB(0, 0, 255)

-- anima neon (suave)
task.spawn(function()
	while true do
		uiStroke.Color = Color3.fromHSV((tick()%5)/5, 1, 1)
		task.wait(0.06)
	end
end)

local title = Instance.new("TextLabel", mainFrame)
title.Size = UDim2.new(1, 0, 0, 36)
title.Position = UDim2.new(0, 0, 0, 0)
title.BackgroundTransparency = 1
title.Font = Enum.Font.Code
title.TextSize = 18
title.TextColor3 = Color3.fromRGB(0, 170, 255)
title.Text = "TEAM BLACK // FOUNDER"

-- container de botões
local buttonsFrame = Instance.new("Frame", mainFrame)
buttonsFrame.Size = UDim2.new(1, -20, 1, -50)
buttonsFrame.Position = UDim2.new(0, 10, 0, 40)
buttonsFrame.BackgroundTransparency = 1

-- lista de poderes (inclui Fade Square)
local powers = {
	"Dark Aura",
	"Black Dash",
	"Electric Shock",
	"Hack Vision (ESP)",
	"Shadow Explosion",
	"Fade Square"
}

-- tabelas de controle
local highlights = {} -- guarda Highlight por player (ESP)
local hackVisionOn = false

-- função utilitária: cria botão
local function createPowerButton(name, index)
	local btn = Instance.new("TextButton")
	btn.Size = UDim2.new(0.95, 0, 0, 34)
	btn.Position = UDim2.new(0.025, 0, 0, (index-1)*40)
	btn.BackgroundColor3 = Color3.fromRGB(12,12,18)
	btn.BorderSizePixel = 0
	btn.Font = Enum.Font.Code
	btn.TextSize = 15
	btn.TextColor3 = Color3.fromRGB(230,230,230)
	btn.Text = name
	btn.AutoButtonColor = true
	btn.Parent = buttonsFrame
	return btn
end

-- função: aplica Dark Aura (partículas ao redor)
local function doDarkAura()
	local char = player.Character
	if not char or not char:FindFirstChild("HumanoidRootPart") then return end
	local root = char.HumanoidRootPart
	local emit = Instance.new("ParticleEmitter")
	emit.Texture = "rbxassetid://241594419" -- exemplo
	emit.Rate = 40
	emit.Lifetime = NumberRange.new(0.9)
	emit.Speed = NumberRange.new(1,2)
	emit.Size = NumberSequence.new(1.5)
	emit.Color = ColorSequence.new(Color3.fromRGB(0,0,255))
	emit.Parent = root
	Debris:AddItem(emit, 8)
end

-- função: dash (teleporte curto com som)
local function doBlackDash()
	local char = player.Character
	if not char or not char:FindFirstChild("HumanoidRootPart") then return end
	local root = char.HumanoidRootPart
	local dir = root.CFrame.LookVector
	local dest = root.Position + dir * 35
	root.CFrame = CFrame.new(dest) * CFrame.Angles(0, root.CFrame:ToEulerAnglesYXZ())
	local s = Instance.new("Sound", root)
	s.SoundId = "rbxassetid://138081500"
	s.Volume = 0.8
	s:Play()
	Debris:AddItem(s, 2)
end

-- função: electric shock (pequena explosão no cliente)
local function doElectricShock()
	local char = player.Character
	if not char or not char:FindFirstChild("HumanoidRootPart") then return end
	local expl = Instance.new("Explosion")
	expl.Position = char.HumanoidRootPart.Position
	expl.BlastRadius = 8
	expl.BlastPressure = 30000
	expl.Parent = workspace
	Debris:AddItem(expl, 1)
end

-- função: shadow explosion (maior)
local function doShadowExplosion()
	local char = player.Character
	if not char or not char:FindFirstChild("HumanoidRootPart") then return end
	local expl = Instance.new("Explosion")
	expl.Position = char.HumanoidRootPart.Position
	expl.BlastRadius = 18
	expl.BlastPressure = 80000
	expl.Parent = workspace
	Debris:AddItem(expl, 2)
end

-- FUNÇÃO ESP (Hack Vision)
local function enableHackVision()
	if hackVisionOn then return end
	hackVisionOn = true

	local function addHighlightToCharacter(char, plr)
		if not char or not char.PrimaryPart then
			-- aguarda PrimaryPart / HumanoidRootPart
			local ok = char:WaitForChild("HumanoidRootPart", 2)
			if not ok then return end
		end
		-- protege contra destacar o próprio jogador
		if plr == player then return end
		-- cria highlight
		local h = Instance.new("Highlight")
		h.Adornee = char
		h.Parent = char
		h.FillColor = Color3.fromRGB(0, 0, 80) -- azul escuro preenchimento
		h.FillTransparency = 0.6
		h.OutlineColor = Color3.fromRGB(0, 170, 255)
		h.OutlineTransparency = 0
		highlights[plr] = h
	end

	-- adiciona para os já presentes
	for _, plr in ipairs(Players:GetPlayers()) do
		if plr.Character and plr ~= player then
			addHighlightToCharacter(plr.Character, plr)
		end
		-- conecta a character adicionada do jogador alvo
		plr.CharacterAdded:Connect(function(char)
			if not hackVisionOn then return end
			addHighlightToCharacter(char, plr)
		end)
	end

	-- future players
	Players.PlayerAdded:Connect(function(plr)
		plr.CharacterAdded:Connect(function(char)
			if not hackVisionOn then return end
			addHighlightToCharacter(char, plr)
		end)
	end)
end

local function disableHackVision()
	hackVisionOn = false
	for plr, h in pairs(highlights) do
		if h and h.Parent then
			h:Destroy()
		end
		highlights[plr] = nil
	end
end

-- FUNÇÃO: Fade Square (cria um quadrado UI com degradê que some)
local function doFadeSquare()
	-- cria container temporário
	local sq = Instance.new("Frame")
	sq.Size = UDim2.new(0, 300, 0, 300)
	sq.Position = UDim2.new(0.5, -150, 0.5, -150)
	sq.AnchorPoint = Vector2.new(0.5, 0.5)
	sq.BackgroundTransparency = 0
	sq.BackgroundColor3 = Color3.fromRGB(0,0,0)
	sq.BorderSizePixel = 0
	sq.Parent = gui

	-- aplica um degradê (UIGradient)
	local grad = Instance.new("UIGradient", sq)
	grad.Rotation = 45
	grad.Transparency = NumberSequence.new({
		NumberSequenceKeypoint.new(0, 0),
		NumberSequenceKeypoint.new(1, 1)
	})
	grad.Color = ColorSequence.new{
		ColorSequenceKeypoint.new(0, Color3.fromRGB(0, 0, 255)),
		ColorSequenceKeypoint.new(1, Color3.fromRGB(0, 0, 0))
	}

	-- anima desaparecimento com Tween (faz o quad sumir em 3s)
	local tweenInfo = TweenInfo.new(3, Enum.EasingStyle.Quart, Enum.EasingDirection.Out)
	local tweenGoal = {BackgroundTransparency = 1}
	local tween = TweenService:Create(sq, tweenInfo, tweenGoal)
	tween:Play()

	-- também animar a transparência do grad (opcional)
	local goal = {Transparency = NumberSequence.new(1)}
	local gradTween = TweenService:Create(grad, tweenInfo, {Transparency = NumberSequence.new(1)})
	gradTween:Play()
	-- depois remove
	tween.Completed:Connect(function()
		if sq and sq.Parent then
			sq:Destroy()
		end
	end)
	-- garante remoção
	Debris:AddItem(sq, 4)
end

-- cria botões e conecta eventos
for i, name in ipairs(powers) do
	local btn = createPowerButton(name, i)
	btn.MouseButton1Click:Connect(function()
		-- checagem de cooldown simples (pode expandir)
		btn.Active = false
		btn.AutoButtonColor = false
		btn.Text = name.." • Activated"
		task.delay(0.3, function() -- anima resposta rápida
			btn.Text = name
			btn.Active = true
			btn.AutoButtonColor = true
		end)

		-- executa habilidade
		if name == "Dark Aura" then
			doDarkAura()
		elseif name == "Black Dash" then
			doBlackDash()
		elseif name == "Electric Shock" then
			doElectricShock()
		elseif name == "Hack Vision (ESP)" then
			-- alterna ESP on/off
			if hackVisionOn then
				disableHackVision()
				btn.Text = "Hack Vision (ESP) • Off"
				task.delay(1.2, function() btn.Text = name end)
			else
				enableHackVision()
				btn.Text = "Hack Vision (ESP) • On"
				task.delay(1.2, function() btn.Text = name end)
			end
		elseif name == "Shadow Explosion" then
			doShadowExplosion()
		elseif name == "Fade Square" then
			doFadeSquare()
		end
	end)
end

-- ---------- EFEITO DE ENTRADA (visual) ----------
local lighting = game:GetService("Lighting")
local blur = Instance.new("BlurEffect")
blur.Size = 0
blur.Parent = lighting
for i = 1, 12 do
	blur.Size = i
	task.wait(0.02)
end
for i = 12, 0, -1 do
	blur.Size = i
	task.wait(0.02)
end
blur:Destroy()

-- mensagem de entrada
local msg = Instance.new("Message", workspace)
msg.Text = "⚡ Fundador do Team Black entrou ⚡"
Debris:AddItem(msg, 4)

-- limpeza ao sair / respawn
player.AncestryChanged:Connect(function()
	if not player:IsDescendantOf(game) then
		disableHackVision()
	end
end)

-- fim do script
