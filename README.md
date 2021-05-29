-- Gui to Lua
-- Version: 3.2

-- Instances:

local LoginMenu = Instance.new("ScreenGui")
local LoginFrame = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local UIGradient = Instance.new("UIGradient")
local Login = Instance.new("TextButton")
local UICorner_2 = Instance.new("UICorner")
local TextLAbel = Instance.new("TextLabel")
local Menu = Instance.new("Frame")
local UICorner_3 = Instance.new("UICorner")
local UIGradient_2 = Instance.new("UIGradient")
local Aimbot = Instance.new("TextButton")
local Fly = Instance.new("TextButton")
local Noclip = Instance.new("TextButton")
local Esp = Instance.new("TextButton")
local SoftAim = Instance.new("TextButton")
local InfJump = Instance.new("TextButton")
local merijncat = Instance.new("TextLabel")
local WelcometoMintyHub = Instance.new("TextLabel")
local UICorner_4 = Instance.new("UICorner")
local UIGradient_3 = Instance.new("UIGradient")

--Properties:

LoginMenu.Name = "LoginMenu"
LoginMenu.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
LoginMenu.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

LoginFrame.Name = "LoginFrame"
LoginFrame.Parent = LoginMenu
LoginFrame.BackgroundColor3 = Color3.fromRGB(134, 255, 120)
LoginFrame.Position = UDim2.new(0.366389096, 0, 0.262798637, 0)
LoginFrame.Size = UDim2.new(0, 352, 0, 416)
LoginFrame.Active = true
LoginFrame.draggble = true

UICorner.Parent = LoginFrame

UIGradient.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(0, 170, 255)), ColorSequenceKeypoint.new(0.11, Color3.fromRGB(31, 180, 255)), ColorSequenceKeypoint.new(0.92, Color3.fromRGB(233, 247, 255)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))}
UIGradient.Parent = LoginFrame

Login.Name = "Login"
Login.Parent = LoginFrame
Login.BackgroundColor3 = Color3.fromRGB(4, 255, 0)
Login.Position = UDim2.new(0.164772734, 0, 0.384615362, 0)
Login.Size = UDim2.new(0, 235, 0, 95)
Login.Font = Enum.Font.SciFi
Login.Text = "Login"
Login.TextColor3 = Color3.fromRGB(0, 0, 0)
Login.TextScaled = true
Login.TextSize = 14.000
Login.TextWrapped = true

UICorner_2.Parent = Login

TextLAbel.Name = "TextLAbel"
TextLAbel.Parent = LoginFrame
TextLAbel.BackgroundColor3 = Color3.fromRGB(0, 255, 217)
TextLAbel.BorderSizePixel = 3
TextLAbel.LayoutOrder = -10
TextLAbel.Size = UDim2.new(0, 352, 0, 57)
TextLAbel.Font = Enum.Font.SourceSans
TextLAbel.Text = "Welcome To Minty Hub Login If You Want To Login"
TextLAbel.TextColor3 = Color3.fromRGB(0, 0, 0)
TextLAbel.TextSize = 30.000
TextLAbel.TextWrapped = true

Menu.Name = "Menu"
Menu.Parent = LoginMenu
Menu.BackgroundColor3 = Color3.fromRGB(134, 255, 142)
Menu.Position = UDim2.new(0.265707791, 0, 0.310580194, 0)
Menu.Size = UDim2.new(0, 619, 0, 332)
Menu.Visible = false
LoginFrame.Active = true
LoginFrame.draggble = true

UICorner_3.Parent = Menu

UIGradient_2.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(0, 170, 255)), ColorSequenceKeypoint.new(0.17, Color3.fromRGB(22, 177, 255)), ColorSequenceKeypoint.new(0.58, Color3.fromRGB(0, 255, 255)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(255, 255, 255))}
UIGradient_2.Parent = Menu

