-- init
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/LifeIsHardZ/Veneyx/main/test"))()
local venyx = library.new("Sun Hub", 5013109572)

-- services
local input = game:GetService("UserInputService")
local run = game:GetService("RunService")
local tween = game:GetService("TweenService")
local tweeninfo = TweenInfo.new

-- additional
local utility = {}


-- themes
local themes = {
    Background = Color3.fromRGB(24, 24, 24),
    Glow = Color3.fromRGB(255, 0, 0),
    Accent = Color3.fromRGB(10, 10, 10),
    LightContrast = Color3.fromRGB(20, 20, 20),
    DarkContrast = Color3.fromRGB(0, 0, 0),  
    TextColor = Color3.fromRGB(255, 0, 0)
}

-- first page
local page = venyx:addPage("Main", 5012544693)
local section1 = page:addSection("Auto Farm")

if _G.Team == "Pirate" then
	for i,v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton.MouseButton1Click)) do
		v.Function()
	end
elseif _G.Team == "Marine" then
	for i,v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Marines.Frame.ViewportFrame.TextButton.MouseButton1Click)) do
		v.Function()
	end
else
	for i,v in pairs(getconnections(game:GetService("Players").LocalPlayer.PlayerGui.Main.ChooseTeam.Container.Pirates.Frame.ViewportFrame.TextButton.MouseButton1Click)) do
		v.Function()
	end
end


--------------------------------Check placeId
Old_World = false
New_World = false
SeaThird_World = false
local placeId = game.PlaceId
if placeId == 2753915549 then
    Old_World = true
elseif placeId == 4442272183 then
    New_World = true
elseif placeId == 7449423635 then
    SeaThird_World = true    
