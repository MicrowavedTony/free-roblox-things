local Players = game:GetService("Players")

local Prefix = '/'

local Whitelisted = {
	['Dope_RBX'] = 'Whitelisted'; --to add more, just make more
}


local function CheckForTarget(Target)
	if not Target then
		warn('Target is not valid')
		return false
	else
		print('Target is valid')
		return true
	end
end

Players.PlayerAdded:Connect(function(Player)
	if Whitelisted[Player.Name] then
		Player.Chatted:Connect(function(Msg)
			if Msg:sub(1,10) == Prefix..'headless ' or Msg:sub(1,10) == Prefix..'Headless ' then
				local Target = Players:FindFirstChild(Msg:sub(11))
				local Valid = CheckForTarget(Target)

				if Valid then
					Target.Character.Head.Transparency = 1
					Target.Character.Head.face.Transparency = 1
				end
			end
		end)
	end
end)
