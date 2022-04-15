

	local placeId = game.PlaceId
	Magnet = true
	if placeId == 2753915549 then
		OldWorld = true
	elseif placeId == 4442272183 then
		NewWorld = true
	elseif placeId == 7449423635 then
		ThreeWorld = true
	end

    
    function CheckQuest()
        local Lv = game:GetService("Players").LocalPlayer.Data.Level.Value
        if OldWorld then
            if Lv == 1 or Lv <= 9 then
                Mon = "Bandit [Lv. 5]"
                NameMon = "Bandit"
                LvQuest = 1
                NameQuest = "BanditQuest1"
                CFrameMon = CFrame.new(1038.2711181640625, 24.537282943725586, 1550.2586669921875)
                CFrameQuest = CFrame.new(1059.8109130859375, 16.362747192382812, 1549.0882568359375)
            elseif Lv == 10 or Lv <= 14 then
                Mon = "Monkey [Lv. 14]"
                NameMon = "Monkey"
                LvQuest = 1
                NameQuest = "JungleQuest"
                CFrameMon = CFrame.new(-1443.7662353515625, 61.851966857910156, -47.555946350097656)
                CFrameQuest = CFrame.new(-1599.8194580078125, 36.852149963378906, 153.0706024169922)
                elseif Lv == 15 or Lv <= 29 then
                Mon = "Gorilla [Lv. 20]"
                NameMon = "Gorilla"
                LvQuest = 2
                NameQuest = "JungleQuest"
                CFrameMon = CFrame.new(-1134.61877, 40.4629173, -519.316956, 0.73422277, 1.82478495e-08, 0.678908646, 3.79294107e-08, 1, -6.7897922e-08, -0.678908646, 7.56028058e-08, 0.73422277)
                CFrameQuest = CFrame.new(-1599.8194580078125, 36.852149963378906, 153.0706024169922) 
                elseif Lv == 30 or Lv <= 39 then
                Mon = "Pirate [Lv. 35]"
                NameMon = "Pirate"
                LvQuest = 1
                NameQuest = "BuggyQuest1"
                CFrameMon = CFrame.new(-1122.23853, 44.7171288, 3860.55493, -0.344251066, 0, 0.938877702, 0, 1, -0, -0.938877583, 0, -0.344251096)
                CFrameQuest = CFrame.new(-1140.76709, 4.75206137, 3830.27881, -0.96363169, 1.72001009e-08, 0.267233938, 9.61536006e-09, 1, -2.96909715e-08, -0.267233938, -2.60416098e-08, -0.96363169) 
                elseif Lv == 40 or Lv <= 59 then
                Mon = "Brute [Lv. 45]"
                NameMon = "Brute"
                LvQuest = 2
                NameQuest = "BuggyQuest1"
                CFrameMon = CFrame.new(-1047.28137, 63.1395187, 4229.59033, 0.821381688, 0.383021981, 0.422641963, -0.422641963, 0.90629673, 4.45172191e-05, -0.383021981, -0.178662807, 0.90629673)
                CFrameQuest = CFrame.new(-1140.76709, 4.75206137, 3830.27881, -0.96363169, 1.72001009e-08, 0.267233938, 9.61536006e-09, 1, -2.96909715e-08, -0.267233938, -2.60416098e-08, -0.96363169)
                elseif Lv == 60 or Lv <= 74 then
                Mon = "Desert Bandit [Lv. 60]"
                NameMon = "Desert Bandit"
                LvQuest = 1
                NameQuest = "DesertQuest"
                CFrameMon = CFrame.new(935.940552, 20.9197369, 4561.29053, 0.999895632, 1.59735301e-08, -0.0144481836, -1.65728586e-08, 1, -4.13614671e-08, 0.0144481836, 4.15965964e-08, 0.999895632)
                CFrameQuest = CFrame.new(895.348999, 6.43847418, 4391.33203, -0.821520209, 6.88208956e-08, 0.570179403, 2.13266933e-08, 1, -8.99727155e-08, -0.570179403, -6.17543634e-08, -0.821520209)
        elseif Lv == 75 or Lv <= 89 then 
            Mon = "Desert Officer [Lv. 70]"
            NameMon = "Desert Officer"
            LvQuest = 2
            NameQuest = "DesertQuest"
            CFrameMon = CFrame.new(1547.1510009766, 14.452038764954, 4381.8002929688)
            CFrameQuest = CFrame.new(896.51721191406, 6.4384617805481, 4390.1494140625)
  
        end
    end
end


local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/zxciaz/VenyxUI/main/Reuploaded"))() --someone reuploaded it so I put it in place of the original back up so guy can get free credit.
local venyx = library.new("Real Hub Beta | BloxFruits", 5013109572)