Aimbot.Name = "Aimbot"
Aimbot.Parent = Menu
Aimbot.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Aimbot.BackgroundTransparency = 1.000
Aimbot.Position = UDim2.new(0.0694668815, 0, 0.204819277, 0)
Aimbot.Size = UDim2.new(0, 200, 0, 50)
Aimbot.Font = Enum.Font.SourceSans
Aimbot.Text = "Aimbot"
Aimbot.TextColor3 = Color3.fromRGB(0, 0, 0)
Aimbot.TextScaled = true
Aimbot.TextSize = 14.000
Aimbot.TextWrapped = true
Aimbot.MouseButton1Down:connect(function()
	pcall(function()
		local espcolor = Color3.fromRGB(140, 69, 102)
		local wallhack_esp_transparency = .4
		local gui_hide_button = {Enum.KeyCode.LeftControl, "h"}
		local plrs = game:GetService("Players")
		local lplr = game:GetService("Players").LocalPlayer
		local TeamBased = true ; local teambasedswitch = "o"
		local presskeytoaim = true; local aimkey = "e"
		aimbothider = false; aimbothiderspeed = .5
		local Aim_Assist = false ; Aim_Assist_Key = {Enum.KeyCode.LeftControl, "z"}
		local espupdatetime = 5; autoesp = false
		local abs = math.abs
		local mouselock = false
		local canaimat = true
		local lockaim = true; local lockangle = 5
		local ver = "2"
		local cam = game.Workspace.CurrentCamera
		local BetterDeathCount = true


		local mouse = lplr:GetMouse()
		local switch = false
		local key = "k"
		local aimatpart = nil




		local Gui = Instance.new("ScreenGui")
		local Move = Instance.new("Frame")
		local Main = Instance.new("Frame")
		local EspStatus = Instance.new("TextLabel")
		local st1 = Instance.new("TextLabel")
		local st1_2 = Instance.new("TextLabel")
		local st1_3 = Instance.new("TextLabel")
		local Name = Instance.new("TextLabel")
		--Properties:

		Gui.Parent = plrs.LocalPlayer:WaitForChild("PlayerGui")



		local gotstring = 0
		local function getrandomstring()
			gotstring = gotstring+666
			local str = ""
			local randomstring = {"a", "b", "c", "d", "e", "f", "g", "h", "i", "g", "k", "l", "m", "o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z",
				"?","?","?","?","?","?","?","?","?","?","?","?","?","?","?","?","?","?","?","?","?","?","?","?","?","?","?","?","?","?", "`", "$", 
				"0","1","2","3","4","5","6","7","8","9", }
			local counting123 = 0
			for i, v in ipairs(randomstring) do
				counting123 = i
			end
			do
				math.randomseed(tick()+gotstring)
				for i = 3, math.random(1,100) do
					math.randomseed(i+tick()+gotstring)

					local oneortwo = math.random(1,2)
					if oneortwo == 2 then
						math.randomseed(i+tick()+gotstring)
						str = str..""..randomstring[math.random(1, counting123)]
					else
						math.randomseed(i+tick()+gotstring)
						str = str..""..string.upper(randomstring[math.random(1, counting123)])
					end

				end
			end
			return str
		end
		local mousedown = false
		local isonmovething = false
		local mouseoffset = Vector2.new()
		local mousedown = false




		Gui.Name = getrandomstring()

		Move.Name = getrandomstring()
		Move.Draggable = true
		Move.Parent = Gui
		Move.BackgroundColor3 = Color3.new(0.0431373, 1, 0.0745098)
		Move.BackgroundTransparency = 0.40000000596046
		Move.BorderSizePixel = 0
		Move.Position = UDim2.new(0.5, 0,0.018, 0)
		Move.Size = UDim2.new(0.2, 0, 0.0320388414, 0)

		Move.MouseEnter:Connect(function()

			isonmovething = true

		end)
		Move.MouseLeave:Connect(function()

			isonmovething = mousedown and true or false
		end)
		mouse.Button1Down:connect(function()
			mousedown = true
			mouseoffset = Move.AbsolutePosition - Vector2.new(mouse.X, mouse.Y)
		end)
		mouse.Button1Up:connect(function()
			mousedown = false
		end)

		mouse.Move:Connect(function()
			if isonmovething == true and mousedown then
				Move.Position = UDim2.new(0, mouseoffset.X + mouse.X, 0, mouseoffset.Y + mouse.Y)
			end
		end)

		Main.Name = getrandomstring()
		Main.Parent = Move
		Main.BackgroundColor3 = Color3.new(0.176471, 0.176471, 0.176471)
		Main.BackgroundTransparency = 0.69999998807907
		Main.Position = UDim2.new(0, 0, 0.995670795, 0)
		Main.Size = UDim2.new(1.0000006, 0, 11.2, 0)

		EspStatus.Name = getrandomstring()
		EspStatus.Parent = Main
		EspStatus.BackgroundColor3 = Color3.new(1, 1, 1)
		EspStatus.BackgroundTransparency = 1
		EspStatus.Size = UDim2.new(0.272955924, 0, 0.161862016, 0)
		EspStatus.Font = Enum.Font.ArialBold
		EspStatus.Text = "Press T to update Esp"
		EspStatus.TextColor3 = Color3.new(0.0431373, 1, 0.0745098)
		EspStatus.TextScaled = true
		EspStatus.TextSize = 14
		EspStatus.TextWrapped = true

		st1.Name = getrandomstring()
		st1.Parent = Main
		st1.BackgroundColor3 = Color3.new(1, 1, 1)
		st1.BackgroundTransparency = 1
		st1.Position = UDim2.new(0.271787882, 0, 0, 0)
		st1.Size = UDim2.new(0.728211343, 0, 0.161862016, 0)
		st1.Font = Enum.Font.ArialBold
		st1.Text = "Press "..aimkey.." to lock on a person inside ur view"
		st1.TextColor3 = Color3.new(0.0431373, 1, 0.0745098)
		st1.TextScaled = true
		st1.TextSize = 14
		st1.TextWrapped = true

		st1_2.Name = getrandomstring()
		st1_2.Parent = Main
		st1_2.BackgroundColor3 = Color3.new(1, 1, 1)
		st1_2.BackgroundTransparency = 1
		st1_2.Position = UDim2.new(0, 0, 0.375590861, 0)
		st1_2.Size = UDim2.new(0.999999881, 0, 0.161862016, 0)
		st1_2.Font = Enum.Font.ArialBold
		st1_2.Text = "Press L to enable esp loop. Press Y to disable/enable aimbot hider"
		st1_2.TextColor3 = Color3.new(0.0431373, 1, 0.0745098)
		st1_2.TextScaled = true
		st1_2.TextSize = 14
		st1_2.TextWrapped = true

		local aimbothiderbox = Instance.new("TextBox")
		aimbothiderbox.Name = getrandomstring()
		aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." off"
		aimbothiderbox.Size = UDim2.new(1, 0,0.162, 0)
		aimbothiderbox.TextScaled = true
		aimbothiderbox.TextColor3 =Color3.fromRGB(255, 0, 0)
		aimbothiderbox.Position = UDim2.new(0, 0,0.853, 0)
		aimbothiderbox.BackgroundTransparency = 1
		aimbothiderbox.Parent = Main

		st1_3.Name = getrandomstring()
		st1_3.Parent = Main
		st1_3.BackgroundColor3 = Color3.new(1, 1, 1)
		st1_3.BackgroundTransparency = 1
		st1_3.Position = UDim2.new(0, 0, 0.18558608, 0)
		st1_3.Size = UDim2.new(0.999999881, 0, 0.161862016, 0)
		st1_3.Font = Enum.Font.ArialBold
		st1_3.Text = "Press O to change team based mode"
		st1_3.TextColor3 = Color3.new(0.0431373, 1, 0.0745098)
		st1_3.TextScaled = true
		st1_3.TextSize = 14
		st1_3.TextWrapped = true
		local teambasedstatus = st1_3:Clone()
		teambasedstatus.Parent = Main
		teambasedstatus.TextScaled = true
		teambasedstatus.Position = UDim2.new(0, 0,.7, 0)
		teambasedstatus.Size = UDim2.new(1, 0,.1, 0)
		teambasedstatus.Name = getrandomstring()
		teambasedstatus.Text = "Team Based: "..tostring(TeamBased)
		local espstatustext = teambasedstatus:Clone()
		espstatustext.Name = getrandomstring()
		espstatustext.Position = UDim2.new(0, 0,0.58, 0)
		espstatustext.Text = "Esp loop :"..tostring(autoesp)
		espstatustext.Parent = Main
		local hide = Instance.new("TextButton")
		hide.Text = "_"
		hide.BackgroundTransparency = 1
		hide.TextScaled = true
		hide.TextWrapped = true
		hide.Size = UDim2.new(0.1, 0,1, 0)
		hide.Position = UDim2.new(0.9, 0,-0.15, 0)
		hide.Name = getrandomstring()
		hide.Parent = Move
		Name.Name = getrandomstring()
		Name.Parent = Move
		Name.BackgroundColor3 = Color3.new(1, 1, 1)
		Name.BackgroundTransparency = 1
		Name.Size = UDim2.new(0.838, 0, 1, 0)
		Name.Font = Enum.Font.Arial
		Name.Text = "FPS gui v"..ver
		Name.TextColor3 = Color3.new(0, 0, 0)
		Name.TextScaled = true
		Name.TextSize = 14
		Name.TextWrapped = true
		Name.TextXAlignment = Enum.TextXAlignment.Left
		local scr = Instance.new("ScrollingFrame")
		scr.Size = Main.Size
		scr.Position = Main.Position
		scr.ScrollBarThickness = 0
		scr.BackgroundTransparency = 1
		scr.Name = getrandomstring()
		Main.Size = UDim2.new(1, 0, 1, 0)
		Main.Position = UDim2.new(0,0,0,0)
		Main.Parent = scr
		scr.Parent = Move
		startpos = Main.Position
		Move.Active = true

		-- Scripts:
		hided = false
		hide.MouseButton1Click:Connect(function()
			if hided == false then
				hided = true
				Main:TweenPosition(UDim2.new(0, 0, -1.5, 0))
			else
				hided = false
				Main:TweenPosition(startpos)
			end
		end)


		aimbothiderbox.FocusLost:Connect(function()
			local numb = tonumber(aimbothiderbox.Text)
			if aimbothider == true then
				aimbothiderbox.TextColor3 =Color3.fromRGB(11, 255, 19)
			else
				aimbothiderbox.TextColor3 =Color3.fromRGB(255, 0, 0)
			end
			if numb ~= nil then
				aimbothiderspeed = numb
				if aimbothider == true then
					aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." on"
				else
					aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." off"
				end
			else
				if aimbothider == true then
					aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." on"
				else
					aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." off"
				end
			end
		end)


		local plrsforaim = {}


		Move.Draggable = true
		Gui.ResetOnSpawn = false
		--Gui.Name = "Chat"
		Gui.DisplayOrder = 999
		if not game:GetService("CoreGui") then
			Gui.Parent = plrs.LocalPlayer.PlayerGui
		else
			Gui.Parent = game:GetService("CoreGui")
		end





		f = {}
		local espforlder
		local partconverter = Instance.new("Part")

		f.addesp = function()
			pcall(function()
				--print("ESP ran")
				if espforlder then
					espforlder:Destroy()
					espforlder = Instance.new("Folder")
					espforlder.Parent = game.Workspace.CurrentCamera
				else
					espforlder = Instance.new("Folder")
					espforlder.Parent = game.Workspace.CurrentCamera
				end
				for i, v in pairs(espforlder:GetChildren()) do
					v:Destroy()
				end
				for _, plr in pairs(plrs:GetChildren()) do
					if plr.Character and plr.Character.Humanoid.Health > 0 and plr.Name ~= lplr.Name then
						if TeamBased == true then
							if plr.Team.Name ~= plrs.LocalPlayer.Team.Name  then
								local e = espforlder:FindFirstChild(plr.Name)
								if not e then
									local fold = Instance.new("Folder", espforlder)
									fold.Name = plr.Name

									--partconverter.BrickColor = plr.Team.Color
									--local teamc = partconverter.Color
									for i, p in pairs(plr.Character:GetChildren()) do
										if p:IsA("BasePart") and p.Name ~= "HumanoidRootPart" then
											local urmom = Instance.new("BoxHandleAdornment")
											urmom.ZIndex = 10
											urmom.AlwaysOnTop = true
											urmom.Color3 = espcolor
											urmom.Size = p.Size
											urmom.Adornee = p
											urmom.Name = tick().." Ur mom has big gay"
											urmom.Transparency = wallhack_esp_transparency
											urmom.Parent = fold

										end
									end
									plr.Character.Humanoid.Died:Connect(function()
										fold:Destroy()
									end)
								end
							end
						else
							local e = espforlder:FindFirstChild(plr.Name)
							if not e then
								local fold = Instance.new("Folder", espforlder)
								fold.Name = plr.Name

								--partconverter.BrickColor = plr.Team.Color
								--local teamc = Move.BackgroundColor3
								for i, p in pairs(plr.Character:GetChildren()) do
									if p:IsA("BasePart") and p.Name ~= "HumanoidRootPart" then
										local urmom = Instance.new("BoxHandleAdornment")
										urmom.ZIndex = 10
										urmom.AlwaysOnTop = true
										urmom.Color3 = espcolor
										urmom.Size = p.Size
										urmom.Adornee = p
										urmom.Name = tick().." Ur mom has big gay"
										urmom.Transparency = wallhack_esp_transparency
										urmom.Parent = fold
									end
								end
								plr.Character.Humanoid.Died:Connect(function()
									fold:Destroy()
								end)
							end
						end


					end
				end
			end)
		end
		local uis = game:GetService("UserInputService")
		local bringall = false
		local hided2 = false
		mouse.KeyDown:Connect(function(a)
			if a == "t" then
				--print("worked1")
				f.addesp()
			elseif a == gui_hide_button[2] and uis:IsKeyDown(gui_hide_button[1]) then
				if hided2 == false then
					hided2 = true
					autoesp =false
					if espforlder then
						espforlder:Destroy()
					end
					Gui.Enabled = false
				else
					Gui.Enabled = true
					hided2 = false
				end
			elseif a == "u" then
				if mouselock == false then
					mouselock = true
				else
					mouselock = false
				end
			elseif a == "y" then
				if aimbothider == false then
					aimbothider = true
					if aimbothider == true then
						aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." on"
					else
						aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." off"
					end
				else

					aimbothider = false
					if aimbothider == true then
						aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." on"
					else
						aimbothiderbox.Text = "Speed :"..tostring(aimbothiderspeed).." off"
					end
				end
				if aimbothider == true then
					aimbothiderbox.TextColor3 =Color3.fromRGB(11, 255, 19)
				else
					aimbothiderbox.TextColor3 =Color3.fromRGB(255, 0, 0)
				end
			elseif a == "l" then
				if autoesp == false then
					autoesp = true
				else
					autoesp = false
				end
			elseif a == Aim_Assist_Key[2] and uis:IsKeyDown(Aim_Assist_Key[1]) then
				if Aim_Assist == true then
					Aim_Assist = false
					--print("disabled")
				else
					Aim_Assist = true
				end
			end
			if a == "j" then
				if mouse.Target then
					mouse.Target:Destroy()
				end
			end
			if a == key then
				if switch == false then
					switch = true
				else
					switch = false
					if aimatpart ~= nil then
						aimatpart = nil
					end
				end
			elseif a == teambasedswitch then
				if TeamBased == true then
					TeamBased = false
					teambasedstatus.Text = "Team Based: "..tostring(TeamBased)
				else
					TeamBased = true
					teambasedstatus.Text = "Team Based: "..tostring(TeamBased)
				end
			elseif a == aimkey then
				if not aimatpart then
					local maxangle = math.rad(20)
					for i, plr in pairs(plrs:GetChildren()) do
						if plr.Name ~= lplr.Name and plr.Character and plr.Character.Head and plr.Character.Humanoid and plr.Character.Humanoid.Health > 1 then
							if TeamBased == true then
								if plr.Team.Name ~= lplr.Team.Name then
									local an = checkfov(plr.Character.Head)
									if an < maxangle then
										maxangle = an
										aimatpart = plr.Character.Head
									end
								end
							else
								local an = checkfov(plr.Character.Head)
								if an < maxangle then
									maxangle = an
									aimatpart = plr.Character.Head
								end
								--print(plr)
							end
							local old = aimatpart
							plr.Character.Humanoid.Died:Connect(function()
								--print("died")
								if aimatpart and aimatpart == old then
									aimatpart = nil
								end
							end)

						end
					end
				else
					aimatpart = nil
					canaimat = false
					delay(1.1, function()
						canaimat = true
					end)
				end
			end
		end)

		function getfovxyz (p0, p1, deg)
			local x1, y1, z1 = p0:ToOrientation()
			local cf = CFrame.new(p0.p, p1.p)
			local x2, y2, z2 = cf:ToOrientation()
			local d = math.deg
			if deg then
				return Vector3.new(d(x1-x2), d(y1-y2), d(z1-z2))
			else
				return Vector3.new((x1-x2), (y1-y2), (z1-z2))
			end
		end


		function aimat(part)
			if part then
				if aimbothider == true or Aim_Assist == true then
					cam.CFrame = cam.CFrame:Lerp(CFrame.new(cam.CFrame.p, part.CFrame.p), aimbothiderspeed)
				else

					cam.CFrame = CFrame.new(cam.CFrame.p, part.CFrame.p)
				end
			end
		end
		function checkfov (part)
			local fov = getfovxyz(game.Workspace.CurrentCamera.CFrame, part.CFrame)
			local angle = math.abs(fov.X) + math.abs(fov.Y)
			return angle
		end
		pcall(function()
			delay(0, function()
				while wait(.4) do
					if Aim_Assist and not aimatpart and canaimat and lplr.Character and lplr.Character.Humanoid and lplr.Character.Humanoid.Health > 0 then
						for i, plr in pairs(plrs:GetChildren()) do


							local minangle = math.rad(5.5)
							local lastpart = nil
							local function gg(plr)
								pcall(function()
									if plr.Name ~= lplr.Name and plr.Character and plr.Character.Humanoid and plr.Character.Humanoid.Health > 0 and plr.Character.Head then
										local raycasted = false
										local cf1 = CFrame.new(cam.CFrame.p, plr.Character.Head.CFrame.p) * CFrame.new(0, 0, -4)
										local r1 = Ray.new(cf1.p, cf1.LookVector * 9000)
										local obj, pos = game.Workspace:FindPartOnRayWithIgnoreList(r1,  {lplr.Character.Head})
										local dist = (plr.Character.Head.CFrame.p- pos).magnitude
										if dist < 4 then
											raycasted = true
										end
										if raycasted == true then
											local an1 = getfovxyz(cam.CFrame, plr.Character.Head.CFrame)
											local an = abs(an1.X) + abs(an1.Y)
											if an < minangle then
												minangle = an
												lastpart = plr.Character.Head
											end
										end
									end
								end)
							end
							if TeamBased then
								if plr.Team.Name ~= lplr.Team.Name then
									gg(plr)
								end
							else
								gg(plr)
							end
							--print(math.deg(minangle))
							if lastpart then
								aimatpart = lastpart
								aimatpart.Parent.Humanoid.Died:Connect(function()
									if aimatpart == lastpart then
										aimatpart = nil
									end
								end)

							end
						end
					end
				end
			end)
		end)
		local oldheadpos
		local lastaimapart
		game:GetService("RunService").RenderStepped:Connect(function()
			espstatustext.Text = "Esp loop :"..tostring(autoesp)
			if aimatpart and lplr.Character and lplr.Character.Head then
				if BetterDeathCount and lastaimapart and lastaimapart == aimatpart then
					local dist = (oldheadpos - aimatpart.CFrame.p).magnitude
					if dist > 40 then
						aimatpart = nil
					end
				end
				lastaimapart = aimatpart
				oldheadpos = lastaimapart.CFrame.p
				do 
					if aimatpart.Parent == plrs.LocalPlayer.Character then
						aimatpart = nil
					end
					aimat(aimatpart)
					pcall(function()
						if Aim_Assist == true then
							local cf1 = CFrame.new(cam.CFrame.p, aimatpart.CFrame.p) * CFrame.new(0, 0, -4)
							local r1 = Ray.new(cf1.p, cf1.LookVector * 1000)
							local obj, pos = game.Workspace:FindPartOnRayWithIgnoreList(r1,  {lplr.Character.Head})
							local dist = (aimatpart.CFrame.p- pos).magnitude
							if obj then
								--print(obj:GetFullName())
							end
							if not obj or dist > 6 then
								aimatpart = nil
								--print("ooof")
							end
							canaimat = false
							delay(.5, function()
								canaimat = true
							end)
						end
					end)
				end



			end
		end)
		delay(0, function()
			while wait(espupdatetime) do
				if autoesp == true then
					pcall(function()
						f.addesp()
					end)
				end
			end
		end)
		--warn("loaded")
	end)
end)