end
--------------------function farm 
function CheckLevel()
    local Lv = game:GetService("Players").LocalPlayer.Data.Level.Value
    if Old_World then
        if Lv == 1 or Lv <= 9 or SeletMon == "Bandit [Lv. 5]" then -- Bandit
            Ms = "Bandit [Lv. 5]"
            NameQuest = "BanditQuest1"
            QuestLv = 1
            Reward = "Reward:\n$350\n250 Exp."
            CFrameQ = CFrame.new(1060.9383544922, 16.455066680908, 1547.7841796875)
            CFrameMon = CFrame.new(1038.5533447266, 41.296249389648, 1576.5098876953)
        elseif Lv == 10 or Lv <= 14 or SeletMon == "Monkey [Lv. 14]" then -- Monkey
            Ms = "Monkey [Lv. 14]"
            NameQuest = "JungleQuest"
            QuestLv = 1
            Reward = "Reward:\n$800\n1,800 Exp."
            CFrameQ = CFrame.new(-1601.6553955078, 36.85213470459, 153.38809204102)
            CFrameMon = CFrame.new(-1448.1446533203, 50.851993560791, 63.60718536377)
        elseif Lv == 15 or Lv <= 29 or SeletMon == "Gorilla [Lv. 20]" then -- Gorilla
            Ms = "Gorilla [Lv. 20]"
            NameQuest = "JungleQuest"
            QuestLv = 2
            Reward = "Reward:\n$1,200\n3,500 Exp."
            CFrameQ = CFrame.new(-1601.6553955078, 36.85213470459, 153.38809204102)
            CFrameMon = CFrame.new(-1142.6488037109, 40.462348937988, -515.39227294922)
        elseif Lv == 30 or Lv <= 39 or SeletMon == "Pirate [Lv. 35]" then -- Pirate
            Ms = "Pirate [Lv. 35]"
            NameQuest = "BuggyQuest1"
            QuestLv = 1
            Reward = "Reward:\n$3,000\n10,000 Exp."
            CFrameQ = CFrame.new(-1140.1761474609, 4.752049446106, 3827.4057617188)
            CFrameMon = CFrame.new(-1201.0881347656, 40.628940582275, 3857.5966796875)
        elseif Lv == 40 or Lv <= 59 or SeletMon == "Brute [Lv. 45]" then -- Brute
            Ms = "Brute [Lv. 45]"
            NameQuest = "BuggyQuest1"
            QuestLv = 2
            Reward = "Reward:\n$3,500\n18,000 Exp."
            CFrameQ = CFrame.new(-1140.1761474609, 4.752049446106, 3827.4057617188)
            CFrameMon = CFrame.new(-1387.5324707031, 24.592035293579, 4100.9575195313)
        elseif Lv == 60 or Lv <= 74 or SeletMon == "Desert Bandit [Lv. 60]" then -- Desert Bandit
            Ms = "Desert Bandit [Lv. 60]"
            NameQuest = "DesertQuest"
            QuestLv = 1
            Reward = "Reward:\n$4,000\n35,000 Exp."
            CFrameQ = CFrame.new(896.51721191406, 6.4384617805481, 4390.1494140625)
            CFrameMon = CFrame.new(984.99896240234, 16.109552383423, 4417.91015625)
        elseif Lv == 75 or Lv <= 89 or SeletMon == "Desert Officer [Lv. 70]" then -- Desert Officer
            Ms = "Desert Officer [Lv. 70]"
            NameQuest = "DesertQuest"
            QuestLv = 2
            Reward = "Reward:\n$4,500\n50,000 Exp."
            CFrameQ = CFrame.new(896.51721191406, 6.4384617805481, 4390.1494140625)
            CFrameMon = CFrame.new(1547.1510009766, 14.452038764954, 4381.8002929688)
        elseif Lv == 90 or Lv <= 99 or SeletMon == "Snow Bandit [Lv. 90]" then -- Snow Bandit
            Ms = "Snow Bandit [Lv. 90]"
            NameQuest = "SnowQuest"
            QuestLv = 1
            Reward = "Reward:\n$5,000\n70,000 Exp."
            CFrameQ = CFrame.new(1386.8073730469, 87.272789001465, -1298.3576660156)
            CFrameMon = CFrame.new(1356.3028564453, 105.76865386963, -1328.2418212891)
        elseif Lv == 100 or Lv <= 119 or SeletMon == "Snowman [Lv. 100]" then -- Snowman
            Ms = "Snowman [Lv. 100]"
            NameQuest = "SnowQuest"
            QuestLv = 2
            Reward = "Reward:\n$5,500\n120,000 Exp."
            CFrameQ = CFrame.new(1386.8073730469, 87.272789001465, -1298.3576660156)
            CFrameMon = CFrame.new(1218.7956542969, 138.01184082031, -1488.0262451172)
        elseif Lv == 120 or Lv <= 149 or SeletMon == "Chief Petty Officer [Lv. 120]" then -- Chief Petty Officer
            Ms = "Chief Petty Officer [Lv. 120]"
            NameQuest = "MarineQuest2"
            QuestLv = 1
            Reward = "Reward:\n$6,000\n180,000 Exp."
            CFrameQ = CFrame.new(-5035.49609375, 28.677835464478, 4324.1840820313)
            CFrameMon = CFrame.new(-4931.1552734375, 65.793113708496, 4121.8393554688)
        elseif Lv == 150 or Lv <= 174 or SeletMon == "Sky Bandit [Lv. 150]" then -- Sky Bandit
            Ms = "Sky Bandit [Lv. 150]"
            NameQuest = "SkyQuest"
            QuestLv = 1
            Reward = "Reward:\n$7,000\n250,000 Exp."
            CFrameQ = CFrame.new(-4842.1372070313, 717.69543457031, -2623.0483398438)
            CFrameMon = CFrame.new(-4955.6411132813, 365.46365356445, -2908.1865234375)
        elseif Lv == 175 or Lv <= 224 or SeletMon == "Dark Master [Lv. 175]" then -- Dark Master
            Ms = "Dark Master [Lv. 175]"
            NameQuest = "SkyQuest"
            QuestLv = 2
            Reward = "Reward:\n$7,500\n350,000 Exp."
            CFrameQ = CFrame.new(-4842.1372070313, 717.69543457031, -2623.0483398438)
            CFrameMon = CFrame.new(-5148.1650390625, 439.04571533203, -2332.9611816406)
        elseif Lv == 225 or Lv <= 274 or SeletMon == "Toga Warrior [Lv. 225]" then -- Toga Warrior
            Ms = "Toga Warrior [Lv. 225]"
            NameQuest = "ColosseumQuest"
            QuestLv = 1
            Reward = "Reward:\n$7,000\n700,000 Exp."
            CFrameQ = CFrame.new(-1577.7890625, 7.4151420593262, -2984.4838867188)
            CFrameMon = CFrame.new(-1872.5166015625, 49.080215454102, -2913.810546875)
        elseif Lv == 275 or Lv <= 299 or SeletMon == "Gladiator [Lv. 275]" then -- Gladiator
            Ms = "Gladiator [Lv. 275]"
            NameQuest = "ColosseumQuest"
            QuestLv = 2
            Reward = "Reward:\n$7,500\n1,000,000 Exp."
            CFrameQ = CFrame.new(-1577.7890625, 7.4151420593262, -2984.4838867188)
            CFrameMon = CFrame.new(-1521.3740234375, 81.203170776367, -3066.3139648438)
        elseif Lv == 300 or Lv <= 329 or SeletMon == "Military Soldier [Lv. 300]" then -- Military Soldier
            Ms = "Military Soldier [Lv. 300]"
            NameQuest = "MagmaQuest"
            QuestLv = 1
            Reward = "Reward:\n$8,250\n1,300,000 Exp."
            CFrameQ = CFrame.new(-5316.1157226563, 12.262831687927, 8517.00390625)
            CFrameMon = CFrame.new(-5369.0004882813, 61.24352645874, 8556.4921875)
        elseif Lv == 330 or Lv <= 374 or SeletMon == "Military Spy [Lv. 330]" then -- Military Spy
            Ms = "Military Spy [Lv. 330]"
            NameQuest = "MagmaQuest"
            QuestLv = 2
            Reward = "Reward:\n$8,500\n1,850,000 Exp."
            CFrameQ = CFrame.new(-5316.1157226563, 12.262831687927, 8517.00390625)
            CFrameMon = CFrame.new(-5984.0532226563, 82.14656829834, 8753.326171875)
        elseif Lv == 375 or Lv <= 399 or SeletMon == "Fishman Warrior [Lv. 375]" then -- Fishman Warrior 
            Ms = "Fishman Warrior [Lv. 375]"
            NameQuest = "FishmanQuest"
            QuestLv = 1
            Reward = "Reward:\n$8,750\n2,500,000 Exp."
            CFrameQ = CFrame.new(61122.65234375, 18.497442245483, 1569.3997802734)
            CFrameMon = CFrame.new(60844.10546875, 98.462875366211, 1298.3985595703)
			if Auto_Farm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
				wait()
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
				wait(.5)
			end
        elseif Lv == 400 or Lv <= 449 or SeletMon == "Fishman Commando [Lv. 400]" then -- Fishman Commando
            Ms = "Fishman Commando [Lv. 400]"
            NameQuest = "FishmanQuest"
            QuestLv = 2
            Reward = "Reward:\n$9,000\n3,000,000 Exp."
            CFrameQ = CFrame.new(61122.65234375, 18.497442245483, 1569.3997802734)
            CFrameMon = CFrame.new(61738.3984375, 64.207321166992, 1433.8375244141)
			if Auto_Farm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
				wait()
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
				wait(.5)
			end
        elseif Lv == 450 or Lv <= 474 or SeletMon == "God's Guard [Lv. 450]" then -- God's Guard
            Ms = "God's Guard [Lv. 450]"
            NameQuest = "SkyExp1Quest"
            QuestLv = 1
            Reward = "Reward:\n$8,750\n3,800,000 Exp."
            CFrameQ = CFrame.new(-4721.8603515625, 845.30297851563, -1953.8489990234)
            CFrameMon = CFrame.new(-4628.0498046875, 866.92877197266, -1931.2352294922)
			if Auto_Farm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
				wait()
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-4607.82275, 872.54248, -1667.55688))
				wait(.5)
			end
        elseif Lv == 475 or Lv <= 524 or SeletMon == "Shanda [Lv. 475]" then -- Shanda
            Ms = "Shanda [Lv. 475]"
            NameQuest = "SkyExp1Quest"
            QuestLv = 2
            Reward = "Reward:\n$9,000\n4,300,000 Exp."
            CFrameQ = CFrame.new(-7863.1596679688, 5545.5190429688, -378.42266845703)
            CFrameMon = CFrame.new(-7685.1474609375, 5601.0751953125, -441.38876342773)
			if Auto_Farm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 3000 then
				wait()
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
				wait(.5)
			end
        elseif Lv == 525 or Lv <= 549 or SeletMon == "Royal Squad [Lv. 525]" then -- Royal Squad
            Ms = "Royal Squad [Lv. 525]"
            NameQuest = "SkyExp2Quest"
            QuestLv = 1
            Reward = "Reward:\n$9,500\n4,600,000 Exp."
            CFrameQ = CFrame.new(-7903.3828125, 5635.9897460938, -1410.923828125)
            CFrameMon = CFrame.new(-7654.2514648438, 5637.1079101563, -1407.7550048828)
        elseif Lv == 550 or Lv <= 624 or SeletMon == "Royal Soldier [Lv. 550]" then -- Royal Soldier
            Ms = "Royal Soldier [Lv. 550]"
            NameQuest = "SkyExp2Quest"
            QuestLv = 2
            Reward = "Reward:\n$9,750\n5,000,000 Exp."
            CFrameQ = CFrame.new(-7903.3828125, 5635.9897460938, -1410.923828125)
            CFrameMon = CFrame.new(-7760.4106445313, 5679.9077148438, -1884.8112792969)
        elseif Lv == 625 or Lv <= 649 or SeletMon == "Galley Pirate [Lv. 625]" then -- Galley Pirate
            Ms = "Galley Pirate [Lv. 625]"
            NameQuest = "FountainQuest"
            QuestLv = 1
            Reward = "Reward:\n$10,000\n5,800,000 Exp."
            CFrameQ = CFrame.new(5258.2788085938, 38.526931762695, 4050.044921875)
            CFrameMon = CFrame.new(5557.1684570313, 152.32717895508, 3998.7758789063)
        elseif Lv >= 650 or SeletMon == "Galley Captain [Lv. 650]" then -- Galley Captain
            Ms = "Galley Captain [Lv. 650]"
            NameQuest = "FountainQuest"
            QuestLv = 2
            Reward = "Reward:\n$10,000\n6,300,000 Exp."
            CFrameQ = CFrame.new(5258.2788085938, 38.526931762695, 4050.044921875)
            CFrameMon = CFrame.new(5677.6772460938, 92.786109924316, 4966.6323242188)
        end
    end
    if New_World then
        if Lv == 700 or Lv <= 724 or SeletMon == "Raider [Lv. 700]" then -- Raider
            Ms = "Raider [Lv. 700]"
            NameQuest = "Area1Quest"
            QuestLv = 1
            Reward = "Reward:\n$10,250\n6,750,000 Exp."
            CFrameQ = CFrame.new(-427.72567749023, 72.99634552002, 1835.9426269531)
            CFrameMon = CFrame.new(68.874565124512, 93.635643005371, 2429.6752929688)
        elseif Lv == 725 or Lv <= 774 or SeletMon == "Mercenary [Lv. 725]" then -- Mercenary
            Ms = "Mercenary [Lv. 725]"
            NameQuest = "Area1Quest"
            QuestLv = 2
            Reward = "Reward:\n$10,500\n7,000,000 Exp."
            CFrameQ = CFrame.new(-427.72567749023, 72.99634552002, 1835.9426269531)
            CFrameMon = CFrame.new(-864.85009765625, 122.47104644775, 1453.1505126953)
        elseif Lv == 775 or Lv <= 799 or SeletMon == "Swan Pirate [Lv. 775]" then -- Swan Pirate
            Ms = "Swan Pirate [Lv. 775]"
            NameQuest = "Area2Quest"
            QuestLv = 1
            Reward = "Reward:\n$10,750\n7,500,000 Exp."
            CFrameQ = CFrame.new(635.61151123047, 73.096351623535, 917.81298828125)
            CFrameMon = CFrame.new(1065.3669433594, 137.64012145996, 1324.3798828125)
        elseif Lv == 800 or Lv <= 874 or SeletMon == "Factory Staff [Lv. 800]" then -- Factory Staff
            Ms = "Factory Staff [Lv. 800]"
            NameQuest = "Area2Quest"
            QuestLv = 2
            Reward = "Reward:\n$11,000\n8,250,000 Exp."
            CFrameQ = CFrame.new(635.61151123047, 73.096351623535, 917.81298828125)
            CFrameMon = CFrame.new(533.22045898438, 128.46876525879, 355.62615966797)
        elseif Lv == 875 or Lv <= 899 or SeletMon == "Marine Lieutenant [Lv. 875]" then -- Marine Lieutenant
            Ms = "Marine Lieutenant [Lv. 875]"
            NameQuest = "MarineQuest3"
            QuestLv = 1
            Reward = "Reward:\n$11,250\n9,000,000 Exp."
            CFrameQ = CFrame.new(-2440.9934082031, 73.04190826416, -3217.7082519531)
            CFrameMon = CFrame.new(-2489.2622070313, 84.613594055176, -3151.8830566406)
        elseif Lv == 900 or Lv <= 949 or SeletMon == "Marine Captain [Lv. 900]" then -- Marine Captain
            Ms = "Marine Captain [Lv. 900]"
            NameQuest = "MarineQuest3"
            QuestLv = 2
            Reward = "Reward:\n$11,500\n10,500,000 Exp."
            CFrameQ = CFrame.new(-2440.9934082031, 73.04190826416, -3217.7082519531)
            CFrameMon = CFrame.new(-2335.2026367188, 79.786659240723, -3245.8674316406)
        elseif Lv == 950 or Lv <= 974 or SeletMon == "Zombie [Lv. 950]" then -- Zombie
            Ms = "Zombie [Lv. 950]"
            NameQuest = "ZombieQuest"
            QuestLv = 1
            Reward = "Reward:\n$11,750\n11,000,000 Exp."
            CFrameQ = CFrame.new(-5494.3413085938, 48.505931854248, -794.59094238281)
            CFrameMon = CFrame.new(-5536.4970703125, 101.08577728271, -835.59075927734)
        elseif Lv == 975 or Lv <= 999 or SeletMon == "Vampire [Lv. 975]" then -- Vampire
            Ms = "Vampire [Lv. 975]"
            NameQuest = "ZombieQuest"
            QuestLv = 2
            Reward = "Reward:\n$12,000\n12,000,000 Exp."
            CFrameQ = CFrame.new(-5494.3413085938, 48.505931854248, -794.59094238281)
            CFrameMon = CFrame.new(-5806.1098632813, 16.722528457642, -1164.4384765625)
        elseif Lv == 1000 or Lv <= 1049 or SeletMon == "Snow Trooper [Lv. 1000]" then -- Snow Trooper
            Ms = "Snow Trooper [Lv. 1000]"
            NameQuest = "SnowMountainQuest"
            QuestLv = 1
            Reward = "Reward:\n$12,250\n13,000,000 Exp."
            CFrameQ = CFrame.new(607.05963134766, 401.44781494141, -5370.5546875)
            CFrameMon = CFrame.new(535.21051025391, 432.74209594727, -5484.9165039063)
        elseif Lv == 1050 or Lv <= 1099 or SeletMon == "Winter Warrior [Lv. 1050]" then -- Winter Warrior
            Ms = "Winter Warrior [Lv. 1050]"
            NameQuest = "SnowMountainQuest"
            QuestLv = 2
            Reward = "Reward:\n$12,500\n14,200,000 Exp."
            CFrameQ = CFrame.new(607.05963134766, 401.44781494141, -5370.5546875)
            CFrameMon = CFrame.new(1234.4449462891, 456.95419311523, -5174.130859375)
        elseif Lv == 1100 or Lv <= 1124 or SeletMon == "Lab Subordinate [Lv. 1100]" then -- Lab Subordinate
            Ms = "Lab Subordinate [Lv. 1100]"
            NameQuest = "IceSideQuest"
            QuestLv = 1
            Reward = "Reward:\n$12,250\n15,500,000 Exp."
            CFrameQ = CFrame.new(-6061.841796875, 15.926671981812, -4902.0385742188)
            CFrameMon = CFrame.new(-5720.5576171875, 63.309471130371, -4784.6103515625)
        elseif Lv == 1125 or Lv <= 1174 or SeletMon == "Horned Warrior [Lv. 1125]" then -- Horned Warrior
            Ms = "Horned Warrior [Lv. 1125]"
            NameQuest = "IceSideQuest"
            QuestLv = 2
            Reward = "Reward:\n$12,500\n16,800,000 Exp."
            CFrameQ = CFrame.new(-6061.841796875, 15.926671981812, -4902.0385742188)
            CFrameMon = CFrame.new(-6292.751953125, 91.181983947754, -5502.6499023438)
        elseif Lv == 1175 or Lv <= 1199 or SeletMon == "Magma Ninja [Lv. 1175]" then -- Magma Ninja
            Ms = "Magma Ninja [Lv. 1175]"
            NameQuest = "FireSideQuest"
            QuestLv = 1
            Reward = "Reward:\n$12,250\n18,000,000 Exp."
            CFrameQ = CFrame.new(-5429.0473632813, 15.977565765381, -5297.9614257813)
            CFrameMon = CFrame.new(-5461.8388671875, 130.36347961426, -5836.4702148438)
        elseif Lv == 1200 or Lv <= 1249 or SeletMon == "Lava Pirate [Lv. 1200]" then -- Lava Pirate
            Ms = "Lava Pirate [Lv. 1200]"
            NameQuest = "FireSideQuest"
            QuestLv = 2
            Reward = "Reward:\n$12,500\n20,000,000 Exp."
            CFrameQ = CFrame.new(-5429.0473632813, 15.977565765381, -5297.9614257813)
            CFrameMon = CFrame.new(-5251.1889648438, 55.164535522461, -4774.4096679688)
        elseif Lv == 1250 or Lv <= 1274 or SeletMon == "Ship Deckhand [Lv. 1250]" then -- Ship Deckhand
            Ms = "Ship Deckhand [Lv. 1250]"
            NameQuest = "ShipQuest1"
            QuestLv = 1
            Reward = "Reward:\n$12,250\n23,000,000 Exp."
            CFrameQ = CFrame.new(1040.2927246094, 125.08293151855, 32911.0390625)
            CFrameMon = CFrame.new(921.12365722656, 125.9839553833, 33088.328125)
			if Auto_Farm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				wait()
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
				wait(.5)
			end
        elseif Lv == 1275 or Lv <= 1299 or SeletMon == "Ship Engineer [Lv. 1275]" then -- Ship Engineer
            Ms = "Ship Engineer [Lv. 1275]"
            NameQuest = "ShipQuest1"
            QuestLv = 2
            Reward = "Reward:\n$12,500\n24,500,000 Exp."
            CFrameQ = CFrame.new(1040.2927246094, 125.08293151855, 32911.0390625)
            CFrameMon = CFrame.new(886.28179931641, 40.47790145874, 32800.83203125)
			if Auto_Farm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				wait()
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
				wait(.5)
			end
        elseif Lv == 1300 or Lv <= 1324 or SeletMon == "Ship Steward [Lv. 1300]" then -- Ship Steward
            Ms = "Ship Steward [Lv. 1300]"
            NameQuest = "ShipQuest2"
            QuestLv = 1
            Reward = "Reward:\n$12,250\n26,500,000 Exp."
            CFrameQ = CFrame.new(971.42065429688, 125.08293151855, 33245.54296875)
            CFrameMon = CFrame.new(943.85504150391, 129.58183288574, 33444.3671875)
			if Auto_Farm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				wait()
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
				wait(.5)
			end
        elseif Lv == 1325 or Lv <= 1349 or SeletMon == "Ship Officer [Lv. 1325]" then -- Ship Officer
            Ms = "Ship Officer [Lv. 1325]"
            NameQuest = "ShipQuest2"
            QuestLv = 2
            Reward = "Reward:\n$12,500\n28,500,000 Exp."
            CFrameQ = CFrame.new(971.42065429688, 125.08293151855, 33245.54296875)
            CFrameMon = CFrame.new(955.38458251953, 181.08335876465, 33331.890625)
			if Auto_Farm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				wait()
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
				wait(.5)
			end
        elseif Lv == 1350 or Lv <= 1374 or SeletMon == "Arctic Warrior [Lv. 1350]" then -- Arctic Warrior
            Ms = "Arctic Warrior [Lv. 1350]"
            NameQuest = "FrostQuest"
            QuestLv = 1
            Reward = "Reward:\n$12,250\n30,000,000 Exp."
            CFrameQ = CFrame.new(5668.1372070313, 28.202531814575, -6484.6005859375)
            CFrameMon = CFrame.new(5935.4541015625, 77.26016998291, -6472.7568359375)
            if Auto_Farm and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				wait()
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-6508.5581054688, 89.034996032715, -132.83953857422))
				wait(.5)
			end
        elseif Lv == 1375 or Lv <= 1424 or SeletMon == "Snow Lurker [Lv. 1375]" then -- Snow Lurker
            Ms = "Snow Lurker [Lv. 1375]"
            NameQuest = "FrostQuest"
            QuestLv = 2
            Reward = "Reward:\n$12,500\n32,000,000 Exp."
            CFrameQ = CFrame.new(5668.1372070313, 28.202531814575, -6484.6005859375)
            CFrameMon = CFrame.new(5628.482421875, 57.574996948242, -6618.3481445313)
        elseif Lv == 1425 or Lv <= 1449 or SeletMon == "Sea Soldier [Lv. 1425]" then -- Sea Soldier
            Ms = "Sea Soldier [Lv. 1425]"
            NameQuest = "ForgottenQuest"
            QuestLv = 1
            Reward = "Reward:\n$12,250\n33,500,000 Exp."
            CFrameQ = CFrame.new(-3054.5827636719, 236.87213134766, -10147.790039063)
            CFrameMon = CFrame.new(-3185.0153808594, 58.789089202881, -9663.6064453125)
        elseif Lv >= 1450 or SeletMon == "Water Fighter [Lv. 1450]" then -- Water Fighter
            Ms = "Water Fighter [Lv. 1450]"
            NameQuest = "ForgottenQuest"
            QuestLv = 2
            Reward = "Reward:\n$12,500\n35,500,000 Exp."
            CFrameQ = CFrame.new(-3054.5827636719, 236.87213134766, -10147.790039063)
            CFrameMon = CFrame.new(-3262.9301757813, 298.69036865234, -10552.529296875)
		end
	end
	if SeaThird_World then
		if Lv == 1500 or Lv <= 1524 or SeletMon == "Pirate Millionaire [Lv. 1500]" then -- Pirate Millionaire
			Ms = "Pirate Millionaire [Lv. 1500]"
			NameQuest = "PiratePortQuest"
			QuestLv = 1
			Reward = "Reward:\n$13,000\n35,000,000 Exp."
			CFrameQ = CFrame.new(-289.61752319336, 43.819011688232, 5580.0903320313)
			CFrameMon = CFrame.new(-435.68109130859, 189.69866943359, 5551.0756835938)
		elseif Lv == 1525 or Lv <= 1574 or SeletMon == "Pistol Billionaire [Lv. 1525]" then -- Pistol Billoonaire
			Ms = "Pistol Billionaire [Lv. 1525]"
			NameQuest = "PiratePortQuest"
			QuestLv = 2
			Reward = "Reward:\n$15,000\n37,500,000 Exp."
			CFrameQ = CFrame.new(-289.61752319336, 43.819011688232, 5580.0903320313)
			CFrameMon = CFrame.new(-236.53652954102, 217.46676635742, 6006.0883789063)
		elseif Lv == 1575 or Lv <= 1599 or SeletMon == "Dragon Crew Warrior [Lv. 1575]" then -- Dragon Crew Warrior
			Ms = "Dragon Crew Warrior [Lv. 1575]"
			NameQuest = "AmazonQuest"
			QuestLv = 1
			Reward = "Reward:\n$13,000\n40,000,000 Exp."
			CFrameQ = CFrame.new(5833.1147460938, 51.60498046875, -1103.0693359375)
			CFrameMon = CFrame.new(6301.9975585938, 104.77153015137, -1082.6075439453)
		elseif Lv == 1600 or Lv <= 1624 or SeletMon == "Dragon Crew Archer [Lv. 1600]" then -- Dragon Crew Archer
			Ms = "Dragon Crew Archer [Lv. 1600]"
			NameQuest = "AmazonQuest"
			QuestLv = 2
			Reward = "Reward:\n$15,000\n42,500,000 Exp."
			CFrameQ = CFrame.new(5833.1147460938, 51.60498046875, -1103.0693359375)
			CFrameMon = CFrame.new(6831.1171875, 441.76708984375, 446.58615112305)
		elseif Lv == 1625 or Lv <= 1649 or SeletMon == "Female Islander [Lv. 1625]" then -- Female Islander
			Ms = "Female Islander [Lv. 1625]"
			NameQuest = "AmazonQuest2"
			QuestLv = 1
			Reward = "Reward:\n$13,000\n45,500,000 Exp."
			CFrameQ = CFrame.new(5446.8793945313, 601.62945556641, 749.45672607422)
			CFrameMon = CFrame.new(5792.5166015625, 848.14392089844, 1084.1818847656)
		elseif Lv == 1650 or Lv <= 1699 or SeletMon == "Giant Islander [Lv. 1650]" then -- Giant Islander
			Ms = "Giant Islander [Lv. 1650]"
			NameQuest = "AmazonQuest2"
			QuestLv = 2
			Reward = "Reward:\n$15,000\n48,000,000 Exp."
			CFrameQ = CFrame.new(5446.8793945313, 601.62945556641, 749.45672607422)
			CFrameMon = CFrame.new(5009.5068359375, 664.11071777344, -40.960144042969)
		elseif Lv == 1700 or Lv <= 1724 or SeletMon == "Marine Commodore [Lv. 1700]" then -- Marine Commodore
			Ms = "Marine Commodore [Lv. 1700]"
			NameQuest = "MarineTreeIsland"
			QuestLv = 1
			Reward = "Reward:\n$13,000\n51,000,000 Exp."
			CFrameQ = CFrame.new(2179.98828125, 28.731239318848, -6740.0551757813)
			CFrameMon = CFrame.new(2198.0063476563, 128.71075439453, -7109.5043945313)
		elseif Lv == 1725 or Lv <= 1774 or SeletMon == "Marine Rear Admiral [Lv. 1725]" then -- Marine Rear Admiral
			Ms = "Marine Rear Admiral [Lv. 1725]"
			NameQuest = "MarineTreeIsland"
			QuestLv = 2
			Reward = "Reward:\n$15,000\n53,500,000 Exp."
			CFrameQ = CFrame.new(2179.98828125, 28.731239318848, -6740.0551757813)
			CFrameMon = CFrame.new(3294.3142089844, 385.41125488281, -7048.6342773438)
		elseif Lv == 1775 or Lv <= 1799 or SeletMon == "Fishman Raider [Lv. 1775]" then -- Fishman Raide
			Ms = "Fishman Raider [Lv. 1775]"
			NameQuest = "DeepForestIsland3"
			QuestLv = 1
			Reward = "Reward:\n$13,000\n56,000,000 Exp."
			CFrameQ = CFrame.new(-10582.759765625, 331.78845214844, -8757.666015625)
			CFrameMon = CFrame.new(-10553.268554688, 521.38439941406, -8176.9458007813)
		elseif Lv == 1800 or Lv <= 1824 or SeletMon == "Fishman Captain [Lv. 1800]" then -- Fishman Captain
			Ms = "Fishman Captain [Lv. 1800]"
			NameQuest = "DeepForestIsland3"
			QuestLv = 2
			Reward = "Reward:\n$15,000\n58,500,000 Exp."
			CFrameQ = CFrame.new(-10583.099609375, 331.78845214844, -8759.4638671875)
			CFrameMon = CFrame.new(-10789.401367188, 427.18637084961, -9131.4423828125)
		elseif Lv == 1825 or Lv <= 1849 or SeletMon == "Forest Pirate [Lv. 1825]" then -- Forest Pirate
			Ms = "Forest Pirate [Lv. 1825]"
			NameQuest = "DeepForestIsland"
			QuestLv = 1
			Reward = "Reward:\n$13,000\n61,000,000 Exp."
			CFrameQ = CFrame.new(-13232.662109375, 332.40396118164, -7626.4819335938)
			CFrameMon = CFrame.new(-13489.397460938, 400.30349731445, -7770.251953125)
		elseif Lv == 1850 or Lv <= 1899 or SeletMon == "Mythological Pirate [Lv. 1850]" then -- Mythological Pirate
			Ms = "Mythological Pirate [Lv. 1850]"
			NameQuest = "DeepForestIsland"
			QuestLv = 2
			Reward = "Reward:\n$13,000\n64,000,000 Exp."
			CFrameQ = CFrame.new(-13232.662109375, 332.40396118164, -7626.4819335938)
			CFrameMon = CFrame.new(-13508.616210938, 582.46228027344, -6985.3037109375)
		elseif Lv == 1900 or Lv <= 1924 or SeletMon == "Jungle Pirate [Lv. 1900]" then -- Jungle Pirate
			Ms = "Jungle Pirate [Lv. 1900]"
			NameQuest = "DeepForestIsland2"
			QuestLv = 1
			Reward = "Reward:\n$13,000\n67,000,000 Exp."
			CFrameQ = CFrame.new(-12682.096679688, 390.88653564453, -9902.1240234375)
			CFrameMon = CFrame.new(-12267.103515625, 459.75262451172, -10277.200195313)
		elseif Lv == 1925 or Lv <= 1974 or SeletMon == "Musketeer Pirate [Lv. 1925]" then -- Musketeer Pirate
			Ms = "Musketeer Pirate [Lv. 1925]"
			NameQuest = "DeepForestIsland2"
			QuestLv = 2
			Reward = "Reward:\n$15,000\n70,000,000 Exp."
			CFrameQ = CFrame.new(-12682.096679688, 390.88653564453, -9902.1240234375)
			CFrameMon = CFrame.new(-13291.5078125, 520.47338867188, -9904.638671875)
		elseif Lv == 1975 or Lv <= 1999 then
			Ms = "Reborn Skeleton [Lv. 1975]"
			NameQuest = "HauntedQuest1"
			QuestLv = 1
			Reward = "Reward:\n$13,000\n73,000,000 Exp."
			CFrameQ = CFrame.new(-9480.80762, 142.130661, 5566.37305, -0.00655503059, 4.52954225e-08, -0.999978542, 2.04920472e-08, 1, 4.51620679e-08, 0.999978542, -2.01955679e-08, -0.00655503059)
			CFrameMon = CFrame.new(-8761.77148, 183.431747, 6168.33301, 0.978073597, -1.3950732e-05, -0.208259016, -1.08073925e-06, 1, -7.20630269e-05, 0.208259016, 7.07080399e-05, 0.978073597)
		elseif Lv == 2000 or Lv <= 2024 then
			Ms = "Living Zombie [Lv. 2000]"
			NameQuest = "HauntedQuest1"
			QuestLv = 2
			Reward = "Reward:\n$13,250\n75,500,000 Exp."
			CFrameQ = CFrame.new(-9480.80762, 142.130661, 5566.37305, -0.00655503059, 4.52954225e-08, -0.999978542, 2.04920472e-08, 1, 4.51620679e-08, 0.999978542, -2.01955679e-08, -0.00655503059)
			CFrameMon = CFrame.new(-10103.7529, 238.565979, 6179.75977, 0.999474227, 2.77547141e-08, 0.0324240364, -2.58006327e-08, 1, -6.06848474e-08, -0.0324240364, 5.98163865e-08, 0.999474227)
		elseif Lv == 2025 or Lv <= 2049 then
			Ms = "Demonic Soul [Lv. 2025]"
			NameQuest = "HauntedQuest2"
			QuestLv = 1
			Reward = "Reward:\n$13,500\n78,000,000 Exp."
			CFrameQ = CFrame.new(-9515.39551, 172.266037, 6078.89746, 0.0121199936, -9.78649624e-08, 0.999926567, 2.30358754e-08, 1, 9.75929382e-08, -0.999926567, 2.18513581e-08, 0.0121199936)
			CFrameMon = CFrame.new(-9709.30762, 204.695892, 6044.04688, -0.845798075, -3.4587876e-07, -0.533503294, -4.46235369e-08, 1, -5.77571257e-07, 0.533503294, -4.64701827e-07, -0.845798075)
		elseif Lv >= 2050 then
			Ms = "Posessed Mummy [Lv. 2050]"
			NameQuest = "HauntedQuest2"
			QuestLv = 2
			Reward = "Reward:\n$13,750\n80,500,000 Exp."
			CFrameQ = CFrame.new(-9515.39551, 172.266037, 6078.89746, 0.0121199936, -9.78649624e-08, 0.999926567, 2.30358754e-08, 1, 9.75929382e-08, -0.999926567, 2.18513581e-08, 0.0121199936)
			CFrameMon = CFrame.new(-9554.11035, 65.6141663, 6041.73584, -0.877069294, 5.33355795e-08, -0.480364174, 2.06420765e-08, 1, 7.33423562e-08, 0.480364174, 5.44105987e-08, -0.877069294)
		end
	end
