-- Script Aimbot:
loadstring(game:HttpGet("https://raw.githubusercontent.com/Sheeshablee73/Scriptss/main/Gun Grounds FFA.lua"))()
-- Script ESP:
pcall(function() loadstring(game:HttpGet('https://raw.githubusercontent.com/ic3w0lf22/Unnamed-ESP/master/UnnamedESP.lua'))() end)
-- Script Speed & TP
loadstring(game:HttpGet("https://raw.githubusercontent.com/Bac0nHck/Scripts/ade1f8efcb4604be34c29476a5baebae4c0ee9d6/ScaryHideSeek"))("t.me/arceusxscripts")
-- Script FreeCam
loadstring(game:HttpGet("https://raw.githubusercontent.com/Fin12n/Script/refs/heads/main/FreeCam.lua"))()
-- Script Infinity jump
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
