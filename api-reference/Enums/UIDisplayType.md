
SurfaceUI 의 DisplayType <br>
<br>
## **Enums**

 **이름** | **설명** |
 --- | --- |
| **Screen** |
| --- |
| **Billboard** |
| --- |

샘플 <br>

```lua
local PlayerNameUI = HUD.PlayerNameUI
PlayerNameUI:SetVisible(false)

local function spawn(character)
   local ui = character:AddPlayerHUD("SomeText", PlayerNameUI, Enum.UIDisplayType.Screen) --캐릭터에 HUD를 추가하고 이름으로 등록해요.
   ui:SetVisible(true)
end
Game.OnSpawnCharacter:Connect(spawn)
```