end

function TP(P)
    local Speed = 0
    Distance = (P.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if Distance < 250 then
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = P
    elseif Distance < 500 then
        Speed = 400
    elseif Distance < 1000 then
        Speed = 350
    elseif Distance >= 1000 then
        Speed = 300
    end
    if Distance >= 300 then
        game:GetService("TweenService"):Create(
            game.Players.LocalPlayer.Character.HumanoidRootPart,
            TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
            {CFrame = P}
        ):Play()
    end
end
    
 function Click()
    game:GetService'VirtualUser':CaptureController()
    game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
 end

 SelectToolWeapon = ""
 function EquipWeapon(ToolSe)
	 if game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe) then
		 local tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
		 wait(.4)
		 game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
	 end
 end
 

 local noclip = Instance.new('Part',workspace)
 noclip.Name = "noclip"
 noclip.CanCollide = true
 noclip.Anchored = true
 noclip.Size = Vector3.new(30,30,30)
 noclip.Transparency = 1
 
 
 
 function noclipnew()
	game:GetService("Workspace")["noclip"].CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame  * CFrame.new(0,-3.5,0)
 end
 spawn(function()
    game:GetService("RunService").RenderStepped:Connect(function()
        pcall(function()
            if _G.noclip == true then
                noclipnew()
            else
               game:GetService("Workspace"):FindFirstChild("noclip"):Destroy()
            end
        end)
    end)
end)


