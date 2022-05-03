_G.activated = true 

local esp_settings = {
	
	textsize = 8,
	colour = 255,255,255
}

local function findFolder()
	for i, v in pairs(game:GetService("Workspace"):GetChildren()) do
		if v:IsA("Folder") and tonumber(v.Name) then 
		    print(v.Name)
			return v 
		end
	end 
end





local billboard = Instance.new("BillboardGui")
local esp = Instance.new("TextLabel", billboard)

billboard.Name = "HeyThere"
billboard.ResetOnSpawn = false 
billboard.AlwaysOnTop = true 
billboard.LightInfluence = 0
billboard.Size = UDim2.new(1.75, 0, 1.75, 0);

esp.BackgroundColor3 = Color3.fromRGB(255, 255, 255);
esp.Text = ""
esp.Size = UDim2.new(0.0001, 0.00001, 0.0001, 0.00001);
esp.BorderSizePixel = 4;
esp.BorderColor3 = Color3.new(esp_settings.colour)
esp.BorderSizePixel = 0
esp.Font = "GothamSemibold"
esp.TextSize = esp_settings.textsize
esp.TextColor3 = Color3.fromRGB(esp_settings.colour) 



spawn(function()
	while _G.activated do 
		local folder = findFolder()
		
		for i, v in pairs(folder:GetChildren()) do 
			if v.Name == "Chest" and not v:FindFirstChild("HeyThere") then 
	
				esp.Text = "Chest"
				billboard:Clone().Parent = v
				
				
			end
			
		end
		
		wait(1)
	end
end)
