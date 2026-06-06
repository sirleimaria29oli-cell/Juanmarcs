local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local Title = Instance.new("TextLabel")

ScreenGui.Parent = game.Players.LocalPlayer.PlayerGui

Frame.Size = UDim2.new(0, 350, 0, 220)
Frame.Position = UDim2.new(0.5, -175, 0.5, -110)
Frame.Parent = ScreenGui

Title.Size = UDim2.new(1, 0, 0, 40)
Title.Text = "FUTURE CONTROL PANEL"
Title.Parent = Frame

local buttons = {
	"Radar",
	"Inventory",
	"Scanner",
	"Drone Control"
}

for i, name in ipairs(buttons) do
	local btn = Instance.new("TextButton")
	btn.Size = UDim2.new(0.8, 0, 0, 35)
	btn.Position = UDim2.new(0.1, 0, 0, 50 + (i - 1) * 40)
	btn.Text = name
	btn.Parent = Frame
end