section1:addToggle("Auto Farm ", false, function(vu)
    _G.Auto_Farm = vu
end)

spawn(function()
    while wait(.1) do
        if _G.Auto_Farm then
            if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                StartMagnet = false
                CheckLevel()
                TP(CFrameQ)
                if (CFrameQ.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 10 then
                    wait(1.1)
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", NameQuest, QuestLv)
                end
            elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                CheckLevel()
                pcall(function()
                    if game:GetService("Workspace").Enemies:FindFirstChild(Ms) then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == Ms then
                                if v:WaitForChild("Humanoid").Health > 0 then
                                    repeat game:GetService("RunService").Heartbeat:wait()
                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                        EquipWeapon(_G.SelectWeapon)
                                        if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestReward.Title.Text, Reward) then
                                            TP(v.HumanoidRootPart.CFrame * CFrame.new(0, 20, 0))
                                            game:GetService("VirtualUser"):CaptureController()
                                            game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
                                            v.HumanoidRootPart.CanCollide = false
                                            v.Head.CanCollide = false
                                            v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
                                            StartMagnet = true
                                            PosMon = v.HumanoidRootPart.CFrame
                                        else
                                            StartMagnet = false
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
                                        end
                                    until not v.Parent or v.Humanoid.Health <= 0 or _G.Auto_Farm == false or game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                    StartMagnet = false
                                end
                            end
                        end
                    else
                        StartMagnet = false
                        CheckLevel()
                        TP(CFrameMon)
                    end
                end)
            end
        end
    end
end)