-- themes
local themes = {
Background = Color3.fromRGB(24, 24, 24),
Glow = Color3.fromRGB(0, 0, 0),
Accent = Color3.fromRGB(10, 10, 10),
LightContrast = Color3.fromRGB(20, 20, 20),
DarkContrast = Color3.fromRGB(14, 14, 14),  
TextColor = Color3.fromRGB(255, 255, 255)
}

-- first page
local page = venyx:addPage("Main", 5012540623)
local section1 = page:addSection("Auto Farm")

    Weapon = {}
    for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
        if v:IsA"Tool" then
            table.insert(Weapon,v.Name)
    end
end

    local WE = section1:addDropdown("Select Weapon",Weapon, function(t)
    _G.SelectWeapon = t
end)

function Equip(ToolX)
    if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(ToolX) then
        getgenv().Tol = game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(ToolX)
        game.Players.LocalPlayer.Character.Humanoid:EquipTool(Tol)
    end
end

function click()
   game:GetService'VirtualUser':CaptureController()
   game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
end
 function TP(P)
   local Distance = (P.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude -- จุดที่จะไป Position Only
   local Speed = 300 -- ความเร็วของมึง
   tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear)
   tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = P})
   tween:Play()
 end

section1:addButton("Refersh Weapon", function()
    SelectWeapon:Clear()
	for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
		if v:IsA("Tool") then
			SelectWeapon:Add(v.Name)
		end
	end
end)

section1:addToggle("Bringmob", nil, function(t)
    _G.BringMob = t
end)

section1:addToggle("Auto Farm Level", nil, function(t)
    _G.AutoFarm = t
end)


section1:addToggle("Auto Superhuman", _G.Superhuman, function(t)
			_G.Superhuman = t
			while _G.Superhuman do wait()
				if _G.Superhuman then
					if game.Players.LocalPlayer.Backpack:FindFirstChild("Combat") or game.Players.LocalPlayer.Character:FindFirstChild("Combat") then
						local args = {
							[1] = "BuyBlackLeg"
						}
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
					end   
					if game.Players.LocalPlayer.Character:FindFirstChild("Superhuman") or game.Players.LocalPlayer.Backpack:FindFirstChild("Superhuman") then
						SelectToolWeapon = "Superhuman"
					end  
					if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") or game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") or game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") or game.Players.LocalPlayer.Character:FindFirstChild("Electro") or game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") or game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate") or game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") or game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") then
						if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value <= 299 then
							SelectToolWeapon = "Black Leg"
						end
						if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value <= 299 then
							SelectToolWeapon = "Electro"
						end
						if game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value <= 299 then
							SelectToolWeapon = "Fishman Karate"
						end
						if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value <= 299 then
							SelectToolWeapon = "Dragon Claw"
						end
						if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value >= 300 then
							local args = {
								[1] = "BuyElectro"
							}
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
						end
						if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 300 then
							local args = {
								[1] = "BuyElectro"
							}
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
						end
						if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value >= 300 then
							local args = {
								[1] = "BuyFishmanKarate"
							}
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
						end
						if game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value >= 300 then
							local args = {
								[1] = "BuyFishmanKarate"
							}
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
						end
						if game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value >= 300 then
							local args = {
								[1] = "BlackbeardReward",
								[2] = "DragonClaw",
								[3] = "1"
							}
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
							local args = {
								[1] = "BlackbeardReward",
								[2] = "DragonClaw",
								[3] = "2"
							}
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args)) 
						end
						if game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate").Level.Value >= 300 then
							local args = {
								[1] = "BlackbeardReward",
								[2] = "DragonClaw",
								[3] = "1"
							}
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
							local args = {
								[1] = "BlackbeardReward",
								[2] = "DragonClaw",
								[3] = "2"
							}
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args)) 
						end
						if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value >= 300 then
							local args = {
								[1] = "BuySuperhuman"
							}
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
						end
						if game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw").Level.Value >= 300 then
							local args = {
								[1] = "BuySuperhuman"
							}
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
						end 
					end
				end
			end
		end)

section1:addButton("Redeem All Code",function()
   	function UseCode(Text)
        game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer(Text)
    end
    UseCode("UPD16")
    UseCode("2BILLION")
    UseCode("UPD15")
    UseCode("FUDD10")
    UseCode("BIGNEWS")
    UseCode("THEGREATACE")
    UseCode("SUB2GAMERROBOT_EXP1")
    UseCode("StrawHatMaine")
    UseCode("Sub2OfficialNoobie")
    UseCode("SUB2NOOBMASTER123")
    UseCode("Sub2Daigrock")
    UseCode("Axiore")
    UseCode("TantaiGaming")
    UseCode("STRAWHATMAINE") 
end)


