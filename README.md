
local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()

local Window = OrionLib:MakeWindow({Name = "OW 힌국", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})

--[[
Name = <string> - The name of the UI.
HidePremium = <bool> - Whether or not the user details shows Premium status or not.
SaveConfig = <bool> - Toggles the config saving in the UI.
ConfigFolder = <string> - The name of the folder where the configs are saved.
IntroEnabled = <bool> - Whether or not to show the intro animation.
IntroText = <string> - Text to show in the intro animation.
IntroIcon = <string> - URL to the image you want to use in the intro animation.
Icon = <string> - URL to the image you want displayed on the window.
CloseCallback = <function> - Function to execute when the window is closed.
]]

local PlayerTab = Window:MakeTab({
 Name = "플레이어",
 Icon = "rbxassetid://4483345998",
 PremiumOnly = false
})

local Section = PlayerTab:AddSection({
 Name = "움직임 PC 전용"
})

PlayerTab:AddSlider({
 Name = "플레이어 스피드",
 Min = 16,
 Max = 500,
 Default = 16,
 Color = Color3.fromRGB(255,255,255),
 Increment = 1,
 ValueName = "WS",
 Callback = function(Value)
  game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
 end    
})

PlayerTab:AddSlider({
 Name = "플레이어 점프",
 Min = 16,
 Max = 500,
 Default = 5,
 Color = Color3.fromRGB(255,255,255),
 Increment = 1,
 ValueName = "Height",
 Callback = function(Value)
  game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
 end    
})
  
local OtherTab = Window:MakeTab({
 Name = "어드민",
 Icon = "rbxassetid://4483345998",
 PremiumOnly = false
})

local Section = OtherTab:AddSection({
 Name = "어드민 GUI"
})

OtherTab:AddButton({
 Name = "어드민 GUI",
Callback = function()
loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()
  end 
})  

local Section = OtherTab:AddSection({
 Name = "스피드 핸드폰 PC"
})

OtherTab:AddButton({
 Name = "스피드 기본속도",
Callback = function()
getgenv().Enabled = true -- change to false then execute again to turn off
getgenv().Speed = 16 -- change speed to the number you want
loadstring(game:HttpGet("https://raw.githubusercontent.com/eclipsology/SimpleSpeed/main/SimpleSpeed.lua"))()
  end 
})  

OtherTab:AddButton({
 Name = "스피드 속도20",
Callback = function()
getgenv().Enabled = true -- change to false then execute again to turn off
getgenv().Speed = 20 -- change speed to the number you want
loadstring(game:HttpGet("https://raw.githubusercontent.com/eclipsology/SimpleSpeed/main/SimpleSpeed.lua"))()
  end 
})  

OtherTab:AddButton({
 Name = "스피드 속도30",
Callback = function()
getgenv().Enabled = true -- change to false then execute again to turn off
getgenv().Speed = 30 -- change speed to the number you want
loadstring(game:HttpGet("https://raw.githubusercontent.com/eclipsology/SimpleSpeed/main/SimpleSpeed.lua"))()
  end 
})  

OtherTab:AddButton({
 Name = "스피드 속도40",
Callback = function()
getgenv().Enabled = true -- change to false then execute again to turn off
getgenv().Speed = 40 -- change speed to the number you want
loadstring(game:HttpGet("https://raw.githubusercontent.com/eclipsology/SimpleSpeed/main/SimpleSpeed.lua"))()
  end 
})  

OtherTab:AddButton({
 Name = "스피드 속도50",
Callback = function()
getgenv().Enabled = true -- change to false then execute again to turn off
getgenv().Speed = 50 -- change speed to the number you want
loadstring(game:HttpGet("https://raw.githubusercontent.com/eclipsology/SimpleSpeed/main/SimpleSpeed.lua"))()
  end 
})  

OtherTab:AddButton({
 Name = "스피드 속도60",
Callback = function()
getgenv().Enabled = true -- change to false then execute again to turn off
getgenv().Speed = 60 -- change speed to the number you want
loadstring(game:HttpGet("https://raw.githubusercontent.com/eclipsology/SimpleSpeed/main/SimpleSpeed.lua"))()
  end 
})  

