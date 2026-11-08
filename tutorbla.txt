local main = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local up = Instance.new("TextButton")
local down = Instance.new("TextButton")
local onof = Instance.new("TextButton")
local TextLabel = Instance.new("TextLabel")
local plus = Instance.new("TextButton")
local speed = Instance.new("TextLabel")
local mine = Instance.new("TextButton")
local closebutton = Instance.new("TextButton")
local mini = Instance.new("TextButton")
local mini2 = Instance.new("TextButton")

главный.Name = "main"
main.Parent = game.Игроки.LocalPlayer:WaitForChild("PlayerGui")
главный.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
main.ResetOnSpawn = false

Рамка.Родительский = основной
Рамка.BackgroundColor3 = Color3.fromRGB(163, 255, 137)
Рамка.BorderColor3 = Color3.fromRGB(103, 221, 213)
Рамка.Position = UDim2.new(0.100320168, 0, 0.379746825, 0)
Рамка.Size = UDim2.new(0, 190, 0, 57)

up.Name = "up"
up.Parent = Frame
up.BackgroundColor3 = Color3.fromRGB(79, 255, 152)
up.Size = UDim2.new(0, 44, 0, 28)
up.Font = Enum.Font.SourceSans
up.Text = "UP"
up.TextColor3 = Color3.fromRGB(0, 0, 0)
up.TextSize = 14.000

вниз.Name = "down"
down.Parent = Frame
down.BackgroundColor3 = Color3.fromRGB(215, 255, 121)
вниз.Position = UDim2.new(0, 0, 0.491228074, 0)
down.Size = UDim2.new(0, 44, 0, 28)
down.Font = Enum.Font.SourceSans
down.Text = "DOWN"
down.TextColor3 = Color3.fromRGB(0, 0, 0)
down.TextSize = 14.000

onof.Name = "onof"
onof.Parent = Frame
onof.BackgroundColor3 = Color3.fromRGB(255, 249, 74)
onof.Position = UDim2.new(0.702823281, 0, 0.491228074, 0)
onof.Size = UDim2.new(0, 56, 0, 28)
onof.Font = Enum.Font.SourceSans
onof.Text = "fly"
onof.TextColor3 = Color3.fromRGB(0, 0, 0)
onof.TextSize = 14.000

TextLabel.Parent = Frame
TextLabel.BackgroundColor3 = Color3.fromRGB(242, 60, 255)
TextLabel.Position = UDim2.new(0.469327301, 0, 0, 0)
TextLabel.Size = UDim2.new(0, 100, 0, 28)
TextLabel.Font = Enum.Font.SourceSans
TextLabel.Text = "FLY GUI V3"
TextLabel.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLabel.TextScaled = true
TextLabel.TextSize = 14.000
TextLabel.TextWrapped = true

плюс.Name = "plus"
plus.Parent = Frame
plus.BackgroundColor3 = Color3.fromRGB(133, 145, 255)
плюс.Position = UDim2.new(0.231578946, 0, 0, 0)
плюс.Size = UDim2.new(0, 45, 0, 28)
plus.Font = Enum.Font.SourceSans
plus.Text = "+"
plus.TextColor3 = Color3.fromRGB(0, 0, 0)
плюс.TextScaled = true
plus.TextSize = 14.000
плюс.TextWrapped = true

скорость.Название = «скорость»
скорость.Parent = Frame
speed.BackgroundColor3 = Color3.fromRGB(255, 85, 0)
speed.Position = UDim2.new(0.468421042, 0, 0.491228074, 0)
speed.Size = UDim2.new(0, 44, 0, 28)
speed.Font = Enum.Font.SourceSans
speed.Текст = «1»
скорость.TextColor3 = Color3.fromRGB(0, 0, 0)
speed.TextScaled = true
speed.TextSize = 14.000
скорость.TextWrapped = true

мой.Name = "mine"
mine.Parent = Frame
mine.BackgroundColor3 = Color3.fromRGB(123, 255, 247)
мой.Position = UDim2.new(0.231578946, 0, 0.491228074, 0)
mine.Size = UDim2.new(0, 45, 0, 29)
mine.Font = Enum.Font.SourceSans
mine.Text = "-"
mine.TextColor3 = Color3.fromRGB(0, 0, 0)
mine.TextScaled = true
mine.TextSize = 14.000
mine.TextWrapped = true

