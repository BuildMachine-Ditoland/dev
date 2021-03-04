
유저가 작성한 Lua 함수를 연결, 특정 상황에 연결된 함수를 호출해 주는 객체에요. 
## **함수**

| **bool Connect(LuaScriptFunction Function)** |
| :--- |

작성한 Lua 함수에 해당 이벤트를 연결해주는 역할이에요. (연결 함수) 

샘플 

```lua
local function EnterPlayer (Player)
	print(“Hello”)
end

-- Game.OnEnterPlayer가 Connect를 통해 EnterPlayer함수에 연결됨
Game.OnEnterPlayer:Connect(EnterPlayer)	 
```