local page = venyx:addPage("Auto Stats", 7040410130)
local section1 = page:addSection("Stats")

section1:addToggle("Melee", nil, function(t)
_G.Melee = t
while _G.Melee do wait(.1)
pcall(function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Melee",Point)
end)
end
end)

section1:addToggle("Defense", nil, function(t)
_G.Defense = t
while _G.Defense do wait(.1)
pcall(function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Defense",Point)
end)
end
end)

section1:addToggle("Sword", nil, function(t)
_G.Sword = t
while _G.Sword do wait(.1)
pcall(function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Sword",Point)
end)
end
end)

section1:addToggle("Gun", nil, function(t)
_G.Gun = t
while _G.Gun do wait(.1)
pcall(function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Gun",Point)
end)
end
end)

section1:addToggle("Fruit", nil, function(t)
_G.Fruit = t
while _G.Fruit do wait(.1)
pcall(function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Demon Fruit",Point)
end)
end
end)

section1:addSlider("Point", 0, 1, 100, function(x)
Point = x
end)


    spawn(function()
    while wait() do
        if _G.BringMob then
            pcall(function()
            CheckQuest()
       for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
for x,y in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
if v.Name == Mon then
    if y.Name == Mon then
   v.HumanoidRootPart.CFrame = y.HumanoidRootPart.CFrame
   v.HumanoidRootPart.Size = Vector3.new(60,60,60)
   y.HumanoidRootPart.Size = Vector3.new(60,60,60)
   v.HumanoidRootPart.Transparency = 1
   v.HumanoidRootPart.CanCollide = false
   y.HumanoidRootPart.CanCollide = false
   v.Humanoid.WalkSpeed = 0
   y.Humanoid.WalkSpeed = 0
   v.Humanoid.JumpPower = 0
   y.Humanoid.JumpPower = 0
   if sethiddenproperty then
     sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
end
end
end
end
end
end)
end
end
end)


spawn(function()
    while wait() do
        if _G.AutoFarm then
            pcall(function()
            CheckQuest()
    if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
    TP(CFrameQuest)
    if (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5 then
    wait(.1)
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,LvQuest)
    end
    elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
        if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text,NameMon) then
            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                if v.Name == Mon and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid")   then
                    if v.Humanoid.Health > 0 then
                    repeat wait()
                        click()
                        Equip(_G.SelectWeapon)
                        HealthMin = v.Humanoid.MaxHealth * 90 / 100
                        Magma = (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
                        if Magma <= 230 then
                            if v.Humanoid.Health > HealthMin then
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0,3,15)
                                else
                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0,3,15)
                            end
                        end
                            if v.Humanoid.Health > HealthMin then
                        Distance = (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude 
                        Speed = 300 
                        tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear)
                        tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0,3,15)})
                        tween:Play() 
                        else
                        Distance = (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude 
                        Speed = 300 
                        tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear)
                        tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0,3,15)})
                        tween:Play()
                            end
                        v.HumanoidRootPart.Size = Vector3.new(60,60,60)
                        v.HumanoidRootPart.CanCaillde = false
                    until _G.AutoFarm == false or v.Humanoid.Health <= 0
                    else
                        TP(CFrameMon)
                    end
                    if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text,NameMon) then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                    end
                    if game.Players.LocalPlayer.Character.Humanoid.Health <= 0 then
                        _G.AutoFarm = false
                        wait(3)
                        _G.AutoFarm = true
                        end
                end
                end
        end
        end
       end)
end
end
end)


spawn(function()
    game:GetService("RunService").Heartbeat:Connect(function()
        if _G.AutoFarm then
        if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Humanoid") then
            setfflag("HumanoidParallelRemoveNoPhysics", "False")
            setfflag("HumanoidParallelRemoveNoPhysicsNoSimulate2", "False")
            game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
            end
        end
    end)
end)


