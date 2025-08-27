-- Gui Script by azzzzbks4 (Pantalla completa y funciona como el primero)

-- Borrar si ya existe para evitar duplicados
if game.Players.LocalPlayer.PlayerGui:FindFirstChild("azzzbkLoading") then
    game.Players.LocalPlayer.PlayerGui:FindFirstChild("azzzbkLoading"):Destroy()
end

-- Crear ScreenGui en PlayerGui
local screenGui = Instance.new("ScreenGui")
screenGui.Name = "azzzbkLoading"
screenGui.ResetOnSpawn = false
screenGui.IgnoreGuiInset = true
screenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

-- Fondo negro (pantalla completa)
local background = Instance.new("Frame")
background.Size = UDim2.new(1, 0, 1, 0)
background.Position = UDim2.new(0, 0, 0, 0)
background.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
background.BorderSizePixel = 0
background.Parent = screenGui

-- Título principal (Nombre del hub)
local title = Instance.new("TextLabel")
title.Size = UDim2.new(1, 0, 0, 100)
title.Position = UDim2.new(0, 0, 0.15, 0)
title.BackgroundTransparency = 1
title.Text = "azzzbk Hub"
title.TextColor3 = Color3.fromRGB(0, 170, 255)
title.TextSize = 60
title.Font = Enum.Font.GothamBold
title.Parent = background

-- Subtítulo (Descripción del script)
local subtitle = Instance.new("TextLabel")
subtitle.Size = UDim2.new(1, 0, 0, 50)
subtitle.Position = UDim2.new(0, 0, 0.28, 0)
subtitle.BackgroundTransparency = 1
subtitle.Text = "Auto Freeze & Auto Gift with User"
subtitle.TextColor3 = Color3.fromRGB(255, 255, 255)
subtitle.TextSize = 28
subtitle.Font = Enum.Font.Gotham
subtitle.Parent = background

-- Texto "Created by"
local createdBy = Instance.new("TextLabel")
createdBy.Size = UDim2.new(1, 0, 0, 30)
createdBy.Position = UDim2.new(0, 0, 0.95, -10)
createdBy.BackgroundTransparency = 1
createdBy.Text = "Created by azzzzbks4"
createdBy.TextColor3 = Color3.fromRGB(100, 100, 255)
createdBy.TextSize = 22
createdBy.Font = Enum.Font.Gotham
createdBy.Parent = background

-- Barra de carga (fondo)
local barBackground = Instance.new("Frame")
barBackground.Size = UDim2.new(0.7, 0, 0, 30)
barBackground.Position = UDim2.new(0.15, 0, 0.55, 0)
barBackground.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
barBackground.BorderSizePixel = 0
barBackground.Parent = background

-- Barra de carga (relleno)
local barFill = Instance.new("Frame")
barFill.Size = UDim2.new(0, 0, 1, 0)
barFill.BackgroundColor3 = Color3.fromRGB(0, 170, 255)
barFill.BorderSizePixel = 0
barFill.Parent = barBackground

-- Texto de porcentaje
local percentText = Instance.new("TextLabel")
percentText.Size = UDim2.new(1, 0, 0, 30)
percentText.Position = UDim2.new(0, 0, 1, 5)
percentText.BackgroundTransparency = 1
percentText.Text = "0%"
percentText.TextColor3 = Color3.fromRGB(255, 255, 255)
percentText.TextSize = 28
percentText.Font = Enum.Font.GothamBold
percentText.Parent = barBackground

-- Animación de carga (5 minutos = 300 segundos)
spawn(function()
    local totalTime = 300
    for i = 1, 100 do
        barFill.Size = UDim2.new(i/100, 0, 1, 0)
        percentText.Text = i.."%"
        wait(totalTime/100)
    end
    -- Mantener en 100%
    barFill.Size = UDim2.new(1, 0, 1, 0)
    percentText.Text = "100%"
end)