OtherTab:AddButton({
 Name = "스피드 속도70",
Callback = function()
getgenv().Enabled = true -- change to false then execute again to turn off
getgenv().Speed = 70 -- change speed to the number you want
loadstring(game:HttpGet("https://raw.githubusercontent.com/eclipsology/SimpleSpeed/main/SimpleSpeed.lua"))()
  end 
})  

OtherTab:AddButton({
 Name = "스피드 속도80",
Callback = function()
getgenv().Enabled = true -- change to false then execute again to turn off
getgenv().Speed = 80 -- change speed to the number you want
loadstring(game:HttpGet("https://raw.githubusercontent.com/eclipsology/SimpleSpeed/main/SimpleSpeed.lua"))()
  end 
})  

OtherTab:AddButton({
 Name = "스피드 속도90",
Callback = function()
getgenv().Enabled = true -- change to false then execute again to turn off
getgenv().Speed = 90 -- change speed to the number you want
loadstring(game:HttpGet("https://raw.githubusercontent.com/eclipsology/SimpleSpeed/main/SimpleSpeed.lua"))()
  end 
})  

OtherTab:AddButton({
 Name = "스피드 속도100",
Callback = function()
getgenv().Enabled = true -- change to false then execute again to turn off
getgenv().Speed = 100 -- change speed to the number you want
loadstring(game:HttpGet("https://raw.githubusercontent.com/eclipsology/SimpleSpeed/main/SimpleSpeed.lua"))()
  end 
})

local Section = OtherTab:AddSection({
 Name = "스핀 작동"
})

OtherTab:AddButton({
 Name = "스핀 속도10",
Callback = function()
 -- Made by JackMcJagger15

power = 10 -- change this to make it more or less powerful

game:GetService('RunService').Stepped:connect(function()
game.Players.LocalPlayer.Character.Head.CanCollide = false
game.Players.LocalPlayer.Character.UpperTorso.CanCollide = false
game.Players.LocalPlayer.Character.LowerTorso.CanCollide = false
game.Players.LocalPlayer.Character.HumanoidRootPart.CanCollide = false
end)
wait(.1)
local bambam = Instance.new("BodyThrust")
bambam.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
bambam.Force = Vector3.new(power,0,power)
bambam.Location = game.Players.LocalPlayer.Character.HumanoidRootPart.Position
end 
})

OtherTab:AddButton({
 Name = "스핀 속도20",
Callback = function()
 -- Made by JackMcJagger15

power = 20 -- change this to make it more or less powerful

game:GetService('RunService').Stepped:connect(function()
game.Players.LocalPlayer.Character.Head.CanCollide = false
game.Players.LocalPlayer.Character.UpperTorso.CanCollide = false
game.Players.LocalPlayer.Character.LowerTorso.CanCollide = false
game.Players.LocalPlayer.Character.HumanoidRootPart.CanCollide = false
end)
wait(.1)
local bambam = Instance.new("BodyThrust")
bambam.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
bambam.Force = Vector3.new(power,0,power)
bambam.Location = game.Players.LocalPlayer.Character.HumanoidRootPart.Position
end 
})

OtherTab:AddButton({
 Name = "스핀 속도30",
Callback = function()
 -- Made by JackMcJagger15

power = 30 -- change this to make it more or less powerful

game:GetService('RunService').Stepped:connect(function()
game.Players.LocalPlayer.Character.Head.CanCollide = false
game.Players.LocalPlayer.Character.UpperTorso.CanCollide = false
game.Players.LocalPlayer.Character.LowerTorso.CanCollide = false
game.Players.LocalPlayer.Character.HumanoidRootPart.CanCollide = false
end)
wait(.1)
local bambam = Instance.new("BodyThrust")
bambam.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
bambam.Force = Vector3.new(power,0,power)
bambam.Location = game.Players.LocalPlayer.Character.HumanoidRootPart.Position
end 
})

