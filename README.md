-- # Fe-spam-Block-Fencing
-- Fixed by me


local args = {
    [1] = "FE spam block loaded made by =  lz",
    [2] = "All"
}

game:GetService("ReplicatedStorage"):WaitForChild("DefaultChatSystemChatEvents"):WaitForChild("SayMessageRequest"):FireServer(unpack(args))



local library = loadstring(game:HttpGet("https://github.com/GoHamza/AppleLibrary/blob/main/main.lua?raw=true"))()


local window = library:init("FencingHub", true, Enum.KeyCode.Insert, true)

window:Divider("FE spam block (Fixed)")

local sectionA = window:Section("Spam Block")

sectionA:Divider("Fe spam block")

sectionA:Button("Magica", function()
   --

local Workspace = game:GetService('Workspace')
local Players = game:GetService('Players')
local Player = Players.LocalPlayer
local Character = Player.Character
local SprayPaint = Workspace:FindFirstChild('Handle')
    
    for i,v in pairs(Workspace:GetChildren()) do
        if v.Name == 'Handle' and v:FindFirstChild('Script') and v:FindFirstChild('TouchInterest') and v:FindFirstChild('Mesh') then
            SprayPaint = v
        end
    end
    
    if SprayPaint then
        local LoopBroken = false
        
        for i,v in pairs(Character:GetChildren()) do
            if v.Name == 'Spray' then
                v.Parent = Character
                v.Parent = Workspace
            end
        end
        
        for i,v in pairs(Player.Backpack:GetChildren()) do
            if v.Name == 'Spray' then
                v.Parent = Character
                v.Parent = Workspace
            end
        end
        
        Player.CharacterRemoving:Connect(function()
            LoopBroken = true
        end)
        
        Character.ChildAdded:Connect(function(Obj)
            if Obj.Name == 'Spray' and LoopBroken == false then
                task.wait()
                pcall(function() Obj.Handle.Mesh:Destroy() end)
                Obj.Parent = Workspace
            end
        end)
        
        Player.Backpack.ChildAdded:Connect(function(Obj)
            if Obj.Name == 'Spray' and LoopBroken == false then
                task.wait()
                Obj.Parent = Character
                pcall(function() Obj.Handle.Mesh:Destroy() end)
                Obj.Parent = Workspace
            end
        end)
        
        
        while true do
            pcall(function()
                firetouchinterest(SprayPaint, Character.HumanoidRootPart, 0) -- touch
                firetouchinterest(SprayPaint, Character.HumanoidRootPart, 1) -- untouch
            end)
            task.wait()
        end
    end


end)

sectionA:Select()

-- Objects

local Idk = Instance.new("ScreenGui")
local ImageLabel = Instance.new("ImageLabel")
local Nigger = Instance.new("Frame")
local Idk_2 = Instance.new("TextLabel")

-- Properties

Idk.Name = "Idk"
Idk.Parent = game.CoreGui
Idk.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

ImageLabel.Parent = Idk
ImageLabel.BackgroundColor3 = Color3.new(1, 1, 1)
ImageLabel.Position = UDim2.new(0.0158730168, 0, 0.783132553, 0)
ImageLabel.Size = UDim2.new(0, 67, 0, 61)
ImageLabel.Image = "http://www.roblox.com/asset/?id=6403436054"

Nigger.Name = "Nigger"
Nigger.Parent = ImageLabel
Nigger.BackgroundColor3 = Color3.new(1, 1, 1)
Nigger.Position = UDim2.new(1.19402981, 0, 0.0819672123, 0)
Nigger.Size = UDim2.new(0, 158, 0, 50)

Idk_2.Name = "Idk"
Idk_2.Parent = Nigger
Idk_2.BackgroundColor3 = Color3.new(1, 1, 1)
Idk_2.BackgroundTransparency = 1
Idk_2.Position = UDim2.new(0.408440173, 0, 0.359999985, 0)
Idk_2.Size = UDim2.new(0, 25, 0, 15)
Idk_2.Font = Enum.Font.Unknown
Idk_2.Text = "RickRoll Scripts Community"
Idk_2.TextColor3 = Color3.new(0, 0, 0)
Idk_2.TextSize = 8

