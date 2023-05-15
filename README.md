# MAGIC-SMP
local brick = Instance.new("Part")
brick.BrickColor = BrickColor.new("Bright blue")
brick.Size = Vector3.new(10, 5, 10)
brick.Position = Vector3.new(0, 5, 0)
brick.Parent = workspace

-- Function to change the color of the brick
local function ChangeColor()
    brick.BrickColor = BrickColor.new("Bright red")
end

-- Event handler for when a player touches the brick
local function OnTouch(otherPart)
    local player = game.Players:GetPlayerFromCharacter(otherPart.Parent)
    if player then
        ChangeColor()
    end
end
-- Level 2 Transition Script

-- Variables
local level2Trigger = workspace.Level2Trigger -- Assume you have a part named "Level2Trigger" in your game

-- Function to transition to level 2
local function TransitionToLevel2()
    -- Code to unload level 1 objects or reset level 1
    -- Insert code here to remove or reset level 1 objects
    
    -- Code to load level 2 objects
    -- Insert code here to create or load level 2 objects
    
    print("Transitioning to Level 2...")
end

-- Function to check for level 2 trigger
local function CheckLevel2Trigger(otherPart)
    local player = game.Players:GetPlayerFromCharacter(otherPart.Parent)
    if player and otherPart == level2Trigger then
        TransitionToLevel2()
    end
end

-- Connect the level 2 trigger event
level2Trigger.Touched:Connect(CheckLevel2Trigger)

-- Level 3 Transition Script

-- Variables
local level3Trigger = workspace.Level3Trigger -- Assume you have a part named "Level3Trigger" in your game

-- Function to transition to level 3
local function TransitionToLevel3()
    -- Code to unload level 2 objects or reset level 2
    -- Insert code here to remove or reset level 2 objects
    
    -- Code to load level 3 objects
    -- Insert code here to create or load level 3 objects
    
    print("Transitioning to Level 3...")
end

-- Function to check for level 3 trigger
local function CheckLevel3Trigger(otherPart)
    local player = game.Players:GetPlayerFromCharacter(otherPart.Parent)
    if player and otherPart == level3Trigger then
        TransitionToLevel3()
    end
end

-- Connect the level 3 trigger event
level3Trigger.Touched:Connect(CheckLevel3Trigger)

-- Level 4 Script

-- Variables
local level4Start = workspace.Level4Start -- Assume you have a part named "Level4Start" in your game
local level4Goal = workspace.Level4Goal -- Assume you have a part named "Level4Goal" in your game

-- Function to transition to level 4
local function TransitionToLevel4()
    -- Code to unload level 3 objects or reset level 3
    -- Insert code here to remove or reset level 3 objects
    
    -- Code to load level 4 objects
    -- Insert code here to create or load level 4 objects
    
    print("Transitioning to Level 4...")
end

-- Function to check for level 4 start
local function CheckLevel4Start(otherPart)
    local player = game.Players:GetPlayerFromCharacter(otherPart.Parent)
    if player and otherPart == level4Start then
        TransitionToLevel4()
    end
end

-- Connect the level 4 start event
level4Start.Touched:Connect(CheckLevel4Start)

-- Function to check for level 4 goal
local function CheckLevel4Goal(otherPart)
    local player = game.Players:GetPlayerFromCharacter(otherPart.Parent)
    if player and otherPart == level4Goal then
        -- Code to complete level 4 or trigger victory
        -- Insert code here to handle level completion or victory
        print("Level 4 completed!")
    end
end

-- Connect the level 4 goal event
level4Goal.Touched:Connect(CheckLevel4Goal)
