```cs
local sex = loadstring(game:HttpGet("https://raw.githubusercontent.com/TsouHub/Garry-UI/refs/heads/main/source"))()

local Window = sex:Create('BEDOL HUB','BLADE BALL','TESTER')
local ExampleTab = Window:CreateTab('Example','earth')

ExampleTab:CreateButton("Button",function()
	print('press button')
end)

ExampleTab:CreateLabel("Label")

ExampleTab:CreateToggle("Toggle",false,function(val)
	print('toggle',val)
end)

ExampleTab:CreateKeybind("Keybind",Enum.KeyCode.E,function(val)
	print('keybind',val)
end)

ExampleTab:CreateSlider("Slider",1,100,10,function(val)
	print('slider',val)
end)

Window:CreateButton('earth',false,function(val)
	print('set time')
	if val then
		Window:Notify('Time Change','Night',1.5)
		game:GetService('TweenService'):Create(game:GetService('Lighting'),TweenInfo.new(0.5),{ClockTime = 0}):Play()
	else
		Window:Notify('Time Change','Day',1.5)
		game:GetService('TweenService'):Create(game:GetService('Lighting'),TweenInfo.new(0.5),{ClockTime = 14}):Play()
	end
end)

Window:CreateButton('ads',false,function(val)
	print('fov change')
	if val then
		Window:Notify('FOV Change','120',1)
		game:GetService('TweenService'):Create(workspace.CurrentCamera,TweenInfo.new(0.5),{FieldOfView = 120}):Play()
	else
		Window:Notify('FOV Change','70',1)
		game:GetService('TweenService'):Create(workspace.CurrentCamera,TweenInfo.new(0.5),{FieldOfView = 70}):Play()
	end
end)

```