Fly.Name = "Fly"
Fly.Parent = Menu
Fly.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Fly.BackgroundTransparency = 1.000
Fly.Position = UDim2.new(0.617124379, 0, 0.204819277, 0)
Fly.Size = UDim2.new(0, 200, 0, 50)
Fly.Font = Enum.Font.SourceSans
Fly.Text = "Fly"
Fly.TextColor3 = Color3.fromRGB(0, 0, 0)
Fly.TextScaled = true
Fly.TextSize = 14.000
Fly.TextWrapped = true
Fly.MouseButton1Down:connect(function()
	local plr = game.Players.LocalPlayer
	local mouse = plr:GetMouse()

	localplayer = plr

	if workspace:FindFirstChild("Core") then
		workspace.Core:Destroy()
	end

	local Core = Instance.new("Part")
	Core.Name = "Core"
	Core.Size = Vector3.new(0.05, 0.05, 0.05)

	spawn(function()
		Core.Parent = workspace
		local Weld = Instance.new("Weld", Core)
		Weld.Part0 = Core
		Weld.Part1 = localplayer.Character.LowerTorso
		Weld.C0 = CFrame.new(0, 0, 0)
	end)

	workspace:WaitForChild("Core")

	local torso = workspace.Core
	flying = true
	local speed=10
	local keys={a=false,d=false,w=false,s=false}
	local e1
	local e2
	local function start()
		local pos = Instance.new("BodyPosition",torso)
		local gyro = Instance.new("BodyGyro",torso)
		pos.Name="EPIXPOS"
		pos.maxForce = Vector3.new(math.huge, math.huge, math.huge)
		pos.position = torso.Position
		gyro.maxTorque = Vector3.new(9e9, 9e9, 9e9)
		gyro.cframe = torso.CFrame
		repeat
			wait()
			localplayer.Character.Humanoid.PlatformStand=true
			local new=gyro.cframe - gyro.cframe.p + pos.position
			if not keys.w and not keys.s and not keys.a and not keys.d then
				speed=5
			end
			if keys.w then
				new = new + workspace.CurrentCamera.CoordinateFrame.lookVector * speed
				speed=speed+0
			end
			if keys.s then
				new = new - workspace.CurrentCamera.CoordinateFrame.lookVector * speed
				speed=speed+0
			end
			if keys.d then
				new = new * CFrame.new(speed,0,0)
				speed=speed+0
			end
			if keys.a then
				new = new * CFrame.new(-speed,0,0)
				speed=speed+0
			end
			if speed>10 then
				speed=5
			end
			pos.position=new.p
			if keys.w then
				gyro.cframe = workspace.CurrentCamera.CoordinateFrame*CFrame.Angles(-math.rad(speed*0),0,0)
			elseif keys.s then
				gyro.cframe = workspace.CurrentCamera.CoordinateFrame*CFrame.Angles(math.rad(speed*0),0,0)
			else
				gyro.cframe = workspace.CurrentCamera.CoordinateFrame
			end
		until flying == false
		if gyro then gyro:Destroy() end
		if pos then pos:Destroy() end
		flying=false
		localplayer.Character.Humanoid.PlatformStand=false
		speed=10
	end
	e1=mouse.KeyDown:connect(function(key)
		if not torso or not torso.Parent then flying=false e1:disconnect() e2:disconnect() return end
		if key=="w" then
			keys.w=true
		elseif key=="s" then
			keys.s=true
		elseif key=="a" then
			keys.a=true
		elseif key=="d" then
			keys.d=true
		elseif key=="x" then
			if flying==true then
				flying=false
			else
				flying=true
				start()
			end
		end
	end)
	e2=mouse.KeyUp:connect(function(key)
		if key=="w" then
			keys.w=false
		elseif key=="s" then
			keys.s=false
		elseif key=="a" then
			keys.a=false
		elseif key=="d" then
			keys.d=false
		end
	end)
	start()
end)

Noclip.Name = "Noclip"
Noclip.Parent = Menu
Noclip.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Noclip.BackgroundTransparency = 1.000
Noclip.Position = UDim2.new(0.0694668889, 0, 0.466867447, 0)
Noclip.Size = UDim2.new(0, 200, 0, 50)
Noclip.Font = Enum.Font.SourceSans
Noclip.Text = "Noclip"
Noclip.TextColor3 = Color3.fromRGB(0, 0, 0)
Noclip.TextScaled = true
Noclip.TextSize = 14.000
Noclip.TextWrapped = true
Noclip.MouseButton1Down:connect(function()
	noclip = false
	game:GetService('RunService').Stepped:connect(function()
		if noclip then
			game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
		end
	end)
	plr = game.Players.LocalPlayer
	mouse = plr:GetMouse()
	mouse.KeyDown:connect(function(key)
		if key == "e" then
			noclip = not noclip
			game.Players.LocalPlayer.Character.Humanoid:ChangeState(11)
		end
	end)
	game.StarterGui:SetCore("SendNotification", {
		Title = "Noclip";
		Text = "Loaded.";
		Duration = "10";
	})
	wait(1)
	game.StarterGui:SetCore("SendNotification", {
		Title = "Noclip";
		Text = "Press E To Noclip";
		Duration = "10";
	})
end)