spawn(function()
	game:GetService("RunService").Heartbeat:Connect(function()
		pcall(function()
			CheckLevel()
			for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
				if _G.Auto_Farm and StartMagnet then
					if v.Name == Ms and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
						if v.Name == "Monkey [Lv. 14]" then
							if (v.HumanoidRootPart.Position - PosMon.Position).Magnitude <= 250 then
								v.Head.CanCollide = false
								v.HumanoidRootPart.CanCollide = false
								v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
								v.HumanoidRootPart.CFrame = PosMon
								sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
							end
						elseif v.Name == "Factory Staff [Lv. 800]" then
							if (v.HumanoidRootPart.Position - PosMon.Position).Magnitude <= 250 then
								v.Head.CanCollide = false
								v.HumanoidRootPart.CanCollide = false
								v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
								v.HumanoidRootPart.CFrame = PosMon
								sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
							end
						elseif v.Name == Ms then
							if (v.HumanoidRootPart.Position - PosMon.Position).Magnitude <= 400 then
								v.Head.CanCollide = false
								v.HumanoidRootPart.CanCollide = false
								v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
								v.HumanoidRootPart.CFrame = PosMon
								sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
							end
						end
					end
        				elseif _G.AutoCandy and CandyMagnet then
        					if (v.Name == "Peanut Scout [Lv. 2075]" or v.Name == "Peanut President [Lv. 2100]"  or v.Name == "Ice Cream Chef [Lv. 2125]" or v.Name == "Ice Cream Commander [Lv. 2150]") and (v.HumanoidRootPart.Position - MainMonCandy.Position).Magnitude <= 300 then
        						v.Head.CanCollide = false
        						v.HumanoidRootPart.CanCollide = false
        						v.HumanoidRootPart.Size = Vector3.new(60,60,60)
        						v.HumanoidRootPart.CFrame = CandyMoney
        						sethiddenproperty(game.Player.LocalPlayer,  "SimulationRadius", math.huge)	

					end
				end
			end
		end)	
	end)
end)

section1:addToggle("Fast Attack  ", false, function(value)
    _G.FastAttack = value
end)

local RigC = require(game:GetService("Players").LocalPlayer.PlayerScripts.CombatFramework)
kkii = require(game.ReplicatedStorage.Util.CameraShaker)
kkii:Stop()
spawn(function()
            game:GetService("RunService").Heartbeat:Connect(function()
 if _G.FastAttack then
            if not RigC.activeController.hitboxMagnitude == 240 then
              RigC.activeController.hitboxMagnitude = 240
            end
            RigC.activeController.attacking = false
            RigC.activeController.increment = 3
            RigC.activeController.timeToNextAttack = (-math.huge^math.huge*math.huge)
            game:GetService'VirtualUser':CaptureController()
            game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
end
    end)
end)


section1:addToggle("Auto Superhuman", _G.Superhuman, function(vu)
	_G.Superhuman = vu
end)
spawn(function()
		while wait() do wait()
			if _G.Superhuman then
				if game.Players.LocalPlayer.Backpack:FindFirstChild("Combat") or game.Players.LocalPlayer.Character:FindFirstChild("Combat") then
					local args = {
						[1] = "BuyBlackLeg"
					}
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
				end   
				if game.Players.LocalPlayer.Character:FindFirstChild("Superhuman") or game.Players.LocalPlayer.Backpack:FindFirstChild("Superhuman") then
					_G.SelectWeapon = "Superhuman"
				end  
				if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") or game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") or game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") or game.Players.LocalPlayer.Character:FindFirstChild("Electro") or game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") or game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate") or game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") or game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") then
					if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value <= 299 then
						_G.SelectWeapon = "Black Leg"
					end
					if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value <= 299 then
						_G.SelectWeapon = "Electro"
					end
					if game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value <= 299 then
						_G.SelectWeapon = "Fishman Karate"
					end
					if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value <= 299 then
						_G.SelectWeapon = "Dragon Claw"
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