function TP2(P1)
	Distance = (P1.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
	if Distance < 1000 then
		Speed = 400
	elseif Distance >= 1000 then
		Speed = 250
	end
    game:GetService("TweenService"):Create(
        game.Players.LocalPlayer.Character.HumanoidRootPart,
        TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
        {CFrame = P1}
    ):Play()
    Clip = true
    wait(Distance/Speed)
    Clip = false
end


local page = venyx:addPage("Teleport", 7044226690)
local section4 = page:addSection("island")

if NewWorld then
    section4:addButton("Dock",function()
        TP2(CFrame.new(82.9490662, 18.0710983, 2834.98779))
    end)
    section4:addButton("Kingdom of Rose",function()
        TP2(CFrame.new(-394.983521, 118.503128, 1245.8446))
    end)
    section4:addButton("Mansion",function()
        TP2(CFrame.new(-390.096313, 331.886475, 673.464966))
    end)
    section4:addButton("Flamingo Room",function()
        TP2(CFrame.new(2302.19019, 15.1778421, 663.811035))
    end)
    section4:addButton("Green Zone",function()
        TP2(CFrame.new(-2372.14697, 72.9919434, -3166.51416))
    end)
    section4:addButton("Cafe",function()
        TP2(CFrame.new(-385.250916, 73.0458984, 297.388397))
    end)
    section4:addButton("Factroy",function()
        TP2(CFrame.new(430.42569, 210.019623, -432.504791))
    end)
    section4:addButton("Colosseum",function()
        TP2(CFrame.new(-1836.58191, 44.5890656, 1360.30652))
    end)
    section4:addButton("GraveIsland",function()
        TP2(CFrame.new(-5411.47607, 48.8234024, -721.272522))
    end)
    section4:addButton("Snow Mountain",function()
        TP2(CFrame.new(511.825226, 401.765198, -5380.396))
    end)
    section4:addButton("Cold Island",function()
        TP2(CFrame.new(-6026.96484, 14.7461271, -5071.96338))
    end)
    section4:addButton("Hot Island",function()
        TP2(CFrame.new(-5478.39209, 15.9775667, -5246.9126))
    end)
    section4:addButton("Cursed Ship",function()
        TP2(CFrame.new(902.059143, 124.752518, 33071.8125))
    end)
    section4:addButton("IceCastle",function()
        TP2(CFrame.new(5400.40381, 28.21698, -6236.99219))
    end)
    section4:addButton("Forgotten Island",function()
        TP2(CFrame.new(-3043.31543, 238.881271, -10191.5791))
    end)
    section4:addButton("Usoapp Island",function()
        TP2(CFrame.new(4748.78857, 8.35370827, 2849.57959))
    end)
    section4:addButton("Minisky Island",function()
        TP2(CFrame.new(-260.358917, 49325.7031, -35259.3008))
    end)
end
if OldWorld then
    section4:addButton("Pirates Start ",function()
        TP2(CFrame.new(1071.2832, 16.3085976, 1426.86792))
    end)
    section4:addButton("Marine Start",function()
        TP2(CFrame.new(-2573.3374, 6.88881969, 2046.99817))
    end)
    section4:addButton("Middle Town",function()
        TP2(CFrame.new(-655.824158, 7.88708115, 1436.67908))
    end)
    section4:addButton("Jungle",function()
        TP2(CFrame.new(-1249.77222, 11.8870859, 341.356476))
    end)
    section4:addButton("Pirate Village",function()
        TP2(CFrame.new(-1122.34998, 4.78708982, 3855.91992))
    end)
    section4:addButton("Desert",function()
        TP2(CFrame.new(1094.14587, 6.47350502, 4192.88721))
    end)
    section4:addButton("Frozen Village",function()
        TP2(CFrame.new(1198.00928, 27.0074959, -1211.73376))
    end)
    section4:addButton("MarineFord",function()
        TP2(CFrame.new(-4505.375, 20.687294, 4260.55908))
    end)
    section4:addButton("Colosseum",function()
        TP2(CFrame.new(-1428.35474, 7.38933945, -3014.37305))
    end)
    section4:addButton("Sky island 1 ",function()
        TP2(CFrame.new(-4970.21875, 717.707275, -2622.35449))
    end)
    section4:addButton("Sky island 2 ",function()
        TP2(CFrame.new(-4813.0249, 903.708557, -1912.69055))
    end)
    section4:addButton("Sky island 3 ",function()
        TP2(CFrame.new(-7952.31006, 5545.52832, -320.704956))
    end)
    section4:addButton("Sky island 4 ",function()
        TP2(CFrame.new(-7793.43896, 5607.22168, -2016.58362))
    end)
    section4:addButton("Prison",function()
        TP2(CFrame.new(4854.16455, 5.68742752, 740.194641))
    end)
    section4:addButton("Magma Village",function()
        TP2(CFrame.new(-5231.75879, 8.61593437, 8467.87695))
    end)
    section4:addButton("UndeyWater City",function()
        TP2(CFrame.new(61163.8516, 11.7796879, 1819.78418))
    end)
    section4:addButton("Fountain City",function()
        TP2(CFrame.new(5132.7124, 4.53632832, 4037.8562))
    end)
    section4:addButton("House Cyborg's",function()
        TP2(CFrame.new(6262.72559, 71.3003616, 3998.23047))
    end)
    section4:addButton("Shank's Room",function()
        TP2(CFrame.new(-1442.16553, 29.8788261, -28.3547478))
    end)
    section4:addButton("Mob Island",function()
        TP2(CFrame.new(-2850.20068, 7.39224768, 5354.99268))
    end)
end   
if ThreeWorld then
    section4:addButton("Port Towen",function()
        TP2(CFrame.new(-610.309692, 57.8323097, 6436.33594))
    end)
    section4:addButton("Hydra Island",function()
        TP2(CFrame.new(5229.99561, 603.916565, 345.154022))
    end)
    section4:addButton("Great Tree",function()
        TP2(CFrame.new(2174.94873, 28.7312393, -6728.83154))
    end)
    section4:addButton("Castle on the Sea",function()
        TP2(CFrame.new(-5477.62842, 313.794739, -2808.4585))
    end)
    section4:addButton("Floating Turtle",function()
        TP2(CFrame.new(-10919.2998, 331.788452, -8637.57227))
    end)
    section4:addButton("Mansion",function()
        TP2(CFrame.new(-12553.8125, 332.403961, -7621.91748))
    end)
    section4:addButton("Secret Temple",function()
        TP2(CFrame.new(5217.35693, 6.56511116, 1100.88159))
    end)
    section4:addButton("Friendly Arena",function()
        TP2(CFrame.new(5220.28955, 72.8193436, -1450.86304))
    end)
    section4:addButton("Beautiful Pirate Domain",function()
        TP2(CFrame.new(5310.8095703125, 21.594484329224, 129.39053344727))
    end)
    section4:addButton("Teler Park",function()
        TP2(CFrame.new(-9512.3623046875, 142.13258361816, 5548.845703125))
    end)
    section4:addButton("Peanut Island",function()
        TP2(CFrame.new(-2062.67773, 38.1294556, -10287.752, -0.258864403, 0, -0.965913653, 0, 1, 0, 0.965913653, 0, -0.258864403))
    end)
    section4:addButton("Ice Cream Island",function()
        TP2(CFrame.new(-840.188477, 65.8452759, -10877.3789, -0.573598981, 0, 0.819136262, 0, 1, 0, -0.819136262, 0, -0.573598981))
    end)
end



local page = venyx:addPage("Game", 7044233235)
local section1 = page:addSection("Game")

section1:addToggle("Esp Players", nil, function(Value)
    PlayerESP = Value
	while PlayerESP do wait()
		UpdatePlayer()
	end
end)

section1:addToggle("Esp Fruit", nil, function(Value)
    DevilESP = Value
	while DevilESP do wait()
		UpdateDevilFruit()
	end
end)

Number = math.random(1,1000000)

function UpdateChest()
	for i,v in pairs(game.Workspace:GetChildren()) do
		pcall(function()
			if v.Name == "Chest1" or v.Name == "Chest2" or v.Name == "Chest3" then
				if ChestESP then
					if (v.Name == "Chest1" or v.Name == "Chest2" or v.Name == "Chest3") and (v.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 60000 then
						if not v:FindFirstChild("ChestESP"..Number) then
							local Bb = Instance.new("BillboardGui", v)
							Bb.Name = "ChestESP"..Number
							Bb.ExtentsOffset = Vector3.new(0, 1, 0)
							Bb.Size = UDim2.new(1, 200, 1, 30)
							Bb.Adornee = v
							Bb.AlwaysOnTop = true
							local Textlb = Instance.new("TextLabel", Bb)
							Textlb.Font = "GothamBold"
							Textlb.FontSize = "Size14"
							Textlb.Size = UDim2.new(1,0,1,0)
							Textlb.BackgroundTransparency = 1
							Textlb.TextStrokeTransparency = 0.5
							if v.Name == "Chest1" then
								Textlb.TextColor3 = Color3.fromRGB(174, 123, 47)
								Textlb.Text = "Bronze Chest".."
"..math.round((v.Position - game:GetService('Players').LocalPlayer.Character.HumanoidRootPart.Position).Magnitude/3).." m."
							end
							if v.Name == "Chest2" then
								Textlb.TextColor3 = Color3.fromRGB(255, 255, 127)
								Textlb.Text = "Gold Chest".."
"..math.round((v.Position - game:GetService('Players').LocalPlayer.Character.HumanoidRootPart.Position).Magnitude/3).." m."
							end
							if v.Name == "Chest3" then
								Textlb.Text = "Diamond Chest".."
"..math.round((v.Position - game:GetService('Players').LocalPlayer.Character.HumanoidRootPart.Position).Magnitude/3).." m."
								Textlb.TextColor3 = Color3.fromRGB(5, 243, 255)
							end
						else
							v["ChestESP"..Number].TextLabel.Text = v.Name.."
"..math.round((v.Position - game:GetService('Players').LocalPlayer.Character.HumanoidRootPart.Position).Magnitude/3).." m."
						end
					end
				else
					if v:FindFirstChild("ChestESP"..Number) then
						v:FindFirstChild("ChestESP"..Number):Destroy()
					end
				end
			end
		end)
	end
end

function UpdatePlayer()
	for i,v in pairs(game:GetService("Players"):GetChildren()) do
		pcall(function()
			if v.Character then
				if PlayerESP then
					if v.Character.Head and not v.Character.Head:FindFirstChild("PlayerESP"..Number) then
						local Bb = Instance.new("BillboardGui", v.Character.Head)
						Bb.Name = "PlayerESP"..Number
						Bb.ExtentsOffset = Vector3.new(0, 1, 0)
						Bb.Size = UDim2.new(1, 200, 1, 30)
						Bb.Adornee = v.Character.Head
						Bb.AlwaysOnTop = true
						local Textlb = Instance.new("TextLabel", Bb)
						Textlb.Font = "GothamBold"
						Textlb.FontSize = "Size14"
						Textlb.Text = v.Name.."
"..math.round((v.Character.Head.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude/3).." m."
						Textlb.Size = UDim2.new(1,0,1,0)
						Textlb.BackgroundTransparency = 1
						Textlb.TextStrokeTransparency = 0.5
						if v.Team == game:GetService("Players").LocalPlayer.Team then
							Textlb.TextColor3 = Color3.new(0, 255, 0)
						else
							Textlb.TextColor3 = Color3.new(0, 0, 204)
						end
					else
						v.Character.Head["PlayerESP"..Number].TextLabel.Text = v.Name.."
"..math.round((v.Character.Head.Position - game:GetService('Players').LocalPlayer.Character.HumanoidRootPart.Position).Magnitude/3).." m."
					end
				else
					if v.Character.Head:FindFirstChild("PlayerESP"..Number) then
						v.Character.Head:FindFirstChild("PlayerESP"..Number):Destroy()
					end
				end
			end
		end)
	end
end

function UpdateDevilFruit()
	for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
		pcall(function()
			if string.find(v.Name, "Fruit") then
				if DevilESP then
					if string.find(v.Name, "Fruit") then
						if not v.Handle:FindFirstChild("DevilESP"..Number) then
							local Bb = Instance.new("BillboardGui", v.Handle)
							Bb.Name = "DevilESP"..Number
							Bb.ExtentsOffset = Vector3.new(0, 1, 0)
							Bb.Size = UDim2.new(1, 200, 1, 30)
							Bb.Adornee = v.Handle
							Bb.AlwaysOnTop = true
							local Textlb = Instance.new("TextLabel", Bb)
							Textlb.Font = "GothamBold"
							Textlb.FontSize = "Size14"
							Textlb.Size = UDim2.new(1,0,1,0)
							Textlb.BackgroundTransparency = 1
							Textlb.TextStrokeTransparency = 0.5
							Textlb.Text = v.Name.."
"..math.round((v.Handle.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude/3).." m."
							Textlb.TextColor3 = Color3.new(255, 255, 255)
						else
							v.Handle["DevilESP"..Number].TextLabel.Text = v.Name.."
"..math.round((v.Handle.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude/3).." m."
						end
					end
				else
					if v.Handle:FindFirstChild("DevilESP"..Number) then
						v.Handle:FindFirstChild("DevilESP"..Number):Destroy()
					end
				end
			end
		end)
	end
end

function UpdateFlower()
	for i,v in pairs(game.Workspace:GetChildren()) do
		pcall(function()
			if v.Name == "Flower2" or v.Name == "Flower1" then
				if FlowerESP then
					if not v:FindFirstChild("FindFlower"..Number) then
						local bill = Instance.new("BillboardGui",v)
						bill.Name = "FindFlower"..Number
						bill.ExtentsOffset = Vector3.new(0, 1, 0)
						bill.Size = UDim2.new(1,200,1,30)
						bill.Adornee = v
						bill.AlwaysOnTop = true
						local name = Instance.new("TextLabel",bill)
						name.Font = "GothamBold"
						name.FontSize = "Size14"
						name.TextWrapped = true
						name.Size = UDim2.new(1,0,1,0)
						name.TextYAlignment = "Top"
						name.BackgroundTransparency = 1
						name.TextStrokeTransparency = 0.5
						name.TextColor3 = Color3.fromRGB(248, 41, 41)
						if v.Name == "Flower1" then
							name.Text = ("Blue Flower".."
"..math.round((v.Position - game:GetService('Players').LocalPlayer.Character.HumanoidRootPart.Position).Magnitude/3).." m.")
							name.TextColor3 = Color3.fromRGB(28, 126, 255)
						end
						if v.Name == "Flower2" then
							name.Text = ("Red Flower".."
"..math.round((v.Position - game:GetService('Players').LocalPlayer.Character.HumanoidRootPart.Position).Magnitude/3).." m.")
							name.TextColor3 = Color3.fromRGB(248, 41, 41)
						end
					else
						v["FindFlower"..Number].TextLabel.Text = (v.Name.."
"..math.round((v.Position - game:GetService('Players').LocalPlayer.Character.HumanoidRootPart.Position).Magnitude/3).." m.")
					end
				else
					if v:FindFirstChild("FindFlower"..Number) then
						v:FindFirstChild("FindFlower"..Number):Destroy()
					end
				end
			end
		end)
	end
end

function UpdateFruits()
	for i,v in pairs(game.Workspace:GetChildren()) do
	    pcall(function()
			if v.Name == "Banana" or v.Name == "Apple" or v.Name == "Pineapple" then
				if FindFruits then
					if not v:FindFirstChild("FindFruit"..Number) then
						local bill = Instance.new("BillboardGui",v)
						bill.Name = "FindFruit"..Number
						bill.ExtentsOffset = Vector3.new(0, 1, 0)
						bill.Size = UDim2.new(1,200,1,30)
						bill.Adornee = v
						bill.AlwaysOnTop = true
						local name = Instance.new("TextLabel",bill)
						name.Font = "GothamBold"
						name.FontSize = "Size14"
						name.TextWrapped = true
						name.Size = UDim2.new(1,0,1,0)
						name.TextYAlignment = "Top"
						name.BackgroundTransparency = 1
						name.TextStrokeTransparency = 0.5
						if v.Name == "Banana" then
							name.Text = ("Banana".."
"..math.round((v.Handle.Position - game:GetService('Players').LocalPlayer.Character.HumanoidRootPart.Position).Magnitude/3).." m.")
							name.TextColor3 = Color3.fromRGB(255, 255, 0)
						end
						if v.Name == "Apple" then
							name.Text = ("Apple".."
"..math.round((v.Handle.Position - game:GetService('Players').LocalPlayer.Character.HumanoidRootPart.Position).Magnitude/3).." m.")
							name.TextColor3 = Color3.fromRGB(208, 0, 0)
						end
						if v.Name == "PineApple" then
						    name.Text = ("PineApple".."
"..math.round((v.Handle.Position - game:GetService('Players').LocalPlayer.Character.HumanoidRootPart.Position).Magnitude/3).." m.")
							name.TextColor3 = Color3.fromRGB(255, 128, 0)
						end
					else
						v["FindFruit"..Number].TextLabel.Text = (v.Name.."
"..math.round((v.Handel.Position - game:GetService('Players').LocalPlayer.Character.HumanoidRootPart.Position).Magnitude/3).." m.")
					end
				else
					if v:FindFirstChild("FindFruit"..Number) then
						v:FindFirstChild("FindFruit"..Number):Destroy()
					end
				end
			end
		end)
	end
end

section1:addButton("Rejoin",function()
game:GetService("TeleportService"):Teleport(game.PlaceId, game:GetService("Players").localPlayer)
end)
section1:addSlider("WalkSpeed", 0, 25, 1000, function(g)
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = g
end)

section1:addSlider("Jumppower", 0, 25, 1000, function(exe)
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = exe
end)


local section22 = page:addSection("Team")

section22:addButton("Join Team Pirates",function()
    local args = {
        [1] = "SetTeam",
        [2] = "Pirates"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args)) 
    local args = {
        [1] = "BartiloQuestProgress"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)

section22:addButton("Join Team Marines",function()
    local args = {
        [1] = "SetTeam",
        [2] = "Marines"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    local args = {
        [1] = "BartiloQuestProgress"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
end)


local section2 = page:addSection("Gui")
section2:addButton("Fruit Shop",function()
    local args = {
        [1] = "GetFruits"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    game.Players.localPlayer.PlayerGui.Main.FruitShop.Visible = true
end)

section2:addButton("Inventory",function()
	game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("getInventoryWeapons")
    game.Players.localPlayer.PlayerGui.Main.Inventory.Visible = true
end)

section2:addButton("Fruit Inventory",function()
	local args = {
		[1] = "getInventoryFruits"
	}
	
	game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("getInventoryFruits")
	game:GetService("Players").LocalPlayer.PlayerGui.Main.FruitInventory.Visible = true
end)

section2:addButton("Color Haki",function()
    game.Players.localPlayer.PlayerGui.Main.Colors.Visible = true
end)


section2:addButton("Title Name",function()
    local args = {
        [1] = "getTitles"
    }
    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    game.Players.localPlayer.PlayerGui.Main.Titles.Visible = true
end)

local Fuck = page:addSection("game")

Fuck:addToggle("Inf Energy", nil, function(value)
    InfinitsEnergy = value
    originalstam = LocalPlayer.Character.Energy.Value
end)

Fuck:addToggle("No Dodge Cooldown", nil, function(Value)
    nododgecool = Value
    NoDodgeCool()
end)

Fuck:addToggle("Inf Ability", nil, function(vu)
	InfAbility = vu
end)

spawn(function()
	while wait() do
		if InfAbility then
			InfAb()
		end
	end
end)

function InfAb()
	if InfAbility then
		if not game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("Agility") then
			local inf = Instance.new("ParticleEmitter")
			inf.Acceleration = Vector3.new(0,0,0)
			inf.Archivable = true
			inf.Drag = 20
			inf.EmissionDirection = Enum.NormalId.Top
			inf.Enabled = true
			inf.Lifetime = NumberRange.new(0.2,0.2)
			inf.LightInfluence = 0
			inf.LockedToPart = true
			inf.Name = "Agility"
			inf.Rate = 500
			local numberKeypoints2 = {
				NumberSequenceKeypoint.new(0, 0);  -- At t=0, size of 0
				NumberSequenceKeypoint.new(1, 4); -- At t=1, size of 10
			}

			inf.Size = NumberSequence.new(numberKeypoints2)
			inf.RotSpeed = NumberRange.new(999, 9999)
			inf.Rotation = NumberRange.new(0, 0)
			inf.Speed = NumberRange.new(30, 30)
			inf.SpreadAngle = Vector2.new(360,360)
			inf.Texture = "rbxassetid://243098098"
			inf.VelocityInheritance = 0
			inf.ZOffset = 2
			inf.Transparency = NumberSequence.new(0)
			inf.Color = ColorSequence.new(Color3.fromRGB(0, 255, 255),Color3.fromRGB(0, 255, 255))
			inf.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
		end
	else
		if game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("Agility") then
			game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("Agility"):Destroy()
		end
	end
end


Fuck:addButton("FPS Boost",function()
    local decalsyeeted = true
    local g = game
    local w = g.Workspace
    local l = g.Lighting
    local t = w.Terrain
    t.WaterWaveSize = 0
    t.WaterWaveSpeed = 0
    t.WaterReflectance = 0
    t.WaterTransparency = 0
    l.GlobalShadows = false
    l.FogEnd = 9e9
    l.Brightness = 0
    settings().Rendering.QualityLevel = "Level01"
    for i, v in pairs(g:GetDescendants()) do
        if v:IsA("Part") or v:IsA("Union") or v:IsA("CornerWedgePart") or v:IsA("TrussPart") then 
            v.Material = "Plastic"
            v.Reflectance = 0
        elseif v:IsA("Decal") or v:IsA("Texture") and decalsyeeted then
            v.Transparency = 1
        elseif v:IsA("ParticleEmitter") or v:IsA("Trail") then
            v.Lifetime = NumberRange.new(0)
        elseif v:IsA("Explosion") then
            v.BlastPressure = 1
            v.BlastRadius = 1
        elseif v:IsA("Fire") or v:IsA("SpotLight") or v:IsA("Smoke") or v:IsA("Sparkles") then
            v.Enabled = false
        elseif v:IsA("MeshPart") then
            v.Material = "Plastic"
            v.Reflectance = 0
            v.TextureID = 10385902758728957
        end
    end
    for i, e in pairs(l:GetChildren()) do
        if e:IsA("BlurEffect") or e:IsA("SunRaysEffect") or e:IsA("ColorCorrectionEffect") or e:IsA("BloomEffect") or e:IsA("DepthOfFieldEffect") then
            e.Enabled = false
        end
    end
end)

Fuck:addButton("Remove Lava",function()
    for i,v in pairs(game.Workspace:GetDescendants()) do
        if v.Name == "Lava" then   
            v:Destroy()
        end
    end
    for i,v in pairs(game.ReplicatedStorage:GetDescendants()) do
        if v.Name == "Lava" then   
            v:Destroy()
        end
    end
end)

local page = venyx:addPage("Setting", 7040347038)
local section1 = page:addSection("Setting")

section1:addToggle("Auto Attack", true, function(annn)

end)

local ui = page:addSection("Ui Setting")

ui:addKeybind("Toggle Keybind", Enum.KeyCode.RightControl, function()
print("Activated Keybind")
venyx:toggle()
end, function()
print("Changed Keybind")
end)

for theme, color in pairs(themes) do
ui:addColorPicker(theme, color, function(color3)
Venyx:setTheme(theme, color3)
end)
end