Esp.Name = "Esp"
Esp.Parent = Menu
Esp.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Esp.BackgroundTransparency = 1.000
Esp.Position = UDim2.new(0.617124379, 0, 0.466867447, 0)
Esp.Size = UDim2.new(0, 200, 0, 50)
Esp.Font = Enum.Font.SourceSans
Esp.Text = "Esp"
Esp.TextColor3 = Color3.fromRGB(0, 0, 0)
Esp.TextScaled = true
Esp.TextSize = 14.000
Esp.TextWrapped = true
Esp.MouseButton1Down:connect(function()
	-- Unnamed ESP

	assert(Drawing, 'exploit not supported')

	local UserInputService = game:GetService'UserInputService';
	local HttpService = game:GetService'HttpService';
	local GUIService = game:GetService'GuiService';
	local RunService = game:GetService'RunService';
	local Players = game:GetService'Players';
	local LocalPlayer = Players.LocalPlayer;
	local Camera = workspace.CurrentCamera
	local Mouse = LocalPlayer:GetMouse();
	local Menu = {};
	local MouseHeld = false;
	local LastRefresh = 0;
	local OptionsFile = 'IC3_ESP_SETTINGS.dat';
	local Binding = false;
	local BindedKey = nil;
	local OIndex = 0;
	local LineBox = {};
	local UIButtons = {};
	local Sliders = {};
	local Dragging = false;
	local DraggingUI = false;
	local DragOffset = Vector2.new();
	local DraggingWhat = nil;
	local OldData = {};
	local IgnoreList = {};
	local Red = Color3.new(1, 0, 0);
	local Green = Color3.new(0, 1, 0);
	local MenuLoaded = false;

	shared.MenuDrawingData = shared.MenuDrawingData or { Instances = {} };
	shared.PlayerData = shared.PlayerData or {};
	shared.RSName = shared.RSName or ('UnnamedESP_by_ic3-' .. HttpService:GenerateGUID(false));

	local GetDataName = shared.RSName .. '-GetData';
	local UpdateName = shared.RSName .. '-Update';

	local Debounce = setmetatable({}, {
		__index = function(t, i)
			return rawget(t, i) or false
		end;
	});

	pcall(function() shared.InputBeganCon:disconnect() end);
	pcall(function() shared.InputEndedCon:disconnect() end);

	function GetMouseLocation()
		return UserInputService:GetMouseLocation();
	end

	function MouseHoveringOver(Values)
		local X1, Y1, X2, Y2 = Values[1], Values[2], Values[3], Values[4]
		local MLocation = GetMouseLocation();
		return (MLocation.x >= X1 and MLocation.x <= (X1 + (X2 - X1))) and (MLocation.y >= Y1 and MLocation.y <= (Y1 + (Y2 - Y1)));
	end

	function GetTableData(t) -- basically table.foreach i dont even know why i made this
		if typeof(t) ~= 'table' then return end
		return setmetatable(t, {
			__call = function(t, func)
				if typeof(func) ~= 'function' then return end;
				for i, v in pairs(t) do
					pcall(func, i, v);
				end
			end;
		});
	end
	local function Format(format, ...)
		return string.format(format, ...);
	end
	function CalculateValue(Min, Max, Percent)
		return Min + math.floor(((Max - Min) * Percent) + .5);
	end

	local Options = setmetatable({}, {
		__call = function(t, ...)
			local Arguments = {...};
			local Name = Arguments[1];
			OIndex = OIndex + 1; -- (typeof(Arguments[3]) == 'boolean' and 1 or 0);
			rawset(t, Name, setmetatable({
				Name = Arguments[1];
				Text = Arguments[2];
				Value = Arguments[3];
				DefaultValue = Arguments[3];
				AllArgs = Arguments;
				Index = OIndex;
			}, {
				__call = function(t, v)
					if typeof(t.Value) == 'function' then
						t.Value();
					elseif typeof(t.Value) == 'EnumItem' then
						local BT = Menu:GetInstance(Format('%s_BindText', t.Name));
						Binding = true;
						local Val = 0
						while Binding do
							wait();
							Val = (Val + 1) % 17;
							BT.Text = Val <= 8 and '|' or '';
						end
						t.Value = BindedKey;
						BT.Text = tostring(t.Value):match'%w+%.%w+%.(.+)';
						BT.Position = t.BasePosition + Vector2.new(t.BaseSize.X - BT.TextBounds.X - 20, -10);
					else
						local NewValue = v;
						if NewValue == nil then NewValue = not t.Value; end
						rawset(t, 'Value', NewValue);
						if Arguments[2] ~= nil then
							if typeof(Arguments[3]) == 'number' then
								local AMT = Menu:GetInstance(Format('%s_AmountText', t.Name));
								AMT.Text = tostring(t.Value);
								AMT.Position = t.BasePosition + Vector2.new(t.BaseSize.X - AMT.TextBounds.X - 10, -10);
							else
								local Inner = Menu:GetInstance(Format('%s_InnerCircle', t.Name));
								Inner.Visible = t.Value;
							end
						end
					end
				end;
			}));
		end;
	})

	function Load()
		local _, Result = pcall(readfile, OptionsFile);
		if _ then -- extremely ugly code yea i know but i dont care p.s. i hate pcall
			local _, Table = pcall(HttpService.JSONDecode, HttpService, Result);
			if _ then
				for i, v in pairs(Table) do
					if Options[i] ~= nil and Options[i].Value ~= nil and (typeof(Options[i].Value) == 'boolean' or typeof(Options[i].Value) == 'number') then
						Options[i].Value = v.Value;
						pcall(Options[i], v.Value);
					end
				end
			end
		end
	end

	Options('Enabled', 'ESP Enabled', true);
	Options('ShowTeam', 'Show Team', false);
	Options('ShowName', 'Show Names', true);
	Options('ShowDistance', 'Show Distance', true);
	Options('ShowHealth', 'Show Health', true);
	Options('ShowBoxes', 'Show Boxes', true);
	Options('ShowTracers', 'Show Tracers', true);
	Options('ShowDot', 'Show Head Dot', false);
	Options('VisCheck', 'Visibility Check', false);
	Options('Crosshair', 'Crosshair', false);
	Options('TextOutline', 'Text Outline', true);
	Options('TextSize', 'Text Size', syn and 18 or 14, 10, 24); -- cuz synapse fonts look weird???
	Options('MaxDistance', 'Max Distance', 2500, 100, 5000);
	Options('RefreshRate', 'Refresh Rate (ms)', 5, 1, 200);
	Options('MenuKey', 'Menu Key', Enum.KeyCode.F4, 1);
	Options('ResetSettings', 'Reset Settings', function()
		for i, v in pairs(Options) do
			if Options[i] ~= nil and Options[i].Value ~= nil and Options[i].Text ~= nil and (typeof(Options[i].Value) == 'boolean' or typeof(Options[i].Value) == 'number') then
				Options[i](Options[i].DefaultValue);
			end
		end
	end, 4);
	Options('LoadSettings', 'Load Settings', Load, 3);
	Options('SaveSettings', 'Save Settings', function()
		writefile(OptionsFile, HttpService:JSONEncode(Options));
	end, 2)
	-- Options.SaveSettings.Value();

	Load();

	Options('MenuOpen', nil, true);

	local function Set(t, i, v)
		t[i] = v;
	end
	local function Combine(...)
		local Output = {};
		for i, v in pairs{...} do
			if typeof(v) == 'table' then
				table.foreach(v, function(i, v)
					Output[i] = v;
				end)
			end
		end
		return Output
	end
	function IsStringEmpty(String)
		if type(String) == 'string' then
			return String:match'^%s+$' ~= nil or #String == 0 or String == '' or false;
		end
		return false
	end

	function NewDrawing(InstanceName)
		local Instance = Drawing.new(InstanceName);
		return (function(Properties)
			for i, v in pairs(Properties) do
				pcall(Set, Instance, i, v);
			end
			return Instance;
		end)
	end

	function Menu:AddMenuInstace(Name, Instance)
		if shared.MenuDrawingData.Instances[Name] ~= nil then
			shared.MenuDrawingData.Instances[Name]:Remove();
		end
		shared.MenuDrawingData.Instances[Name] = Instance;
		return Instance;
	end
	function Menu:UpdateMenuInstance(Name)
		local Instance = shared.MenuDrawingData.Instances[Name];
		if Instance ~= nil then
			return (function(Properties)
				for i, v in pairs(Properties) do
					-- print(Format('%s %s -> %s', Name, tostring(i), tostring(v)));
					pcall(Set, Instance, i, v);
				end
				return Instance;
			end)
		end
	end
	function Menu:GetInstance(Name)
		return shared.MenuDrawingData.Instances[Name];
	end

	function LineBox:Create(Properties)
		local Box = { Visible = true }; -- prevent errors not really though dont worry bout the Visible = true thing

		local Properties = Combine({
			Transparency = 1;
			Thickness = 1;
			Visible = true;
		}, Properties);

		Box['TopLeft'] = NewDrawing'Line'(Properties);
		Box['TopRight'] = NewDrawing'Line'(Properties);
		Box['BottomLeft'] = NewDrawing'Line'(Properties);
		Box['BottomRight'] = NewDrawing'Line'(Properties);

		function Box:Update(CF, Size, Color, Properties)
			if not CF or not Size then return end

			local TLPos, Visible1 = Camera:WorldToViewportPoint((CF * CFrame.new( Size.X,  Size.Y, 0)).p);
			local TRPos, Visible2 = Camera:WorldToViewportPoint((CF * CFrame.new(-Size.X,  Size.Y, 0)).p);
			local BLPos, Visible3 = Camera:WorldToViewportPoint((CF * CFrame.new( Size.X, -Size.Y, 0)).p);
			local BRPos, Visible4 = Camera:WorldToViewportPoint((CF * CFrame.new(-Size.X, -Size.Y, 0)).p);
			-- ## BEGIN UGLY CODE
			if Visible1 then
				Box['TopLeft'].Visible = true;
				Box['TopLeft'].Color = Color;
				Box['TopLeft'].From = Vector2.new(TLPos.X, TLPos.Y);
				Box['TopLeft'].To = Vector2.new(TRPos.X, TRPos.Y);
			else
				Box['TopLeft'].Visible = false;
			end
			if Visible2 then
				Box['TopRight'].Visible = true;
				Box['TopRight'].Color = Color;
				Box['TopRight'].From = Vector2.new(TRPos.X, TRPos.Y);
				Box['TopRight'].To = Vector2.new(BRPos.X, BRPos.Y);
			else
				Box['TopRight'].Visible = false;
			end
			if Visible3 then
				Box['BottomLeft'].Visible = true;
				Box['BottomLeft'].Color = Color;
				Box['BottomLeft'].From = Vector2.new(BLPos.X, BLPos.Y);
				Box['BottomLeft'].To = Vector2.new(TLPos.X, TLPos.Y);
			else
				Box['BottomLeft'].Visible = false;
			end
			if Visible4 then
				Box['BottomRight'].Visible = true;
				Box['BottomRight'].Color = Color;
				Box['BottomRight'].From = Vector2.new(BRPos.X, BRPos.Y);
				Box['BottomRight'].To = Vector2.new(BLPos.X, BLPos.Y);
			else
				Box['BottomRight'].Visible = false;
			end
			-- ## END UGLY CODE
			if Properties then
				GetTableData(Properties)(function(i, v)
					pcall(Set, Box['TopLeft'], i, v);
					pcall(Set, Box['TopRight'], i, v);
					pcall(Set, Box['BottomLeft'], i, v);
					pcall(Set, Box['BottomRight'], i, v);
				end)
			end
		end
		function Box:SetVisible(bool)
			pcall(Set, Box['TopLeft'], 'Visible', bool);
			pcall(Set, Box['TopRight'], 'Visible', bool);
			pcall(Set, Box['BottomLeft'], 'Visible', bool);
			pcall(Set, Box['BottomRight'], 'Visible', bool);
		end
		function Box:Remove()
			self:SetVisible(false);
			Box['TopLeft']:Remove();
			Box['TopRight']:Remove();
			Box['BottomLeft']:Remove();
			Box['BottomRight']:Remove();
		end

		return Box;
	end

	function CreateMenu(NewPosition) -- Create Menu
		local function FromHex(HEX)
			HEX = HEX:gsub('#', '');
			return Color3.fromRGB(tonumber('0x' .. HEX:sub(1, 2)), tonumber('0x' .. HEX:sub(3, 4)), tonumber('0x' .. HEX:sub(5, 6)));
		end

		local Colors = {
			Primary = {
				Main = FromHex'424242';
				Light = FromHex'6d6d6d';
				Dark = FromHex'1b1b1b';
			};
			Secondary = {
				Main = FromHex'e0e0e0';
				Light = FromHex'ffffff';
				Dark = FromHex'aeaeae';
			};
		};

		MenuLoaded = false;

		GetTableData(UIButtons)(function(i, v)
			v.Instance.Visible = false;
			v.Instance:Remove();
		end)
		GetTableData(Sliders)(function(i, v)
			v.Instance.Visible = false;
			v.Instance:Remove();
		end)

		UIButtons = {};
		Sliders = {};

		local BaseSize = Vector2.new(300, 580);
		local BasePosition = NewPosition or Vector2.new(Camera.ViewportSize.X / 8 - (BaseSize.X / 2), Camera.ViewportSize.Y / 2 - (BaseSize.Y / 2));

		Menu:AddMenuInstace('CrosshairX', NewDrawing'Line'{
			Visible = false;
			Color = Color3.new(0, 1, 0);
			Transparency = 1;
			Thickness = 1;
		});
		Menu:AddMenuInstace('CrosshairY', NewDrawing'Line'{
			Visible = false;
			Color = Color3.new(0, 1, 0);
			Transparency = 1;
			Thickness = 1;
		});

		delay(.025, function() -- since zindex doesnt exist
			Menu:AddMenuInstace('Main', NewDrawing'Square'{
				Size = BaseSize;
				Position = BasePosition;
				Filled = false;
				Color = Colors.Primary.Main;
				Thickness = 3;
				Visible = true;
			});
		end);
		Menu:AddMenuInstace('TopBar', NewDrawing'Square'{
			Position = BasePosition;
			Size = Vector2.new(BaseSize.X, 25);
			Color = Colors.Primary.Dark;
			Filled = true;
			Visible = true;
		});
		Menu:AddMenuInstace('TopBarTwo', NewDrawing'Square'{
			Position = BasePosition + Vector2.new(0, 25);
			Size = Vector2.new(BaseSize.X, 60);
			Color = Colors.Primary.Main;
			Filled = true;
			Visible = true;
		});
		Menu:AddMenuInstace('TopBarText', NewDrawing'Text'{
			Size = 25;
			Position = shared.MenuDrawingData.Instances.TopBarTwo.Position + Vector2.new(25, 15);
			Text = 'Unnamed ESP';
			Color = Colors.Secondary.Light;
			Visible = true;
		});
		Menu:AddMenuInstace('TopBarTextBR', NewDrawing'Text'{
			Size = 15;
			Position = shared.MenuDrawingData.Instances.TopBarTwo.Position + Vector2.new(BaseSize.X - 65, 40);
			Text = 'by ic3w0lf';
			Color = Colors.Secondary.Dark;
			Visible = true;
		});
		Menu:AddMenuInstace('Filling', NewDrawing'Square'{
			Size = BaseSize - Vector2.new(0, 85);
			Position = BasePosition + Vector2.new(0, 85);
			Filled = true;
			Color = Colors.Secondary.Main;
			Transparency= .5;
			Visible = true;
		});

		local CPos = 0;

		GetTableData(Options)(function(i, v)
			if typeof(v.Value) == 'boolean' and not IsStringEmpty(v.Text) and v.Text ~= nil then
				CPos = CPos + 25;
				local BaseSize = Vector2.new(BaseSize.X, 30);
				local BasePosition = shared.MenuDrawingData.Instances.Filling.Position + Vector2.new(30, v.Index * 25 - 10);
				UIButtons[#UIButtons + 1] = {
					Option = v;
					Instance = Menu:AddMenuInstace(Format('%s_Hitbox', v.Name), NewDrawing'Square'{
						Position = BasePosition - Vector2.new(30, 15);
						Size = BaseSize;
						Visible = false;
					});
				};
				Menu:AddMenuInstace(Format('%s_OuterCircle', v.Name), NewDrawing'Circle'{
					Radius = 10;
					Position = BasePosition;
					Color = Colors.Secondary.Light;
					Filled = true;
					Visible = true;
				});
				Menu:AddMenuInstace(Format('%s_InnerCircle', v.Name), NewDrawing'Circle'{
					Radius = 7;
					Position = BasePosition;
					Color = Colors.Secondary.Dark;
					Filled = true;
					Visible = v.Value;
				});
				Menu:AddMenuInstace(Format('%s_Text', v.Name), NewDrawing'Text'{
					Text = v.Text;
					Size = 20;
					Position = BasePosition + Vector2.new(20, -10);
					Visible = true;
					Color = Colors.Primary.Dark;
				});
			end
		end)
		GetTableData(Options)(function(i, v) -- just to make sure certain things are drawn before or after others, too lazy to actually sort table
			if typeof(v.Value) == 'number' then
				CPos = CPos + 25;

				local BaseSize = Vector2.new(BaseSize.X, 30);
				local BasePosition = shared.MenuDrawingData.Instances.Filling.Position + Vector2.new(0, CPos - 10);

				local Text = Menu:AddMenuInstace(Format('%s_Text', v.Name), NewDrawing'Text'{
					Text = v.Text;
					Size = 20;
					Position = BasePosition + Vector2.new(20, -10);
					Visible = true;
					Color = Colors.Primary.Dark;
				});
				local AMT = Menu:AddMenuInstace(Format('%s_AmountText', v.Name), NewDrawing'Text'{
					Text = tostring(v.Value);
					Size = 20;
					Position = BasePosition;
					Visible = true;
					Color = Colors.Primary.Dark;
				});
				local Line = Menu:AddMenuInstace(Format('%s_SliderLine', v.Name), NewDrawing'Line'{
					Transparency = 1;
					Color = Colors.Primary.Dark;
					Thickness = 3;
					Visible = true;
					From = BasePosition + Vector2.new(20, 20);
					To = BasePosition + Vector2.new(BaseSize.X - 10, 20);
				});
				CPos = CPos + 10;
				local Slider = Menu:AddMenuInstace(Format('%s_Slider', v.Name), NewDrawing'Circle'{
					Visible = true;
					Filled = true;
					Radius = 6;
					Color = Colors.Secondary.Dark;
					Position = BasePosition + Vector2.new(35, 20);
				})

				local CSlider = {Slider = Slider; Line = Line; Min = v.AllArgs[4]; Max = v.AllArgs[5]; Option = v};
				Sliders[#Sliders + 1] = CSlider;

				-- local Percent = (v.Value / CSlider.Max) * 100;
				-- local Size = math.abs(Line.From.X - Line.To.X);
				-- local Value = Size * (Percent / 100); -- this shit's inaccurate but fuck it i'm not even gonna bother fixing it

				Slider.Position = BasePosition + Vector2.new(40, 20);

				v.BaseSize = BaseSize;
				v.BasePosition = BasePosition;
				AMT.Position = BasePosition + Vector2.new(BaseSize.X - AMT.TextBounds.X - 10, -10)
			end
		end)
		GetTableData(Options)(function(i, v) -- just to make sure certain things are drawn before or after others, too lazy to actually sort table
			if typeof(v.Value) == 'EnumItem' then
				CPos = CPos + 30;

				local BaseSize = Vector2.new(BaseSize.X, 30);
				local BasePosition = shared.MenuDrawingData.Instances.Filling.Position + Vector2.new(0, CPos - 10);

				UIButtons[#UIButtons + 1] = {
					Option = v;
					Instance = Menu:AddMenuInstace(Format('%s_Hitbox', v.Name), NewDrawing'Square'{
						Size = Vector2.new(BaseSize.X, 20) - Vector2.new(30, 0);
						Visible = true;
						Transparency= .5;
						Position = BasePosition + Vector2.new(15, -10);
						Color = Colors.Secondary.Light;
						Filled = true;
					});
				};
				local Text = Menu:AddMenuInstace(Format('%s_Text', v.Name), NewDrawing'Text'{
					Text = v.Text;
					Size = 20;
					Position = BasePosition + Vector2.new(20, -10);
					Visible = true;
					Color = Colors.Primary.Dark;
				});
				local BindText = Menu:AddMenuInstace(Format('%s_BindText', v.Name), NewDrawing'Text'{
					Text = tostring(v.Value):match'%w+%.%w+%.(.+)';
					Size = 20;
					Position = BasePosition;
					Visible = true;
					Color = Colors.Primary.Dark;
				});

				Options[i].BaseSize = BaseSize;
				Options[i].BasePosition = BasePosition;
				BindText.Position = BasePosition + Vector2.new(BaseSize.X - BindText.TextBounds.X - 20, -10);
			end
		end)
		GetTableData(Options)(function(i, v) -- just to make sure certain things are drawn before or after others, too lazy to actually sort table
			if typeof(v.Value) == 'function' then
				local BaseSize = Vector2.new(BaseSize.X, 30);
				local BasePosition = shared.MenuDrawingData.Instances.Filling.Position + Vector2.new(0, CPos + (25 * v.AllArgs[4]) - 35);

				UIButtons[#UIButtons + 1] = {
					Option = v;
					Instance = Menu:AddMenuInstace(Format('%s_Hitbox', v.Name), NewDrawing'Square'{
						Size = Vector2.new(BaseSize.X, 20) - Vector2.new(30, 0);
						Visible = true;
						Transparency= .5;
						Position = BasePosition + Vector2.new(15, -10);
						Color = Colors.Secondary.Light;
						Filled = true;
					});
				};
				local Text = Menu:AddMenuInstace(Format('%s_Text', v.Name), NewDrawing'Text'{
					Text = v.Text;
					Size = 20;
					Position = BasePosition + Vector2.new(20, -10);
					Visible = true;
					Color = Colors.Primary.Dark;
				});

				-- BindText.Position = BasePosition + Vector2.new(BaseSize.X - BindText.TextBounds.X - 10, -10);
			end
		end)

		delay(.1, function()
			MenuLoaded = true;
		end);

		-- this has to be at the bottom cuz proto drawing api doesnt have zindex :triumph:
		Menu:AddMenuInstace('Cursor1', NewDrawing'Line'{
			Visible = false;
			Color = Color3.new(1, 0, 0);
			Transparency = 1;
			Thickness = 2;
		});
		Menu:AddMenuInstace('Cursor2', NewDrawing'Line'{
			Visible = false;
			Color = Color3.new(1, 0, 0);
			Transparency = 1;
			Thickness = 2;
		});
		Menu:AddMenuInstace('Cursor3', NewDrawing'Line'{
			Visible = false;
			Color = Color3.new(1, 0, 0);
			Transparency = 1;
			Thickness = 2;
		});
	end

	CreateMenu();

	shared.InputBeganCon = UserInputService.InputBegan:connect(function(input)
		if input.UserInputType.Name == 'MouseButton1' and Options.MenuOpen.Value then
			MouseHeld = true;
			local Bar = Menu:GetInstance'TopBar';
			local Values = {
				Bar.Position.X;
				Bar.Position.Y;
				Bar.Position.X + Bar.Size.X;
				Bar.Position.Y + Bar.Size.Y;
			}
			if MouseHoveringOver(Values) and not syn then -- disable dragging for synapse cuz idk why it breaks
				DraggingUI = false; -- also breaks for other exploits
				DragOffset = Menu:GetInstance'Main'.Position - GetMouseLocation();
			else
				for i, v in pairs(Sliders) do
					local Values = {
						v.Line.From.X - (v.Slider.Radius);
						v.Line.From.Y - (v.Slider.Radius);
						v.Line.To.X + (v.Slider.Radius);
						v.Line.To.Y + (v.Slider.Radius);
					};
					if MouseHoveringOver(Values) then
						DraggingWhat = v;
						Dragging = true;
						break
					end
				end
			end
		end
	end)
	shared.InputEndedCon = UserInputService.InputEnded:connect(function(input)
		if input.UserInputType.Name == 'MouseButton1' and Options.MenuOpen.Value then
			MouseHeld = false;
			for i, v in pairs(UIButtons) do
				local Values = {
					v.Instance.Position.X;
					v.Instance.Position.Y;
					v.Instance.Position.X + v.Instance.Size.X;
					v.Instance.Position.Y + v.Instance.Size.Y;
				};
				if MouseHoveringOver(Values) then
					v.Option();
					break -- prevent clicking 2 options
				end
			end
		elseif input.UserInputType.Name == 'Keyboard' then
			if Binding then
				BindedKey = input.KeyCode;
				Binding = false;
			elseif input.KeyCode == Options.MenuKey.Value or (input.KeyCode == Enum.KeyCode.Home and UserInputService:IsKeyDown(Enum.KeyCode.LeftControl)) then
				Options.MenuOpen();
			end
		end
	end)

	function ToggleMenu()
		if Options.MenuOpen.Value then
			GetTableData(shared.MenuDrawingData.Instances)(function(i, v)
				if OldData[v] then
					pcall(Set, v, 'Visible', true);
				end
			end)
		else
			-- GUIService:SetMenuIsOpen(false);
			GetTableData(shared.MenuDrawingData.Instances)(function(i, v)
				if v.Visible == true then
					OldData[v] = true;
					pcall(Set, v, 'Visible', false);
				end
			end)
		end
	end

	function CheckRay(Player, Distance, Position, Unit)
		local Pass = true;

		if Distance > 999 then return false; end

		local _Ray = Ray.new(Position, Unit * Distance);

		local List = {LocalPlayer.Character, Camera, Mouse.TargetFilter};

		for i,v in pairs(IgnoreList) do table.insert(List, v); end;

		local Hit = workspace:FindPartOnRayWithIgnoreList(_Ray, List);
		if Hit and not Hit:IsDescendantOf(Player.Character) then
			Pass = false;
			if Hit.Transparency >= .3 or not Hit.CanCollide and Hit.ClassName ~= Terrain then -- Detect invisible walls
				IgnoreList[#IgnoreList + 1] = Hit;
			end
		end

		return Pass;
	end

	function CheckPlayer(Player)
		if not Options.Enabled.Value then return false end

		local Pass = true;
		local Distance = 0;

		if Player ~= LocalPlayer and Player.Character then
			if not Options.ShowTeam.Value and Player.TeamColor == LocalPlayer.TeamColor then
				Pass = false;
			end

			local Head = Player.Character:FindFirstChild'Head';

			if Pass and Player.Character and Head then
				Distance = (Camera.CFrame.p - Head.Position).magnitude;
				if Options.VisCheck.Value then
					Pass = CheckRay(Player, Distance, Camera.CFrame.p, (Head.Position - Camera.CFrame.p).unit);
				end
				if Distance > Options.MaxDistance.Value then
					Pass = false;
				end
			end
		else
			Pass = false;
		end

		return Pass, Distance;
	end

	function UpdatePlayerData()
		if (tick() - LastRefresh) > (Options.RefreshRate.Value / 1000) then
			LastRefresh = tick();
			for i, v in pairs(Players:GetPlayers()) do
				local Data = shared.PlayerData[v.Name] or { Instances = {} };

				Data.Instances['Box'] = Data.Instances['Box'] or LineBox:Create{Thickness = 3};
				Data.Instances['Tracer'] = Data.Instances['Tracer'] or NewDrawing'Line'{
					Transparency = 1;
					Thickness = 2;
				}
				Data.Instances['HeadDot'] = Data.Instances['HeadDot'] or NewDrawing'Circle'{
					Filled = true;
					NumSides = 30;
				}
				Data.Instances['NameTag'] = Data.Instances['NameTag'] or NewDrawing'Text'{
					Size = Options.TextSize.Value;
					Center = true;
					Outline = Options.TextOutline.Value;
					Visible = true;
				};
				Data.Instances['DistanceHealthTag'] = Data.Instances['DistanceHealthTag'] or NewDrawing'Text'{
					Size = Options.TextSize.Value - 1;
					Center = true;
					Outline = Options.TextOutline.Value;
					Visible = true;
				};

				local NameTag = Data.Instances['NameTag'];
				local DistanceTag = Data.Instances['DistanceHealthTag'];
				local Tracer = Data.Instances['Tracer'];
				local HeadDot = Data.Instances['HeadDot'];
				local Box = Data.Instances['Box'];

				local Pass, Distance = CheckPlayer(v);

				if Pass and v.Character then
					Data.LastUpdate = tick();
					local Humanoid = v.Character:FindFirstChildOfClass'Humanoid';
					local Head = v.Character:FindFirstChild'Head';
					local HumanoidRootPart = v.Character:FindFirstChild'HumanoidRootPart';
					if v.Character ~= nil and Head then
						local ScreenPosition, Vis = Camera:WorldToViewportPoint(Head.Position);
						if Vis then
							local Color = v.TeamColor == LocalPlayer.TeamColor and Green or Red;

							local ScreenPositionUpper = Camera:WorldToViewportPoint(Head.CFrame * CFrame.new(0, Head.Size.Y, 0).p);
							local Scale = Head.Size.Y / 2;

							if Options.ShowName.Value then
								NameTag.Visible = true;
								NameTag.Text = v.Name;
								NameTag.Size = Options.TextSize.Value;
								NameTag.Outline = Options.TextOutline.Value;
								NameTag.Position = Vector2.new(ScreenPositionUpper.X, ScreenPositionUpper.Y);
								NameTag.Color = Color;
								if Drawing.Fonts then -- CURRENTLY SYNAPSE ONLY :MEGAHOLY:
									NameTag.Font = Drawing.Fonts.UI;
								end
							else
								NameTag.Visible = false;
							end
							if Options.ShowDistance.Value or Options.ShowHealth.Value then
								DistanceTag.Visible = true;
								DistanceTag.Size = Options.TextSize.Value - 1;
								DistanceTag.Outline = Options.TextOutline.Value;
								DistanceTag.Color = Color3.new(1, 1, 1);
								if Drawing.Fonts then -- CURRENTLY SYNAPSE ONLY :MEGAHOLY:
									NameTag.Font = Drawing.Fonts.UI;
								end

								local Str = '';

								if Options.ShowDistance.Value then
									Str = Str .. Format('[%d] ', Distance);
								end
								if Options.ShowHealth.Value and Humanoid then
									Str = Str .. Format('[%d/100]', Humanoid.Health / Humanoid.MaxHealth * 100);
								end

								DistanceTag.Text = Str;
								DistanceTag.Position = Vector2.new(ScreenPositionUpper.X, ScreenPositionUpper.Y) + Vector2.new(0, NameTag.Size);
							else
								DistanceTag.Visible = false;
							end
							if Options.ShowDot.Value then
								local Top = Camera:WorldToViewportPoint((Head.CFrame * CFrame.new(0, Scale, 0)).p);
								local Bottom = Camera:WorldToViewportPoint((Head.CFrame * CFrame.new(0, -Scale, 0)).p);
								local Radius = (Top - Bottom).y;

								HeadDot.Visible = true;
								HeadDot.Color = Color;
								HeadDot.Position = Vector2.new(ScreenPosition.X, ScreenPosition.Y);
								HeadDot.Radius = Radius;
							else
								HeadDot.Visible = false;
							end
							if Options.ShowTracers.Value then
								Tracer.Visible = true;
								Tracer.From = Vector2.new(Camera.ViewportSize.X / 2, Camera.ViewportSize.Y);
								Tracer.To = Vector2.new(ScreenPosition.X, ScreenPosition.Y);
								Tracer.Color = Color;
							else
								Tracer.Visible = false;
							end
							if Options.ShowBoxes.Value and HumanoidRootPart then
								Box:Update(HumanoidRootPart.CFrame, Vector3.new(2, 3, 0) * (Scale * 2), Color);
							else
								Box:SetVisible(false);
							end
						else
							NameTag.Visible = false;
							DistanceTag.Visible = false;
							Tracer.Visible = false;
							HeadDot.Visible = false;

							Box:SetVisible(false);
						end
					end
				else
					NameTag.Visible = false;
					DistanceTag.Visible = false;
					Tracer.Visible = false;
					HeadDot.Visible = false;

					Box:SetVisible(false);
				end

				shared.PlayerData[v.Name] = Data;
			end
		end
	end

	function Update()
		for i, v in pairs(shared.PlayerData) do
			if not Players:FindFirstChild(tostring(i)) then
				GetTableData(v.Instances)(function(i, obj)
					obj.Visible = false;
					obj:Remove();
					v.Instances[i] = nil;
				end)
				shared.PlayerData[i] = nil;
			end
		end

		local CX = Menu:GetInstance'CrosshairX';
		local CY = Menu:GetInstance'CrosshairY';
		if Options.Crosshair.Value then
			CX.Visible = true;
			CY.Visible = true;

			CX.To = Vector2.new((Camera.ViewportSize.X / 2) - 8, (Camera.ViewportSize.Y / 2));
			CX.From = Vector2.new((Camera.ViewportSize.X / 2) + 8, (Camera.ViewportSize.Y / 2));
			CY.To = Vector2.new((Camera.ViewportSize.X / 2), (Camera.ViewportSize.Y / 2) - 8);
			CY.From = Vector2.new((Camera.ViewportSize.X / 2), (Camera.ViewportSize.Y / 2) + 8);
		else
			CX.Visible = false;
			CY.Visible = false;
		end

		if Options.MenuOpen.Value and MenuLoaded then
			local MLocation = GetMouseLocation();
			shared.MenuDrawingData.Instances.Main.Color = Color3.fromHSV(tick() * 24 % 255/255, 1, 1);
			local MainInstance = Menu:GetInstance'Main';
			local Values = {
				MainInstance.Position.X;
				MainInstance.Position.Y;
				MainInstance.Position.X + MainInstance.Size.X;
				MainInstance.Position.Y + MainInstance.Size.Y;
			};
			if MainInstance and MouseHoveringOver(Values) then
				Debounce.CursorVis = true;
				-- GUIService:SetMenuIsOpen(true);
				Menu:UpdateMenuInstance'Cursor1'{
					Visible = true;
					From = Vector2.new(MLocation.x, MLocation.y);
					To = Vector2.new(MLocation.x + 5, MLocation.y + 6);
				}
				Menu:UpdateMenuInstance'Cursor2'{
					Visible = true;
					From = Vector2.new(MLocation.x, MLocation.y);
					To = Vector2.new(MLocation.x, MLocation.y + 8);
				}
				Menu:UpdateMenuInstance'Cursor3'{
					Visible = true;
					From = Vector2.new(MLocation.x, MLocation.y + 6);
					To = Vector2.new(MLocation.x + 5, MLocation.y + 5);
				}
			else
				if Debounce.CursorVis then
					Debounce.CursorVis = false;
					-- GUIService:SetMenuIsOpen(false);
					Menu:UpdateMenuInstance'Cursor1'{Visible = false};
					Menu:UpdateMenuInstance'Cursor2'{Visible = false};
					Menu:UpdateMenuInstance'Cursor3'{Visible = false};
				end
			end
			if MouseHeld then
				if Dragging then
					DraggingWhat.Slider.Position = Vector2.new(math.clamp(MLocation.X, DraggingWhat.Line.From.X, DraggingWhat.Line.To.X), DraggingWhat.Slider.Position.Y);
					local Percent = (DraggingWhat.Slider.Position.X - DraggingWhat.Line.From.X) / ((DraggingWhat.Line.To.X - DraggingWhat.Line.From.X));
					local Value = CalculateValue(DraggingWhat.Min, DraggingWhat.Max, Percent);
					DraggingWhat.Option(Value);
				elseif DraggingUI then
					Debounce.UIDrag = true;
					local Main = Menu:GetInstance'Main';
					local MousePos = GetMouseLocation();
					Main.Position = MousePos + DragOffset;
				end
			else
				Dragging = false;
				if DraggingUI and Debounce.UIDrag then
					Debounce.UIDrag = false;
					DraggingUI = false;
					CreateMenu(Menu:GetInstance'Main'.Position);
				end
			end
			if not Debounce.Menu then
				Debounce.Menu = true;
				ToggleMenu();
			end
		elseif Debounce.Menu and not Options.MenuOpen.Value then
			Debounce.Menu = false;
			ToggleMenu();
		end
	end

	RunService:UnbindFromRenderStep(GetDataName);
	RunService:UnbindFromRenderStep(UpdateName);

	RunService:BindToRenderStep(GetDataName, 1, UpdatePlayerData);
	RunService:BindToRenderStep(UpdateName, 1, Update);
end)

SoftAim.Name = "SoftAim"
SoftAim.Parent = Menu
SoftAim.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
SoftAim.BackgroundTransparency = 1.000
SoftAim.Position = UDim2.new(0.0694668889, 0, 0.69879514, 0)
SoftAim.Size = UDim2.new(0, 200, 0, 50)
SoftAim.Font = Enum.Font.SourceSans
SoftAim.Text = "SoftAim"
SoftAim.TextColor3 = Color3.fromRGB(0, 0, 0)
SoftAim.TextScaled = true
SoftAim.TextSize = 14.000
SoftAim.TextWrapped = true
SoftAim.MouseButton1Down:connect(function()
	getgenv().SelectedPart = "Head"
	getgenv().VisibiltyCheck = false
	getgenv().TargetESP = true
	getgenv().FOV = 250
	getgenv().CircleVisibility = true
	getgenv().Distance = 500
--[[ // CREDITS \\--

    YESOK FOR DEVELOPMENT
https://v3rmillion.net/member.php?action=profile&uid=514695

    JAN FOR ESP
https://v3rmillion.net/member.php?action=profile&uid=557102

    CRISHOUX FOR STRUCID/NERF-FPS FUNCTIONS
https://v3rmillion.net/member.php?action=profile&uid=490270
--]]

	warn("Loading...")

	local Players = game:GetService("Players")
	local UserInput = game:GetService("UserInputService")
	local HTTP = game:GetService("HttpService")
	local RunServ = game:GetService("RunService")
	local CoreGui = game:GetService("CoreGui")

	local PlaceId = game.PlaceId
	local LocalPlayer = Players.LocalPlayer
	local CharacterAdded
	local Camera = workspace.CurrentCamera
	local PlayerGui = LocalPlayer:WaitForChild("PlayerGui")
	PlayerGui:SetTopbarTransparency(1)
	local Mouse = LocalPlayer:GetMouse()
	getgenv().methodsTable = {"Ray", "Raycast", "FindPartOnRay", "FindPartOnRayWithIgnoreList", "FindPartOnRayWithWhitelist"}

	local rigType = string.split(tostring(LocalPlayer.Character:WaitForChild("Humanoid").RigType), ".")[3]
	local selected_teamType = "Regular"
	local selected_rigType

	local rigTypeR6 = {
		["Head"] = true,
		["Torso"] = true,
		["LowerTorso"] = true,
		["Left Arm"] = true,
		["Right Arm"] = true,
		["Left Leg"] = true,
		["Right Leg"] = true
	}

	local rigTypeR15 = {
		["Head"] = true,
		["UpperTorso"] = true,
		["LowerTorso"] = true,
		["LeftUpperArm"] = true,
		["RightUpperArm"] = true,
		["RightLowerArm"] = true,
		["LeftLowerArm"] = true,
		["LeftHand"] = true,
		["RightHand"] = true,
		["LeftUpperLeg"] = true,
		["RightUpperLeg"] = true,
		["LeftLowerLeg"] = true,
		["RightLowerLeg"] = true,
		["LeftFoot"] = true,
		["RightFoot"] = true
	}

	local rigTypeStrucid = {
		["LeftLowerArm"] = true,
		["RightLowerArm"] = true,
		["Head"] = true,
		["LeftUpperLeg"] = true,
		["LeftUpperLeg"] = true,
		["RightLowerLeg"] = true,
		["Neck"] = true,
		["RightFoot"] = true,
		["UpperTorso"] = true,
		["LeftLowerLeg"] = true,
		["LowerTorso"] = true,
		["RightUpperLeg"] = true,
		["LeftUpperArm"] = true,
		["RightUpperArm"] = true
	}

	local rigTypeAceOfSpadez = {
		["Head"] = true,
		["LeftFoot"] = true,
		["LowerLeftArm"] = true,
		["LowerLeftLeg"] = true,
		["LowerRightArm"] = true,
		["LowerRightLeg"] = true,
		["LowerTorso"] = true,
		["RightFoot"] = true,
		["MidTorso"] = true,
		["UpperLeftArm"] = true,
		["UpperLeftLeg"] = true,
		["UpperRightArm"] = true,
		["UpperRightLeg"] = true,
		["UpperTorso"] = true,
		["LeftHandle"] = true,
		["RightHandle"] = true,
		["Shoulders"] = true,
		["Torso"] = true
	}

	local rigTypeStandardIssue = {
		["lowerrightleg"] = true,
		["leftforearm"] = true,
		["lowerleftleg"] = true,
		["waist"] = true,
		["Torso"] = true,
		["rightforearm"] = true,
		["Head"] = true,
	}

	local rigTypeRecoil = {
		["Head"] = true,
		["LeftFoot"] = true,
		["RightFoot"] = true,
		["LeftLowerLeg"] = true,
		["LeftUpperLeg"] = true,
		["RightLowerLeg"] = true,
		["RightUpperLeg"] = true,
		["UpperTorso"] = true,
		["LowerTorso"] = true,
		["LeftUpperArm"] = true,
		["RightUpperArm"] = true,
		["LeftLowerArm"] = true,
		["RightLowerArm"] = true,
		["RightHand"] = true,
		["LeftHand"] = true
	}

	local rigTypePloyguns = {
		["Head"] = true,
		["Right Forearm"] = true,
		["Right Leg"] = true,
		["Right Foreleg"] = true,
		["Left Arm"] = true,
		["Right Hand"] = true,
		["Right Foot"] = true,
		["Right Arm"] = true,
		["Left Hand"] = true,
		["Left Foreleg"] = true,
		["Left Leg"] = true,
		["Hips"] = true,
		["Torso"] = true,
		["Left Foot"] = true,
		["Mid"] = true
	}

	local rigTypeKineticCode = {
		["UpperTorso"] = true,
		["Head"] = true,
		["Hips"] = true,
		["LeftArm"] = true,
		["LeftFoot"] = true,
		["LeftHip"] = true,
		["LeftKnuckles"] = true,
		["LeftLeg"] = true,
		["LeftPalm"] = true,
		["LeftShoulder"] = true,
		["LowerTorso"] = true,
		["Neck"] = true,
		["RightArm"] = true,
		["RightFoot"] = true,
		["RightHip"] = true,
		["RightKnuckles"] = true,
		["RightLeg"] = true,
		["RightPalm"] = true,
		["RightShoulder"] = true
	}

	if PlaceId == 2377868063 then
		selected_rigType = rigTypeStrucid
	elseif PlaceId == 2555870920 then
		selected_rigType = rigTypeAceOfSpadez
	elseif PlaceId == 388599755 then
		selected_rigType = rigTypePloyguns
	elseif PlaceId == 1837257681 then
		selected_rigType = rigTypeStandardIssue
	elseif PlaceId == 4651779470 then
		selected_rigType = rigTypeRecoil
		selected_teamType = "Recoil"
	elseif PlaceId == 4738545896 then
		selected_rigType = rigTypeR15
		selected_teamType = "ShootOut"
	elseif PlaceId == 3210442546 then
		selected_rigType = rigTypeR15
		selected_teamType = "IslandRoyale"
	elseif PlaceId == 401356052 then
		selected_rigType = rigTypeKineticCode
	elseif PlaceId == 983224898 then
		selected_teamType = "WildRevolvers"
		selected_rigType = rigTypeR15
	elseif rigType == "R6" then
		selected_rigType = rigTypeR6
	elseif rigType == "R15" then
		selected_rigType = rigTypeR15
	end

	print("Rig Type: " .. rigType)
	print("Team Type: " .. selected_teamType)

	local function teamType(player)
		if selected_teamType == "Recoil" then
			return player:FindFirstChild("GameStats").Team.Value
		elseif selected_teamType == "ShootOut" then
			if player == LocalPlayer then
				return tostring(BrickColor.new(0.172549, 0.329412, 1))
			else
				for _, Player in next, Players:GetPlayers() do
					if Player.Character then
						if Player.Character:FindFirstChild("Head") then
							if Player.Character == player.Character then
								if Player.Character.Head:FindFirstChild("NameTag") then
									NameTag = Player.Character.Head.NameTag.TextLabel
									if string.find(tostring(BrickColor.new(NameTag.TextColor3)), "red") then
										return tostring(BrickColor.new(NameTag.TextColor3))
									elseif string.find(tostring(BrickColor.new(NameTag.TextStrokeColor3)), "blue") then
										return tostring(BrickColor.new(NameTag.TextStrokeColor3))
									end
								end
							end
						end
					end
				end
			end
		elseif selected_teamType == "IslandRoyale" then
			return player:FindFirstChild("TeamName").Value
		elseif selected_teamType == "WildRevolvers" then
			if player == LocalPlayer then
				return tostring(BrickColor.new(0, 255, 0))
			else
				for _, Player in next, game.Players:GetPlayers() do
					if Player.Character then
						if Player.Character:FindFirstChild("Head") then
							if Player.Character == player.Character then
								return tostring(BrickColor.new(Player.Character.Head.HeadTag.Label.TextColor3))
							end
						end
					end
				end
			end
		else
			if player.Team or player.TeamColor then
				local teamplayer = player.Team or player.TeamColor
				return teamplayer
			end
		end
	end

	local function characterType(player)
		if player.Character or workspace:FindFirstChild(player.Name) then
			local playerCharacter = player.Character or workspace:FindFirstChild(player.Name)
			return playerCharacter
		end
	end

	local function FFA()
		sameTeam = 0
		for _, player in next, Players:GetPlayers() do
			if teamType(player) == teamType(LocalPlayer) then
				sameTeam = sameTeam + 1
			end
		end
		if sameTeam == #Players:GetChildren() then
			return true
		else
			return false
		end
	end

	local function returnVisibility(player)
		if getgenv().VisibiltyCheck then
			if characterType(player) then 
				if player.Character:FindFirstChild(getgenv().SelectedPart) then 
					CastPoint = {LocalPlayer.Character[getgenv().SelectedPart].Position, player.Character[getgenv().SelectedPart].Position}
					IgnoreList = {player.Character, LocalPlayer.Character}
					local castpointparts = workspace.CurrentCamera:GetPartsObscuringTarget(CastPoint, IgnoreList)
					if unpack(castpointparts) then
						return false
					end
				end
			end
		end
		return true
	end

	local function returnRay(args, hit)
		if PlaceId == 2377868063 then
			args[3] = {workspace.IgnoreThese, LocalPlayer.Character, workspace.BuildStuff, workspace.Map}
			return args[3]
		elseif PlaceId == 625364452 then
			return hit, hit.Position, Vector3.new(0, 0, 0), hit.Material
		else
			CCF = Camera.CFrame.p
			args[2] = Ray.new(CCF, (hit.Position + Vector3.new(0,(CCF-hit.Position).Magnitude/getgenv().Distance,0) - CCF).unit * (getgenv().Distance * 10))
			return args[2]
		end
	end

	print("FFA: " .. tostring(FFA()))
	print("Visibility Check: " .. tostring(getgenv().VisibiltyCheck))
	print("Target ESP: " .. tostring(getgenv().VisibiltyCheck))

	local function createBox(player)
		local lines = Instance.new("Frame")
		lines.Name = player.Name
		lines.BackgroundTransparency = 1
		lines.AnchorPoint = Vector2.new(0.5,0.5)

		local outlines = Instance.new("Folder", lines)
		outlines.Name = "outlines"
		local inlines = Instance.new("Folder", lines)
		inlines.Name = "inlines"

		local outline1 = Instance.new("Frame", outlines)
		outline1.Name = "left"
		outline1.BorderSizePixel = 0
		outline1.BackgroundColor3 = Color3.new(0,0,0)
		outline1.Size = UDim2.new(0,-1,1,0)

		local outline2 = Instance.new("Frame", outlines)
		outline2.Name = "right"
		outline2.BorderSizePixel = 0
		outline2.BackgroundColor3 = Color3.new(0,0,0)
		outline2.Position = UDim2.new(1,0,0,0)
		outline2.Size = UDim2.new(0,1,1,0)

		local outline3 = Instance.new("Frame", outlines)
		outline3.Name = "up"
		outline3.BorderSizePixel = 0
		outline3.BackgroundColor3 = Color3.new(0,0,0)
		outline3.Size = UDim2.new(1,0,0,-1)

		local outline4 = Instance.new("Frame", outlines)
		outline4.Name = "down"
		outline4.BorderSizePixel = 0
		outline4.BackgroundColor3 = Color3.new(0,0,0)
		outline4.Position = UDim2.new(0,0,1,0)
		outline4.Size = UDim2.new(1,0,0,1)

		local inline1 = Instance.new("Frame", inlines)
		inline1.Name = "left"
		inline1.BorderSizePixel = 0
		inline1.Size = UDim2.new(0,1,1,0)

		local inline2 = Instance.new("Frame", inlines)
		inline2.Name = "right"
		inline2.BorderSizePixel = 0
		inline2.Position = UDim2.new(1,0,0,0)
		inline2.Size = UDim2.new(0,-1,1,0)

		local inline3 = Instance.new("Frame", inlines)
		inline3.Name = "up"
		inline3.BorderSizePixel = 0
		inline3.Size = UDim2.new(1,0,0,1)

		local inline4 = Instance.new("Frame", inlines)
		inline4.Name = "down"
		inline4.BorderSizePixel = 0
		inline4.Position = UDim2.new(0,0,1,0)
		inline4.Size = UDim2.new(1,0,0,-1)

		local text = Instance.new("TextLabel")
		text.Name = "nametag"
		text.Position =  UDim2.new(0.5,0,0,-9)
		text.Size = UDim2.new(0,100,0,-20)
		text.AnchorPoint = Vector2.new(0.5,0.5)
		text.BackgroundTransparency = 1
		text.TextColor3 = Color3.new(1,1,1)
		text.Font = Enum.Font.Code
		text.TextSize = 16
		text.TextStrokeTransparency = 0

		for _,v in pairs(inlines:GetChildren()) do
			v.BackgroundColor3 = Color3.fromRGB(255, 74, 74)
		end

		return lines
	end

	local function updateEsp(player, folder)
		RunServ:BindToRenderStep("Get_Target_ESP", 1, function()
			local playerCharacter = characterType(player)
			local xMin = Camera.ViewportSize.X
			local yMin = Camera.ViewportSize.Y
			local xMax = 0
			local yMax = 0
			if returnVisibility(player) and teamType(player) ~= teamType(LocalPlayer) or FFA() and returnVisibility(player) then
				if player ~= LocalPlayer and player == getTarget() and playerCharacter and playerCharacter:FindFirstChild("Humanoid") and playerCharacter.Humanoid.Health > 0 then
					local box = folder
					local _, onScreen = Camera:WorldToScreenPoint(playerCharacter[getgenv().SelectedPart].Position)
					if onScreen and box then
						box.Visible = true
						local function getCorners(obj, size)
							local corners = {
								Vector3.new(obj.X+size.X/2, obj.Y+size.Y/2, obj.Z+size.Z/2);
								Vector3.new(obj.X-size.X/2, obj.Y+size.Y/2, obj.Z+size.Z/2);

								Vector3.new(obj.X-size.X/2, obj.Y-size.Y/2, obj.Z-size.Z/2);
								Vector3.new(obj.X+size.X/2, obj.Y-size.Y/2, obj.Z-size.Z/2);

								Vector3.new(obj.X-size.X/2, obj.Y+size.Y/2, obj.Z-size.Z/2);
								Vector3.new(obj.X+size.X/2, obj.Y+size.Y/2, obj.Z-size.Z/2);

								Vector3.new(obj.X-size.X/2, obj.Y-size.Y/2, obj.Z+size.Z/2);
								Vector3.new(obj.X+size.X/2, obj.Y-size.Y/2, obj.Z+size.Z/2);
							}
							return corners
						end
						local cornerCount = 1
						local allCorners = {}
						for _, bodyPart in next, playerCharacter:GetChildren() do
							if selected_rigType[bodyPart.Name] then
								local fetchCorners = getCorners(bodyPart.CFrame, bodyPart.Size)
								for _, corner in next, fetchCorners do
									table.insert(allCorners, cornerCount, corner)
									cornerCount = cornerCount + 1
								end
							end
						end
						for _, corner in next, allCorners do
							local pos = Camera:WorldToScreenPoint(corner)
							if pos.X > xMax then
								xMax = pos.X
							end
							if pos.X < xMin then
								xMin = pos.X
							end
							if pos.Y > yMax then
								yMax = pos.Y
							end
							if pos.Y < yMin then
								yMin = pos.Y
							end
						end
						local xSize = xMax - xMin
						local ySize = yMax - yMin
						box.Position = UDim2.new(0,xMin+(Vector2.new(xMax,0)-Vector2.new(xMin,0)).magnitude/2,0,yMin+(Vector2.new(0,yMax)-Vector2.new(0,yMin)).magnitude/2)
						box.Size = UDim2.new(0,xSize,0,ySize)
					end
				end
			end
		end)
	end

	spawn(function()
		repeat
			for Hue = 0,1,0.003 do
				getgenv().Rainbow = Color3.fromHSV(Hue,1,1)
				wait()
			end
		until false
	end)

	spawn(function()
		local Circle = Drawing.new('Circle')
		Circle.Transparency = 1
		Circle.Thickness = 1.5
		Circle.Visible = true
		Circle.Color = Color3.fromRGB(255,0,0)
		Circle.Filled = false
		Circle.Radius = getgenv().FOV

		local TargetText = Drawing.new("Text")
		getgenv().SelectedTarget = ""
		TargetText.Text = ""
		TargetText.Size = 17
		TargetText.Center = true
		TargetText.Visible = true
		TargetText.Color = Color3.fromRGB(255,0,0)
		TargetText.Font = Drawing.Fonts.Monospace

		local lineX = Drawing.new("Line")
		lineX.Transparency = 1
		lineX.Thickness = 1.5
		lineX.Visible = true
		lineX.Color = Color3.fromRGB(255,0,0)

		local lineY = Drawing.new("Line")
		lineX.Transparency = 1
		lineY.Thickness = 1.5
		lineY.Visible = true
		lineY.Color = Color3.fromRGB(255,0,0)

		RunServ:BindToRenderStep("Get_Fov",1,function()
			local Length = 10
			local Middle = 37
			Circle.Visible = getgenv().CircleVisibility
			TargetText.Visible = getgenv().CircleVisibility
			lineX.Visible = getgenv().CircleVisibility
			lineY.Visible = getgenv().CircleVisibility 
			Circle.Color = getgenv().Rainbow
			lineX.Color = getgenv().Rainbow
			lineY.Color = getgenv().Rainbow
			Circle.Radius = getgenv().FOV
			Circle.Position = Vector2.new(Mouse.X,Mouse.Y+Middle)
			TargetText.Position = Vector2.new(Mouse.X,Mouse.Y+Middle-180)
			lineX.From = Vector2.new((Mouse.X)+Length+1,Mouse.Y-0.5+Middle)
			lineX.To = Vector2.new(Mouse.X-Length,Mouse.Y-0.5+Middle)
			lineY.From = Vector2.new(Mouse.X,Mouse.Y+Length+Middle)
			lineY.To = Vector2.new(Mouse.X,Mouse.Y-Length+Middle)
			TargetText.Text = getgenv().SelectedTarget
		end)
	end)

	function getTarget()
		local closestTarg = math.huge
		local Target = nil

		for _, Player in next, Players:GetPlayers() do
			if Player ~= LocalPlayer and returnVisibility(Player) and teamType(Player) ~= teamType(LocalPlayer) or FFA() and Player ~= LocalPlayer and returnVisibility(Player) then
				local playerCharacter = characterType(Player)
				if playerCharacter then
					local playerHumanoid = playerCharacter:FindFirstChild("Humanoid")
					local playerHumanoidRP = playerCharacter:FindFirstChild(getgenv().SelectedPart)
					if playerHumanoidRP and playerHumanoid then
						local hitVector, onScreen = Camera:WorldToScreenPoint(playerHumanoidRP.Position)
						if onScreen and playerHumanoid.Health > 0 then
							local CCF = Camera.CFrame.p
							if workspace:FindPartOnRayWithIgnoreList(Ray.new(CCF, (playerHumanoidRP.Position-CCF).unit * getgenv().Distance),{Player}) then
								local hitTargMagnitude = (Vector2.new(Mouse.X, Mouse.Y) - Vector2.new(hitVector.X, hitVector.Y)).magnitude
								if hitTargMagnitude < closestTarg and hitTargMagnitude <= getgenv().FOV then
									Target = Player
									closestTarg = hitTargMagnitude
								end
							else
							end
						else
						end
					end
				end
			end
		end
		return Target
	end

	local mt = getrawmetatable(game)
	setreadonly(mt, false)
	local index = mt.__index
	local namecall = mt.__namecall
	local hookfunc

	mt.__namecall = newcclosure(function(...)
		local method = getnamecallmethod()
		local args = {...}
		for _, rayMethod in next, getgenv().methodsTable do
			if tostring(method) == rayMethod and Hit then
				returnRay(args, Hit)
				return namecall(unpack(args))
			end
		end
		return namecall(unpack(args))
	end)

	mt.__index = newcclosure(function(func, idx)
		if func == Mouse and tostring(idx) == "Hit" and Hit then
			return Hit.CFrame
		end
		return index(func, idx)
	end)

	hookfunc = hookfunction(workspace.FindPartOnRayWithIgnoreList, function(...)
		local args = {...}
		if Hit then
			if PlaceId == 625364452 then
				return returnRay(args, Hit)
			else
				returnRay(args, Hit)
			end
		end
		return hookfunc(unpack(args))
	end)

	fovVal = Instance.new("ObjectValue", game)
	fovVal.Changed:Connect(function(player)
		if CoreGui:FindFirstChild("Get_ESP", true) then
			RunServ:UnbindFromRenderStep("Get_Target_ESP")
			CoreGui["Get_ESP"].Folder:ClearAllChildren()
		else
			local ScreenGui = Instance.new("ScreenGui", CoreGui) 
			ScreenGui.Name = "Get_ESP"
			Instance.new("Folder", ScreenGui)
		end
		for _, Player in next, Players:GetPlayers() do
			if Player == player and Player.Character.Humanoid.Health > 0 and getgenv().TargetESP then
				wait()
				espBox = createBox(Player)
				updateEsp(Player, espBox)
				espBox.Parent = CoreGui["Get_ESP"].Folder
			end
		end
	end)

	RunServ:BindToRenderStep("Get_Target",1,function()
		local Target = getTarget()
		if not Target then
			Hit = nil
			getgenv().SelectedTarget = ""
			fovVal.Value = nil
		else
			getgenv().SelectedTarget = Target.Name .. "\n" .. math.floor((LocalPlayer.Character[getgenv().SelectedPart].Position - Target.Character[getgenv().SelectedPart].Position).magnitude) .. " Studs"
			fovVal.Value = Target
		end
		if UserInput:IsMouseButtonPressed(0) then
			if Target then
				Hit = Target.Character[getgenv().SelectedPart]
			end
		else
			Hit = nil
		end
	end)

	warn("Loaded!")
end)

InfJump.Name = "InfJump"
InfJump.Parent = Menu
InfJump.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
InfJump.BackgroundTransparency = 1.000
InfJump.Position = UDim2.new(0.617124379, 0, 0.69879514, 0)
InfJump.Size = UDim2.new(0, 200, 0, 50)
InfJump.Font = Enum.Font.SourceSans
InfJump.Text = "InfJump"
InfJump.TextColor3 = Color3.fromRGB(0, 0, 0)
InfJump.TextScaled = true
InfJump.TextSize = 14.000
InfJump.TextWrapped = true
InfJump.MouseButton1Down:connect(function()
	-- Gui to Lua
	-- Version: 3.2

	-- Instances:

	local ScreenGui = Instance.new("ScreenGui")
	local main = Instance.new("Frame")
	local TextLabel = Instance.new("TextLabel")
	local Frame = Instance.new("Frame")
	local INFJUMP = Instance.new("TextButton")
	local TextLabel_2 = Instance.new("TextLabel")

	--Properties:

	ScreenGui.Parent = game.CoreGui

	main.Name = "main"
	main.Parent = ScreenGui
	main.Active = true
	main.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	main.BorderSizePixel = 0
	main.Position = UDim2.new(0.119258665, 0, 0, 0)
	main.Size = UDim2.new(0, 146, 0, 28)
	main.Active = true
	main.Draggable = false

	TextLabel.Parent = main
	TextLabel.BackgroundColor3 = Color3.fromRGB(38, 38, 38)
	TextLabel.BorderSizePixel = 0
	TextLabel.Size = UDim2.new(0, 146, 0, 28)
	TextLabel.Font = Enum.Font.SciFi
	TextLabel.Text = "Misc"
	TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel.TextSize = 17.000
	TextLabel.TextWrapped = true

	Frame.Parent = main
	Frame.BackgroundColor3 = Color3.fromRGB(86, 86, 86)
	Frame.BorderSizePixel = 0
	Frame.Position = UDim2.new(0, 0, 1, 0)
	Frame.Size = UDim2.new(0, 146, 0, 61)

	INFJUMP.Name = "INFJUMP"
	INFJUMP.Parent = main
	INFJUMP.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
	INFJUMP.BorderSizePixel = 0
	INFJUMP.Position = UDim2.new(0.794520497, 0, 1.6785717, 0)
	INFJUMP.Size = UDim2.new(0, 21, 0, 21)
	INFJUMP.Font = Enum.Font.SourceSans
	INFJUMP.Text = ""
	INFJUMP.TextColor3 = Color3.fromRGB(0, 0, 0)
	INFJUMP.TextSize = 14.000
	INFJUMP.MouseButton1Down:connect(function()
		local Player = game:GetService'Players'.LocalPlayer;
		local UIS = game:GetService'UserInputService';

		_G.JumpHeight = 50;

		function Action(Object, Function) if Object ~= nil then Function(Object); end end

		UIS.InputBegan:connect(function(UserInput)
			if UserInput.UserInputType == Enum.UserInputType.Keyboard and UserInput.KeyCode == Enum.KeyCode.Space then
				Action(Player.Character.Humanoid, function(self)
					if self:GetState() == Enum.HumanoidStateType.Jumping or self:GetState() == Enum.HumanoidStateType.Freefall then
						Action(self.Parent.HumanoidRootPart, function(self)
							self.Velocity = Vector3.new(0, _G.JumpHeight, 0);
						end)
					end
				end)
			end
		end)
	end)

	TextLabel_2.Parent = main
	TextLabel_2.BackgroundColor3 = Color3.fromRGB(38, 38, 38)
	TextLabel_2.BorderSizePixel = 0
	TextLabel_2.Position = UDim2.new(0.0547945201, 0, 1.57142854, 0)
	TextLabel_2.Size = UDim2.new(0, 94, 0, 28)
	TextLabel_2.Font = Enum.Font.SciFi
	TextLabel_2.Text = "Inf jump"
	TextLabel_2.TextColor3 = Color3.fromRGB(255, 255, 255)
	TextLabel_2.TextSize = 17.000
	TextLabel_2.TextWrapped = true

	-- Scripts:

	local function TKDWQ_fake_script() -- INFJUMP.LocalScript 
		local script = Instance.new('LocalScript', INFJUMP)

		function zigzag(X) return math.acos(math.cos(X*math.pi))/math.pi end

		counter = 0

		while wait(0.1)do
			script.Parent.BackgroundColor3 = Color3.fromHSV(zigzag(counter),1,1)

			counter = counter + 0.01
		end
	end
	coroutine.wrap(TKDWQ_fake_script)()
end)

merijncat.Name = "@merijncat"
merijncat.Parent = Menu
merijncat.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
merijncat.BackgroundTransparency = 1.000
merijncat.Position = UDim2.new(0.0242326334, 0, 0.879518092, 0)
merijncat.Size = UDim2.new(0, 184, 0, 31)
merijncat.Font = Enum.Font.SourceSans
merijncat.Text = "Made By @merijncat"
merijncat.TextColor3 = Color3.fromRGB(0, 0, 0)
merijncat.TextSize = 20.000

WelcometoMintyHub.Name = "WelcometoMintyHub"
WelcometoMintyHub.Parent = Menu
WelcometoMintyHub.BackgroundColor3 = Color3.fromRGB(60, 255, 174)
WelcometoMintyHub.Position = UDim2.new(0.0242326334, 0, 0.0210843366, 0)
WelcometoMintyHub.Size = UDim2.new(0, 598, 0, 43)
WelcometoMintyHub.Font = Enum.Font.SourceSans
WelcometoMintyHub.Text = "Welcome To MintyHub"
WelcometoMintyHub.TextColor3 = Color3.fromRGB(6, 225, 236)
WelcometoMintyHub.TextScaled = true
WelcometoMintyHub.TextSize = 14.000
WelcometoMintyHub.TextWrapped = true

UICorner_4.Parent = WelcometoMintyHub

UIGradient_3.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(112, 112, 112)), ColorSequenceKeypoint.new(0.04, Color3.fromRGB(112, 112, 112)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(112, 112, 112))}
UIGradient_3.Parent = WelcometoMintyHub

-- Scripts:

local function YQOSG_fake_script() -- Login.LocalScript 
	local script = Instance.new('LocalScript', Login)

	script.Parent.MouseButton1Click:Connect(function()
		script.Parent.Parent.Visible = false
		script.Parent.Parent.Parent.Menu.Visible = true
	end)
	
	
	
	
	
	
	
	
	
end
coroutine.wrap(YQOSG_fake_script)()