section1:addButton("RTX Graphic",function()

			getgenv().mode = "Autumn" -- Choose from Summer and Autumn




			local a = game.Lighting
			a.Ambient = Color3.fromRGB(33, 33, 33)
			a.Brightness = 6.67
			a.ColorShift_Bottom = Color3.fromRGB(0, 0, 0)
			a.ColorShift_Top = Color3.fromRGB(255, 247, 237)
			a.EnvironmentDiffuseScale = 0.105
			a.EnvironmentSpecularScale = 0.522
			a.GlobalShadows = true
			a.OutdoorAmbient = Color3.fromRGB(51, 54, 67)
			a.ShadowSoftness = 0.04
			a.GeographicLatitude = -15.525
			a.ExposureCompensation = 0.75
			local b = Instance.new("BloomEffect", a)
			b.Enabled = true
			b.Intensity = 0.04
			b.Size = 1900
			b.Threshold = 0.915
			local c = Instance.new("ColorCorrectionEffect", a)
			c.Brightness = 0.176
			c.Contrast = 0.39
			c.Enabled = true
			c.Saturation = 0.2
			c.TintColor = Color3.fromRGB(217, 145, 57)
			if getgenv().mode == "Summer" then
				c.TintColor = Color3.fromRGB(255, 220, 148)
			elseif getgenv().mode == "Autumn" then
				c.TintColor = Color3.fromRGB(217, 145, 57)
			else
				warn("No mode selected!")
				print("Please select a mode")
				b:Destroy()
				c:Destroy()
			end
			local d = Instance.new("DepthOfFieldEffect", a)
			d.Enabled = true
			d.FarIntensity = 0.077
			d.FocusDistance = 21.54
			d.InFocusRadius = 20.77
			d.NearIntensity = 0.277
			local e = Instance.new("ColorCorrectionEffect", a)
			e.Brightness = 0
			e.Contrast = -0.07
			e.Saturation = 0
			e.Enabled = true
			e.TintColor = Color3.fromRGB(255, 247, 239)
			local e2 = Instance.new("ColorCorrectionEffect", a)
			e2.Brightness = 0.2
			e2.Contrast = 0.45
			e2.Saturation = -0.1
			e2.Enabled = true
			e2.TintColor = Color3.fromRGB(255, 255, 255)
			local s = Instance.new("SunRaysEffect", a)
			s.Enabled = true
			s.Intensity = 0.01
			s.Spread = 0.146

		end)

         --	spawn(function()
         --		pcall(function()
         --		while wait(.1) do
         --			if _G.Superhuman then
         --				local args = {
         --					[1] = "BuySuperhuman"
         --				}
         --				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
         --				-----------------
         --				local MyLevel = game.Players.LocalPlayer.Data.Level.Value
         --				if MyLevel >= 1100 then
         --					if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") or game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") then
         --				_G.autoraid = false
         --					else
		 --						_G.Auto_Farm = false
         --						_G.Chip = "Flame"
		 --						_G.AutoRaid = true
         --							local args = {
         --								[1] = "BlackbeardReward",
         --								[2] = "DragonClaw",
         --								[3] = "1"
         --							}
         --						
         --							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
         --							local args = {
         --								[1] = "BlackbeardReward",
         --								[2] = "DragonClaw",
         --								[3] = "2"
         --							}
         --						
         --							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
         --					end
         --				end
       --  			end
    --     		end
  --       	end)
 --       end) 
    

Wapon = {}
for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do  
    if v:IsA("Tool") then
        table.insert(Wapon ,v.Name)
    end
end
for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do  
    if v:IsA("Tool") then
        table.insert(Wapon, v.Name)
    end
end

local SelectWeapona = section1:addDropdown("Select Weapon",Wapon,function(Value)
    _G.SelectWeapon = Value
    _G.SelectToolWeaponOld = Value
end)

section1:addButton("Refresh Weapon",function()
    table.clear(Wapon)
    for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
       if v:IsA("Tool") then
          table.insert(Wapon,v.Name)
       end
    end
    for i,v in pairs(game.Players.LocalPlayer.Character:GetChildren()) do
       if v:IsA("Tool") then
          table.insert(Wapon,v.Name)
       end
    end
 end)

-- second page
local page = venyx:addPage("Stat", 5012544693)
local section4 = page:addSection("Stat")


section4:addToggle("Melee", false, function(value)
    melee = value  
end)
section4:addToggle("Defense", false, function(value)
    defense = value
end)
section4:addToggle("Sword", false, function(value)
    sword = value
end)
section4:addToggle("Gun",false, function(value)
    gun = value
end)
section4:addToggle("Devil Fruit", false, function(value)
    demonfruit = value
end)
section4:addSlider("Point", 1, 1, 6000, function(a) 
    PointStats = a 
end)
spawn(function()
    while wait() do
       if game.Players.localPlayer.Data.Points.Value then
          if melee then
             local args = {
             [1] = "AddPoint",
             [2] = "Melee",
             [3] = PointStats
             }
             game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
          end 
          if defense then
             local args = {
             [1] = "AddPoint",
             [2] = "Defense",
             [3] = PointStats
             }
             game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
          end 
          if sword then
             local args = {
             [1] = "AddPoint",
             [2] = "Sword",
             [3] = PointStats
             }
             game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
          end 
          if gun then
             local args = {
             [1] = "AddPoint",
             [2] = "Gun",
             [3] = PointStats
             }
             game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
          end 
          if demonfruit then
             local args = {
             [1] = "AddPoint",
             [2] = "Demon Fruit",
             [3] = PointStats
             }
             game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
          end
       end
    end
 end)

--Teleport page
local page = venyx:addPage("Teleport ", 5012544693)
local section1 = page:addSection("Teleport")