OtherTab:AddButton({
 Name = "스핀 속도40",
Callback = function()
 -- Made by JackMcJagger15

power = 40 -- change this to make it more or less powerful

game:GetService('RunService').Stepped:connect(function()
game.Players.LocalPlayer.Character.Head.CanCollide = false
game.Players.LocalPlayer.Character.UpperTorso.CanCollide = false
game.Players.LocalPlayer.Character.LowerTorso.CanCollide = false
game.Players.LocalPlayer.Character.HumanoidRootPart.CanCollide = false
end)
wait(.1)
local bambam = Instance.new("BodyThrust")
bambam.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
bambam.Force = Vector3.new(power,0,power)
bambam.Location = game.Players.LocalPlayer.Character.HumanoidRootPart.Position
end 
})

OtherTab:AddButton({
 Name = "스핀 속도50",
Callback = function()
 -- Made by JackMcJagger15

power = 50 -- change this to make it more or less powerful

game:GetService('RunService').Stepped:connect(function()
game.Players.LocalPlayer.Character.Head.CanCollide = false
game.Players.LocalPlayer.Character.UpperTorso.CanCollide = false
game.Players.LocalPlayer.Character.LowerTorso.CanCollide = false
game.Players.LocalPlayer.Character.HumanoidRootPart.CanCollide = false
end)
wait(.1)
local bambam = Instance.new("BodyThrust")
bambam.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
bambam.Force = Vector3.new(power,0,power)
bambam.Location = game.Players.LocalPlayer.Character.HumanoidRootPart.Position
end 
})

OtherTab:AddButton({
 Name = "스핀 속도100",
Callback = function()
 -- Made by JackMcJagger15

power = 100 -- change this to make it more or less powerful

game:GetService('RunService').Stepped:connect(function()
game.Players.LocalPlayer.Character.Head.CanCollide = false
game.Players.LocalPlayer.Character.UpperTorso.CanCollide = false
game.Players.LocalPlayer.Character.LowerTorso.CanCollide = false
game.Players.LocalPlayer.Character.HumanoidRootPart.CanCollide = false
end)
wait(.1)
local bambam = Instance.new("BodyThrust")
bambam.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
bambam.Force = Vector3.new(power,0,power)
bambam.Location = game.Players.LocalPlayer.Character.HumanoidRootPart.Position
end 
})




local OtherTab = Window:MakeTab({
 Name = "작동",
 Icon = "rbxassetid://4483345998",
 PremiumOnly = false
})

local Section = OtherTab:AddSection({
 Name = "작동"
})

OtherTab:AddButton({
 Name = "문삭제 하기",
 Callback = function()
       game.Workspace.Doors:Destroy()
   end    
})

OtherTab:AddButton({
 Name = "esp작동",
 Callback = function()
   loadstring(game:HttpGet("https://raw.githubusercontent.com/ekgj2beifh/OW-/main/%EC%97%AC%EB%8E%8C37"))()
   end    
})

local OtherTab = Window:MakeTab({
 Name = "보물선 만들기",
 Icon = "rbxassetid://4483345998",
 PremiumOnly = false
})

local Section = OtherTab:AddSection({
 Name = "보물선 만들기 GUI"
})

OtherTab:AddButton({
 Name = "오토팜",
Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/Rocks7hub/Rockshub/main/Build.boat"))()
  end 
})

local OtherTab = Window:MakeTab({
 Name = "팝잇 트레이닝",
 Icon = "rbxassetid://4483345998",
 PremiumOnly = false
})

local Section = OtherTab:AddSection({
 Name = "팝잇 트레이닝 GUI"
})

OtherTab:AddButton({
 Name = "팝잇 트레이닝 1",
Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/Farx11122/Dupess/main/SecondDupe"))()
  end 
})

local OtherTab = Window:MakeTab = PlayerTab = Window:MakeTab({
 Name = "테스트",
 Icon = "rbxassetid://4483345998",
 PremiumOnly = false
})

local Section = Tab:AddSection({
 Name = "테스트"
})


