closebutton.Name = "Close"
closebutton.Parent = main.Frame
closebutton.BackgroundColor3 = Color3.fromRGB(225, 25, 0)
closebutton.Font = "SourceSans"
closebutton.Size = UDim2.new(0, 45, 0, 28)
closebutton.Text = "X"
closebutton.TextSize = 30
closebutton.Position = UDim2.new(0, 0, -1, 27)

мини.Name = "minimize"
mini.Parent = main.Frame
mini.BackgroundColor3 = Color3.fromRGB(192, 150, 230)
мини.Font = "SourceSans"
mini.Size = UDim2.new(0, 45, 0, 28)
мини.Text = "-"
mini.TextSize = 40
mini.Position = UDim2.new(0, 44, -1, 27)

mini2.Name = "minimize2"
mini2.Parent = main.Frame
mini2.BackgroundColor3 = Color3.fromRGB(192, 150, 230)
mini2.Font = "SourceSans"
mini2.Size = UDim2.new(0, 45, 0, 28)
mini2.Text = "+"
mini2.TextSize = 40
mini2.Position = UDim2.new(0, 44, -1, 57)
mini2.Visible = false

speeds = 1

местный диктор = game:GetService("Игроки").LocalPlayer

local chr = game.Игроки.LocalPlayer.Character
local hum = chr and chr:FindFirstChildWhichIsA("Humanoid")

nowe = false

game:GetService("StarterGui"):SetCore("SendNotification", { 
 Title = "FLY GUI V3";
 Text = "BY XNEO";
 Icon = "rbxthumb://type=Asset&id=5107182114&w=150&h=150"})
Duration = 5;

Рамка.Active = true — main = gui
Рамка.Draggable = true