function tweenteleoirtzz(XXXXx,Arfggg)
	local Distance = (XXXXx - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
	local Speed = 300
	game:GetService("TweenService"):Create(
	game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart,
	TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
	{CFrame = Arfggg}
	):Play()
	_G.NoClip = true
	wait(Distance/Speed)
	_G.NoClip = false
end

if Old_World then
   section1:addButton("Start Island",function()
      tweenteleoirtzz(Vector3.new(1071.2832, 16.3085976, 1426.86792),CFrame.new(1071.2832, 16.3085976, 1426.86792))
   end)
   section1:addButton("Marine Start",function()
     tweenteleoirtzz(Vector3.new(-2573.3374, 6.88881969, 2046.99817),CFrame.new(-2573.3374, 6.88881969, 2046.99817))
   end)
   section1:addButton("Middle Town",function()
     tweenteleoirtzz(Vector3.new(-655.824158, 7.88708115, 1436.67908),CFrame.new(-655.824158, 7.88708115, 1436.67908))
   end)
  section1:addButton("Jungle",function()
     tweenteleoirtzz(Vector3.new(-1249.77222, 11.8870859, 341.356476),CFrame.new(-1249.77222, 11.8870859, 341.356476))
   end)
   section1:addButton("Pirate Village",function()
     tweenteleoirtzz(Vector3.new(-1122.34998, 4.78708982, 3855.91992),CFrame.new(-1122.34998, 4.78708982, 3855.91992))
   end)
   section1:addButton("Desert",function()
     tweenteleoirtzz(Vector3.new(1094.14587, 6.47350502, 4192.88721),CFrame.new(1094.14587, 6.47350502, 4192.88721))
   end)
   section1:addButton("Frozen Village",function()
     tweenteleoirtzz(Vector3.new(1198.00928, 27.0074959, -1211.73376),CFrame.new(1198.00928, 27.0074959, -1211.73376))
   end)
   section1:addButton("MarineFord",function()
     tweenteleoirtzz(Vector3.new(-4505.375, 20.687294, 4260.55908),CFrame.new(-4505.375, 20.687294, 4260.55908))
   end)
   section1:addButton("Colosseum",function()
     tweenteleoirtzz(Vector3.new(-1428.35474, 7.38933945, -3014.37305),CFrame.new(-1428.35474, 7.38933945, -3014.37305))
   end)
   section1:addButton("Sky 1st Floor",function()
     tweenteleoirtzz(Vector3.new(-4970.21875, 717.707275, -2622.35449),CFrame.new(-4970.21875, 717.707275, -2622.35449))
   end)
   section1:addButton("Sky 2st Floor",function()
     tweenteleoirtzz(Vector3.new(-4813.0249, 903.708557, -1912.69055),CFrame.new(-4813.0249, 903.708557, -1912.69055))
   end)
   section1:addButton("Sky 3st Floor",function()
     tweenteleoirtzz(Vector3.new(-7952.31006, 5545.52832, -320.704956),CFrame.new(-7952.31006, 5545.52832, -320.704956))
   end)
   section1:addButton("Prison",function()
     tweenteleoirtzz(Vector3.new(4854.16455, 5.68742752, 740.194641),CFrame.new(4854.16455, 5.68742752, 740.194641))
   end)
   section1:addButton("Magma Village",function()
     tweenteleoirtzz(Vector3.new(-5231.75879, 8.61593437, 8467.87695),CFrame.new(-5231.75879, 8.61593437, 8467.87695))
   end)
   section1:addButton("UndeyWater City",function()
     tweenteleoirtzz(Vector3.new(61163.8516, 11.7796879, 1819.78418),CFrame.new(61163.8516, 11.7796879, 1819.78418))
   end)
   section1:addButton("Fountain City",function()
     tweenteleoirtzz(Vector3.new(5132.7124, 4.53632832, 4037.8562),CFrame.new(5132.7124, 4.53632832, 4037.8562))
   end)
   section1:addButton("House Cyborg's",function()
     tweenteleoirtzz(Vector3.new(6262.72559, 71.3003616, 3998.23047),CFrame.new(6262.72559, 71.3003616, 3998.23047))
   end)
   section1:addButton("Shank's Room",function()
     tweenteleoirtzz(Vector3.new(-1442.16553, 29.8788261, -28.3547478),CFrame.new(-1442.16553, 29.8788261, -28.3547478))
   end)
   section1:addButton("Mob Island",function()
     tweenteleoirtzz(Vector3.new(-2850.20068, 7.39224768, 5354.99268),CFrame.new(-2850.20068, 7.39224768, 5354.99268))
   end)
end
if New_World then
   section1:addButton("Dock",function()
     tweenteleoirtzz(Vector3.new(82.9490662, 18.0710983, 2834.98779),CFrame.new(82.9490662, 18.0710983, 2834.98779))
   end)
   section1:addButton("Kingdom of Rose",function()
     tweenteleoirtzz(Vector3.new(-394.983521, 118.503128, 1245.8446),CFrame.new(-394.983521, 118.503128, 1245.8446))
   end)
   section1:addButton("Mansion",function()
     tweenteleoirtzz(Vector3.new(-390.096313, 331.886475, 673.464966),CFrame.new(-390.096313, 331.886475, 673.464966))
   end)
   section1:addButton("Flamingo Room",function()
     tweenteleoirtzz(Vector3.new(2302.19019, 15.1778421, 663.811035),CFrame.new(2302.19019, 15.1778421, 663.811035))
   end)
   section1:addButton("Green Zone",function()
     tweenteleoirtzz(Vector3.new(-2372.14697, 72.9919434, -3166.51416),CFrame.new(-2372.14697, 72.9919434, -3166.51416))
   end)
   section1:addButton("Cafe",function()
     tweenteleoirtzz(Vector3.new(-385.250916, 73.0458984, 297.388397),CFrame.new(-385.250916, 73.0458984, 297.388397))
   end)
   section1:addButton("Factroy",function()
     tweenteleoirtzz(Vector3.new(430.42569, 210.019623, -432.504791),CFrame.new(430.42569, 210.019623, -432.504791))
   end)
   section1:addButton("Colosseum",function()
     tweenteleoirtzz(Vector3.new(-1836.58191, 44.5890656, 1360.30652),CFrame.new(-1836.58191, 44.5890656, 1360.30652))
   end)
   section1:addButton("GraveIsland",function()
     tweenteleoirtzz(Vector3.new(-5411.47607, 48.8234024, -721.272522),CFrame.new(-5411.47607, 48.8234024, -721.272522))
   end)
   section1:addButton("Snow Mountain",function()
     tweenteleoirtzz(Vector3.new(511.825226, 401.765198, -5380.396),CFrame.new(511.825226, 401.765198, -5380.396))
   end)
   section1:addButton("Cold Island",function()
     tweenteleoirtzz(Vector3.new(-6026.96484, 14.7461271, -5071.96338),CFrame.new(-6026.96484, 14.7461271, -5071.96338))
   end)
   section1:addButton("Hot Island",function()
     tweenteleoirtzz(Vector3.new(-5478.39209, 15.9775667, -5246.9126),CFrame.new(-5478.39209, 15.9775667, -5246.9126))
   end)
   section1:addButton("Cursed Ship",function()
     tweenteleoirtzz(Vector3.new(902.059143, 124.752518, 33071.8125),CFrame.new(902.059143, 124.752518, 33071.8125))
   end)
   section1:addButton("IceCastle",function()
     tweenteleoirtzz(Vector3.new(5400.40381, 28.21698, -6236.99219),CFrame.new(5400.40381, 28.21698, -6236.99219))
   end)
   section1:addButton("Forgotten Island",function()
     tweenteleoirtzz(Vector3.new(-3043.31543, 238.881271, -10191.5791),CFrame.new(-3043.31543, 238.881271, -10191.5791))
   end)
   section1:addButton("Usoapp Island",function()
     tweenteleoirtzz(Vector3.new(4748.78857, 8.35370827, 2849.57959),CFrame.new(4748.78857, 8.35370827, 2849.57959))
   end)
   section1:addButton("Minisky Island",function()
     tweenteleoirtzz(Vector3.new(-260.358917, 49325.7031, -35259.3008),CFrame.new(-260.358917, 49325.7031, -35259.3008))
   end)
end

if SeaThird_World then

   section1:addButton("Port Town",function()
     tweenteleoirtzz(Vector3.new(-610.309692, 57.8323097, 6436.33594),CFrame.new(-610.309692, 57.8323097, 6436.33594))
   end)
  section1:addButton("Hydra Island",function()
     tweenteleoirtzz(Vector3.new(5229.99561, 603.916565, 345.154022),CFrame.new(5229.99561, 603.916565, 345.154022, -0.137452736))
   end)
   section1:addButton("Great Tree",function()
     tweenteleoirtzz(Vector3.new(2174.94873, 28.7312393, -6728.83154),CFrame.new(2174.94873, 28.7312393, -6728.83154))
   end)
   section1:addButton("Castle on the Sea",function()
     tweenteleoirtzz(Vector3.new(-5477.62842, 313.794739, -2808.4585),CFrame.new(-5477.62842, 313.794739, -2808.4585))
   end)
  section1:addButton("Floating Turtle",function()
     tweenteleoirtzz(Vector3.new(-10919.2998, 331.788452, -8637.57227),CFrame.new(-10919.2998, 331.788452, -8637.57227))
   end)
   section1:addButton("Mansion",function()
     tweenteleoirtzz(Vector3.new(-12553.8125, 332.403961, -7621.91748),CFrame.new(-12553.8125, 332.403961, -7621.91748))
   end)
   section1:addButton("Secret Temple",function()
     tweenteleoirtzz(Vector3.new(5217.35693, 6.56511116, 1100.88159, 0.00408430398),CFrame.new(5217.35693, 6.56511116, 1100.88159, 0.00408430398))
   end)
   section1:addButton("Friendly Arena",function()
     tweenteleoirtzz(Vector3.new(5220.28955, 72.8193436, -1450.86304),CFrame.new(5220.28955, 72.8193436, -1450.86304))
   end)
   section1:addButton("Beautiful Pirate Domain",function()
     tweenteleoirtzz(Vector3.new(5310.8095703125, 21.594484329224, 129.39053344727),CFrame.new(5310.8095703125, 21.594484329224, 129.39053344727))
   end)
      section1:addButton("Haunted Castle",function()
     tweenteleoirtzz(Vector3.new(-9506.1064453125, 142.13989257813, 5526.0405273438),CFrame.new(-9506.1064453125, 142.13989257813, 5526.0405273438))
  end)   
     section1:addButton("Peanut Island",function()
     tweenteleoirtzz(Vector3.new(-1973.15234, 198.272507, -10120.9932, -0.836014748, -7.87028824e-08, -0.548706949, -8.99818957e-08, 1, -6.33614761e-09, 0.548706949, 4.40765824e-08, -0.836014748),CFrame.new(-1973.15234, 198.272507, -10120.9932, -0.836014748, -7.87028824e-08, -0.548706949, -8.99818957e-08, 1, -6.33614761e-09, 0.548706949, 4.40765824e-08, -0.836014748))
    end)    
     section1:addButton("Ice Cream Island",function()
     tweenteleoirtzz(Vector3.new(-867.879028, 64.6137543, -10900.6338, -0.876459777, 3.93537369e-10, 0.481475055, -9.28089072e-09, 1, -1.77119563e-08, -0.481475055, -1.99923349e-08, -0.876459777),CFrame.new(-867.879028, 64.6137543, -10900.6338, -0.876459777, 3.93537369e-10, 0.481475055, -9.28089072e-09, 1, -1.77119563e-08, -0.481475055, -1.99923349e-08, -0.876459777))
   end)
end
         
-- fifth page
local page = venyx:addPage("Shop", 5012544693)
local section1 = page:addSection("Combat")
local section2 = page:addSection("Sword")
local section3 = page:addSection("Gun")
local section4 = page:addSection("Accessories")
local section5 = page:addSection("Ability")

section1:addButton("Black Leg",function()
			local args = {
				[1] = "BuyBlackLeg"
			}
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		end)

		section1:addButton("Electra",function()
			local args = {
				[1] = "BuyElectro"
			}
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		end)

		section1:addButton("Fishman Karate",function()
			local args = {
				[1] = "BuyFishmanKarate"
			}
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		end)

		section1:addButton("Dragon Claw",function()
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
		end)

		section1:addButton("Superhuman",function()
			local args = {
				[1] = "BuySuperhuman"
			}

			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		end)

		section1:addButton("Death Step",function()
			local args = {
				[1] = "BuyDeathStep"
			}

			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		end)

		section1:addButton("Shakman Karate",function()
			local args = {
				[1] = "BuySharkmanKarate",
				[2] = true
			}
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
			local args = {
				[1] = "BuySharkmanKarate"
			}
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		end)
		section1:addToggle("Auto Buy Haki Color",false,function(value)

			_G.buy = value

			while _G.buy do
				wait()

				local A_1 = "ColorsDealer"
				local A_2 = "1"
				local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
				Event:InvokeServer(A_1, A_2)

				local A_1 = "ColorsDealer"
				local A_2 = "2"
				local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
				Event:InvokeServer(A_1, A_2)

				local A_1 = "ColorsDealer"
				local A_2 = "3"
				local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
				Event:InvokeServer(A_1, A_2)

				local A_1 = "ColorsDealer"
				local A_2 = "4"
				local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
				Event:InvokeServer(A_1, A_2)

				local A_1 = "ColorsDealer"
				local A_2 = "5"
				local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
				Event:InvokeServer(A_1, A_2)

				local A_1 = "ColorsDealer"
				local A_2 = "6"
				local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
				Event:InvokeServer(A_1, A_2)

				local A_1 = "ColorsDealer"
				local A_2 = "7"
				local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
				Event:InvokeServer(A_1, A_2)

				local A_1 = "ColorsDealer"
				local A_2 = "8"
				local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
				Event:InvokeServer(A_1, A_2)

				local A_1 = "ColorsDealer"
				local A_2 = "9"
				local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
				Event:InvokeServer(A_1, A_2)

				local A_1 = "ColorsDealer"
				local A_2 = "10"
				local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
				Event:InvokeServer(A_1, A_2)

				local A_1 = "ColorsDealer"
				local A_2 = "11"
				local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
				Event:InvokeServer(A_1, A_2)

				local A_1 = "ColorsDealer"
				local A_2 = "12"
				local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
				Event:InvokeServer(A_1, A_2)

				local A_1 = "ColorsDealer"
				local A_2 = "13"
				local Event = game:GetService("ReplicatedStorage").Remotes["CommF_"]
				Event:InvokeServer(A_1, A_2)

			end

		end)

section5:addButton("Open Devil Shop",function()
			local args = {
				[1] = "GetFruits"
			}
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
			game.Players.localPlayer.PlayerGui.Main.FruitShop.Visible = true
		end)

		section5:addButton("Open Inventory",function()
			local args = {
				[1] = "getInventoryWeapons"
			}
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
			game.Players.localPlayer.PlayerGui.Main.Inventory.Visible = true
		end)

		section5:addButton("Open Color Haki",function()
			game.Players.localPlayer.PlayerGui.Main.Colors.Visible = true
		end)

		section5:addButton("Open Title Name",function()
			local args = {
				[1] = "getTitles"
			}
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
			game.Players.localPlayer.PlayerGui.Main.Titles.Visible = true
		end)

section5:addButton("Buso", function()
local args = {
    [1] = "BuyHaki",
    [2] = "Buso",
}

game:GetService("ReplicatedStorage").Remotes["CommF_"]:InvokeServer(unpack(args))
	print("Clicked")
end)

section5:addButton("Geppo", function()
	
local args = {
    [1] = "BuyHaki",
    [2] = "Geppo",
}

game:GetService("ReplicatedStorage").Remotes["CommF_"]:InvokeServer(unpack(args))
end)

section5:addButton("Soru", function()
local args = {
    [1] = "BuyHaki",
    [2] = "Soru",
}

game:GetService("ReplicatedStorage").Remotes["CommF_"]:InvokeServer(unpack(args))
end)

section5:addButton("Ken", function()
local args = {
    [1] = "BuyKen",
    [2] = "Ken",
}

game:GetService("ReplicatedStorage").Remotes["CommF_"]:InvokeServer(unpack(args))
end)

local page = venyx:addPage("Raid ", 5012544693)
local section1 = page:addSection("Raid Menu")
local section2 = page:addSection("Auto Raids")

section1:addDropdown("Raid",{"Flame","Ice","Light","Dark","Rumble","String","Magma","Human: Budda","Sand"},function(t)
	_G.Chip = t
end)

section1:addToggle("Auto Buy Chip", _G.AutoBuyChip,function(value)
	_G.AutoBuyChip = value
end)

spawn(function()
	pcall(function()
		while wait() do
			if _G.AutoBuyChip then
				if not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Special Microchip") or not game:GetService("Players").LocalPlayer.Character:FindFirstChild("Special Microchip") then
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("RaidsNpc","Select",_G.Chip)
				end
			end
		end
	end)
end)

section1:addToggle("Kill Aura", _G.KillAura, function(value)
	_G.KillAura = value
end)

spawn(function()
	pcall(function() 
		while wait() do
			if _G.KillAura then
				for i,v in pairs(game.Workspace.Enemies:GetDescendants()) do
					if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
						pcall(function()
							repeat wait()
								sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
								v.Humanoid.Health = 0
								v.HumanoidRootPart.CanCollide = false
								v.HumanoidRootPart.Size = Vector3.new(60,60,60)
								v.HumanoidRootPart.Transparency = 1
							until not _G.KillAura or not v.Parent or v.Humanoid.Health <= 0
						end)
					end
				end
			end
		end
	end)
end)

section1:addToggle("Auto Next Island", _G.NextIsland, function(value)
	_G.NextIsland = value
end)

spawn(function()
	pcall(function()
		while wait(.1) do
			if _G.NextIsland then
				if game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") then
					TP(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5").CFrame*CFrame.new(0,70,0))
				elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") then
					TP(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4").CFrame*CFrame.new(0,70,0))
				elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") then
					TP(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3").CFrame*CFrame.new(0,70,0))
				elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") then
					TP(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2").CFrame*CFrame.new(0,70,0))
				elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
					TP(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1").CFrame*CFrame.new(0,70,0))
				end
			end
		end
	end)
end)

section1:addToggle("Auto Awake",_G.Awakener, function(value)
	_G.Awakener = value
end)

spawn(function()
	while wait(.1) do
		if _G.Awakener then
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Awakener","Check")
			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Awakener","Awaken")
		end
	end
end)

if New_World then
	section2:addButton("Teleport to Lab",function()
		TP(CFrame.new(-6438.73535, 250.645355, -4501.50684))
	end)
end
if Third_World then
	section2:addButton("Teleport to Lab",function()
		TP(CFrame.new(-5017.40869, 314.844055, -2823.0127, -0.925743818, 4.48217499e-08, -0.378151238, 4.55503146e-09, 1, 1.07377559e-07, 0.378151238, 9.7681621e-08, -0.925743818))
	end)
end

if New_World then
	section2:addButton("Awakening Room",function()
		TP(CFrame.new(266.227783, 1.39509034, 1857.00732))
	end)

elseif SeaThird_World then
	section2:addButton("Awakening Room",function()
		TP(CFrame.new(-11571.440429688, 49.172668457031, -7574.7368164062))
	end)
end


-- eighth page	
local page = venyx:addPage("Setting ", 5012544693)
local section1 = page:addSection("UI Toggle")

section1:addKeybind("Toggle Keybind", Enum.KeyCode.RightControl, function()
    print("Activated Keybind")
    venyx:toggle()
end, function()
    print("Changed Keybind")
end)

-- ninth page
local theme = venyx:addPage("Theme", 5012544693)
local colors = theme:addSection("Colors")

for theme, color in pairs(themes) do -- all in one theme changer, i know, im cool
    colors:addColorPicker(theme, color, function(color3)
        venyx:setTheme(theme, color3)
    end)
end


-- load
venyx:SelectPage(venyx.pages[1], true)
