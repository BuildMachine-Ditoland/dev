
유저가 작성한 Lua 함수를 연결, 특정 상황에 연결된 함수를 호출해 주는 객체에요. 
<br>
## **함수**

<br>
| **bool Connect(LuaScriptFunction Function)** |
| :--- |

작성한 Lua 함수에 해당 이벤트를 연결해주는 역할이에요. (연결 함수) 

샘플 

```lua
local function EnterPlayer(player) --OnEnterPlayer로 연결된 함수는 player 인자가 고정적으로 들어가요.
	print("Enter " .. player:GetName()) 
end
Game.OnEnterPlayer:Connect(EnterPlayer) --Game에 플레이어가 게임에 입장하면 호출되는 함수를 연결해요.
```