onof.MouseButton1Down:connect(function()

 if nowe == true then
 nowe = false

 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Climbing,true)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.FallingDown,true)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Flying,true)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Freefall,true)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.GettingUp,true)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Jumping,true)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Landed,true)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Physics,true)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.PlatformStanding,true)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Ragdoll,true)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Running,true)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.RunningNoPhysics,true)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated,true)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.StrafingNoPhysics,true)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Swimming,true)
 оратор.Персонаж.Humanoid:ChangeState(Enum.HumanoidStateType.RunningNoPhysics)
 else 
 nowe = true



 for i = 1, speeds do
 spawn(function()

 local hb = game:GetService("RunService").Сердцебиение 


 tpwalking = истина
 локальный chr = игра.Игроки.LocalPlayer.Character
 local hum = chr and chr:FindFirstChildWhichIsA("Humanoid")
 while tpwalking and hb:Wait() and chr and hum and hum.Parent do
 if hum.MoveDirection.Magnitude > 0 then
 chr:TranslateBy(hum.MoveDirection)
 end
 end

 end)
 конец игры.Игроки.Локальный игрок.Персонаж.Одушевлять.Disabled = true
 local Char = game.Игроки.LocalPlayer.Character
 local Hum = Char:FindFirstChildOfClass("Humanoid") or Char:FindFirstChildOfClass("AnimationController")

 for i,v in next, Hum:GetPlayingAnimationTracks() do
 v:AdjustSpeed(0)
 end
 speaker.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Climbing,false)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.FallingDown,false)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Flying,false)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Freefall,false)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.GettingUp,false)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Jumping,false)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Landed,false)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Physics,false)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.PlatformStanding,false)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Ragdoll,false)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Running,false)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.RunningNoPhysics,false)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Seated,false)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.StrafingNoPhysics,false)
 оратор.Персонаж.Humanoid:SetStateEnabled(Enum.HumanoidStateType.Swimming,false)
 оратор.Персонаж.Humanoid:ChangeState(Enum.HumanoidStateType.Swimming)
 конец




 if game:GetService("Игроки").LocalPlayer.Character:FindFirstChildOfClass("Humanoid").RigType == Enum.HumanoidRigType.R6 then



 local plr = game.Игроки.LocalPlayer
 локальный торс = plr.Персонаж.Торс
 local flying = true
 local deb = true
 local ctrl = {f = 0, b = 0, l = 0, r = 0}
 local lastctrl = {f = 0, b = 0, l = 0, r = 0}
 local maxspeed = 50
 local speed = 0


 local bg = Instance.new("BodyGyro", torso)
 bg.P = 9e4
 bg.maxTorque = Vector3.new(9e9, 9e9, 9e9)
 bg.cframe = torso.CFrame
 local bv = Instance.new("BodyVelocity", torso)
 bv.velocity = Vector3.new(0,0.1,0)
 bv.maxForce = Vector3.new(9e9, 9e9, 9e9)
 если nowe == true, то
 plr.Персонаж.Humanoid.PlatformStand = true
 end
 while nowe == true or game:GetService("Players").Локальный игрок.Персонаж.Humanoid.Health == 0 do
 game:GetService("RunService").RenderStepped:Wait()

 if ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0 then
 speed = speed+.5+(speed/maxspeed)
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
 bv.velocity = ((game.Рабочее место.CurrentCamera.CoordinateFrame.lookVector * (ctrl.f+ctrl.b)) + ((game.Рабочее место.CurrentCamera.CoordinateFrame * CFrame.new(ctrl.l+ctrl.r,(ctrl.f+ctrl.b)*.2,0).p) - game.Рабочее место.CurrentCamera.CoordinateFrame.p))*speed
 lastctrl = {f = ctrl.f, b = ctrl.b, l = ctrl.l, r = ctrl.r}
 elseif (ctrl.l + ctrl.r) == 0 and (ctrl.f + ctrl.b) == 0 and speed ~= 0 then
 bv.velocity = ((game.Рабочее место.CurrentCamera.CoordinateFrame.lookVector * (lastctrl.f+lastctrl.b)) + ((game.Рабочее место.CurrentCamera.CoordinateFrame * CFrame.new(lastctrl.l+lastctrl.r,(lastctrl.f+lastctrl.b)*.2,0).p) - game.Рабочее место.CurrentCamera.CoordinateFrame.p))*speed
 else
 bv.velocity = Vector3.new(0,0,0)
 end
 -- game.Игроки.Локальный игрок.Персонаж.Одушевлять.Disabled = true
 bg.cframe = game.Рабочее место.CurrentCamera.CoordinateFrame * CFrame.Angles(-math.rad((ctrl.f+ctrl.b)*50*speed/maxspeed),0,0)
 end
 ctrl = {f = 0, b = 0, l = 0, r = 0}
 lastctrl = {f = 0, b = 0, l = 0, r = 0}
 speed = 0
 bg:Destroy()
 бв:Уничтожить()
 гбнр.Персонаж.Humanoid.PlatformStand = false
 game.Игроки.Локальный игрок.Персонаж.Одушевлять.Disabled = false
 tpwalking = false




 else
 local plr = game.Игроки.LocalPlayer
 local UpperTorso = plr.Персонаж.UpperTorso
 local flying = true
 local deb = true
 local ctrl = {f = 0, b = 0, l = 0, r = 0}
 local lastctrl = {f = 0, b = 0, l = 0, r = 0}
 local maxspeed = 50
 local speed = 0


 local bg = Instance.new("BodyGyro", UpperTorso)
 bg.P = 9e4
 bg.maxTorque = Vector3.new(9e9, 9e9, 9e9)
 bg.cframe = UpperTorso.CFrame
 local bv = Instance.new("BodyVelocity", UpperTorso)
 bv.velocity = Vector3.new(0,0.1,0)
 bv.maxForce = Vector3.new(9e9, 9e9, 9e9)
 if nowe == true then
 plr.Персонаж.Humanoid.PlatformStand = true
 end
 while nowe == true or game:GetService("Players").Локальный игрок.Персонаж.Humanoid.Health == 0 do
 wait()

 if ctrl.l + ctrl.r ~= 0 or ctrl.f + ctrl.b ~= 0 then
 speed = speed+.5+(speed/maxspeed)
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
 bv.velocity = ((game.Рабочее место.CurrentCamera.CoordinateFrame.lookVector * (ctrl.f+ctrl.b)) + ((game.Рабочее место.CurrentCamera.CoordinateFrame * CFrame.new(ctrl.l+ctrl.r,(ctrl.f+ctrl.b)*.2,0).p) - game.Рабочее место.CurrentCamera.CoordinateFrame.p))*speed
 lastctrl = {f = ctrl.f, b = ctrl.b, l = ctrl.l, r = ctrl.r}
 elseif (ctrl.l + ctrl.r) == 0 and (ctrl.f + ctrl.b) == 0 and speed ~= 0 then
 bv.velocity = ((game.Рабочее место.CurrentCamera.CoordinateFrame.lookVector * (lastctrl.f+lastctrl.b)) + ((game.Рабочее место.CurrentCamera.CoordinateFrame * CFrame.new(lastctrl.l+lastctrl.r,(lastctrl.f+lastctrl.b)*.2,0).p) - game.Рабочее место.CurrentCamera.CoordinateFrame.p))*speed
 else
 bv.velocity = Vector3.new(0,0,0)
 конец

 bg.cframe = game.Рабочее место.CurrentCamera.CoordinateFrame * CFrame.Angles(-math.rad((ctrl.f+ctrl.b)*50*speed/maxspeed),0,0)
 end
 ctrl = {f = 0, b = 0, l = 0, r = 0}
 lastctrl = {f = 0, b = 0, l = 0, r = 0}
 speed = 0
 bg:Destroy()
 бв:Уничтожить()
 гбнр.Персонаж.Humanoid.PlatformStand = false
 game.Игроки.Локальный игрок.Персонаж.Одушевлять.Disabled = false
 tpwalking = false



 конец





