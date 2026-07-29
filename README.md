local UIS,TS,p=game:GetService("UserInputService"),game:GetService("TweenService"),game.Players.LocalPlayer
local sg=Instance.new("ScreenGui",p.PlayerGui) sg.Name="OnyxHub" sg.ResetOnSpawn=false
local m=Instance.new("Frame",sg) m.Size=UDim2.new(0,360,0,320) m.Position=UDim2.new(.5,-180,.5,-160) m.BackgroundColor3=Color3.fromRGB(18,20,28) m.Active=true
Instance.new("UICorner",m).CornerRadius=UDim.new(0,14)

local function btn(t,c,y,e)
 local b=Instance.new("TextButton",m) b.Size=UDim2.new(0,320,0,48) b.Position=UDim2.new(0,20,0,y) b.BackgroundColor3=c b.Text=e.."  "..t b.TextColor3=Color3.new(1,1,1) b.TextSize=15 b.Font=Enum.Font.GothamBold
 Instance.new("UICorner",b).CornerRadius=UDim.new(0,10) return b
end

local close=Instance.new("TextButton",m) close.Size=UDim2.new(0,32,0,32) close.Position=UDim2.new(1,-38,0,8) close.BackgroundTransparency=1 close.Text="X" close.TextColor3=Color3.fromRGB(200,200,200) close.TextSize=20 close.Font=Enum.Font.GothamBold
local logo=Instance.new("Frame",m) logo.Size=UDim2.new(0,38,0,38) logo.Position=UDim2.new(0,20,0,20) logo.BackgroundColor3=Color3.fromRGB(220,40,40)
Instance.new("UICorner",logo).CornerRadius=UDim.new(0,9)
local lt=Instance.new("TextLabel",logo) lt.Size=UDim2.new(1,0,1,0) lt.BackgroundTransparency=1 lt.Text="O" lt.TextColor3=Color3.new(1,1,1) lt.TextSize=22 lt.Font=Enum.Font.GothamBold
local title=Instance.new("TextLabel",m) title.Size=UDim2.new(0,200,0,26) title.Position=UDim2.new(0,70,0,20) title.BackgroundTransparency=1 title.Text="OnyxHub" title.TextColor3=Color3.new(1,1,1) title.TextSize=24 title.Font=Enum.Font.GothamBold title.TextXAlignment=Enum.TextXAlignment.Left
local sub=Instance.new("TextLabel",m) sub.Size=UDim2.new(0,240,0,18) sub.Position=UDim2.new(0,70,0,46) sub.BackgroundTransparency=1 sub.Text="Free OnyxHub Verification" sub.TextColor3=Color3.fromRGB(80,140,255) sub.TextSize=13 sub.Font=Enum.Font.Gotham sub.TextXAlignment=Enum.TextXAlignment.Left

local g=btn("UNIRSE AL GRUPO (SCRIPT AQUÃ)",Color3.fromRGB(35,50,85),90,"ðŸ”¥") g.TextColor3=Color3.fromRGB(255,200,50)
local d=btn("Unirse al Servidor de Discord",Color3.fromRGB(40,55,90),150,"ðŸ’¬")
local y=btn("SuscrÃ­bete a mi canal de YouTube",Color3.fromRGB(220,30,30),210,"ðŸ“º")

local f=Instance.new("TextButton",sg) f.Size=UDim2.new(0,52,0,52) f.Position=UDim2.new(1,-70,.5,-26) f.BackgroundColor3=Color3.fromRGB(220,40,40) f.Text="O" f.TextColor3=Color3.new(1,1,1) f.TextSize=24 f.Font=Enum.Font.GothamBold f.Visible=false
Instance.new("UICorner",f).CornerRadius=UDim.new(1,0)

local n=Instance.new("TextLabel",sg) n.Size=UDim2.new(0,180,0,36) n.Position=UDim2.new(.5,-90,.85,0) n.BackgroundColor3=Color3.fromRGB(30,200,80) n.Text="Link copiado!" n.TextColor3=Color3.new(1,1,1) n.TextSize=16 n.Font=Enum.Font.GothamBold n.Visible=false
Instance.new("UICorner",n).CornerRadius=UDim.new(0,8)

local function copy(l) setclipboard(l) n.Visible=true n.BackgroundTransparency=0 n.TextTransparency=0 task.delay(1.6,function() TS:Create(n,TweenInfo.new(.3),{BackgroundTransparency=1,TextTransparency=1}):Play() task.wait(.3) n.Visible=false end) end

close.MouseButton1Click:Connect(function() m.Visible=false f.Visible=true end)
f.MouseButton1Click:Connect(function() m.Visible=true f.Visible=false end)
g.MouseButton1Click:Connect(function() copy("https://roblox.com.ug/communities/8532004476/") end)
d.MouseButton1Click:Connect(function() copy("https://discord.gg/FHrsUBYNjb") end)
y.MouseButton1Click:Connect(function() copy("https://www.youtube.com/@vinay-n1q8k") end)

local drag,start,pos
m.InputBegan:Connect(function(i) if i.UserInputType==Enum.UserInputType.MouseButton1 or i.UserInputType==Enum.UserInputType.Touch then drag=true start=i.Position pos=m.Position end end)
m.InputEnded:Connect(function(i) if i.UserInputType==Enum.UserInputType.MouseButton1 or i.UserInputType==Enum.UserInputType.Touch then drag=false end end)
UIS.InputChanged:Connect(function(i) if drag and (i.UserInputType==Enum.UserInputType.MouseMovement or i.UserInputType==Enum.UserInputType.Touch) then local d=i.Position-start m.Position=UDim2.new(pos.X.Scale,pos.X.Offset+d.X,pos.Y.Scale,pos.Y.Offset+d.Y) end end

Script 