end)

local tis

up.MouseButton1Down:connect(function()
 tis = up.MouseEnter:connect(function()
 while tis do
 wait()
 игра.Игроки.Локальный игрок.Персонаж.HumanoidRootPart.CFrame = game.Игроки.Локальный игрок.Персонаж.HumanoidRootPart.CFrame * CFrame.new(0,1,0)
 end
 end)
end)

up.MouseLeave:connect(function()
 if tis then
 tis:Disconnect()
 tis = nil
 end
end)

local dis

вниз.MouseButton1Down:connect(function()
 dis = down.MouseEnter:connect(function()
 пока это происходит
 wait()
 игра.Игроки.Локальный игрок.Персонаж.HumanoidRootPart.CFrame = game.Игроки.Локальный игрок.Персонаж.HumanoidRootPart.CFrame * CFrame.new(0,-1,0)
 end
 end)
end)

вниз.MouseLeave:connect(function()
 if dis then
 dis:Disconnect()
 dis = nil
 end
end)


game:GetService("Players").LocalPlayer.CharacterAdded:Connect(function(char)
 wait(0.7)
 игра.Игроки.Локальный игрок.Персонаж.Humanoid.PlatformStand = false
 game.Игроки.Локальный игрок.Персонаж.Одушевлять.Disabled = false

end)


плюс.MouseButton1Down:connect(function()
 speeds = speeds + 1
 speed.Text = speeds
 if nowe == true then


 tpwalking = false
 for i = 1, speeds do
 spawn(function()

 local hb = game:GetService("RunService").Сердцебиение 


 tpwalking = true
 local chr = game.Игроки.LocalPlayer.Character
 local hum = chr and chr:FindFirstChildWhichIsA("Humanoid")
 while tpwalking and hb:Wait() and chr and hum and hum.Parent do
 if hum.MoveDirection.Magnitude > 0 then
 chr:TranslateBy(hum.MoveDirection)
 end
 end

 end)
 end
 end
end)
mine.MouseButton1Down:connect(function()
 if speeds == 1 then
 speed.Text = 'cannot be less than 1'
 wait(1)
 скорость.Текст = скорости
 else
 speeds = speeds - 1
 speed.Text = speeds
 if nowe == true then
 tpwalking = false
 for i = 1, speeds do
 spawn(function()

 local hb = game:GetService("RunService").Сердцебиение 


 tpwalking = true
 local chr = game.Игроки.LocalPlayer.Character
 local hum = chr and chr:FindFirstChildWhichIsA("Humanoid")
 while tpwalking and hb:Wait() and chr and hum and hum.Parent do
 if hum.MoveDirection.Magnitude > 0 then
 chr:TranslateBy(hum.MoveDirection)
 end
 end

 end)
 end
 end
 end
end)

closebutton.MouseButton1Click:Connect(function()
 main:Destroy()
end)

мини.MouseButton1Click:Connect(function()
 up.Visible = false
 down.Visible = false
 onof.Visible = false
 plus.Visible = false
 speed.Visible = false
 mine.Visible = false
 mini.Visible = false
 mini2.Visible = true
 main.Рамка.BackgroundTransparency = 1
 closebutton.Position = UDim2.new(0, 0, -1, 57)
end)

mini2.MouseButton1Click:Connect(function()
 up.Visible = true
 down.Visible = true
 onof.Visible = true
 plus.Visible = true
 speed.Visible = true
 mine.Visible = true
 mini.Visible = true
 mini2.Visible = false
 main.Рамка.BackgroundTransparency = 0 
 closebutton.Position = UDim2.new(0, 0, -1, 27)
end)
