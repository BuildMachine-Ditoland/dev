# **RModeScriptValue**

| **특정한 변수가 변경되었을 때 실행되는 함수를 연결하는 객체** |
| :--- |
## **함수**

| **void ConnectChangeEventFunction(string ValueName, FunctionName)** |
| :--- |
| **ValueName의 변수가 변경될 때 FunctionName의 함수가 실행된다.** |

## **샘플**

```lua
local function EnterPlayer (Player)
	Logger:Log(“Hello”)
end

-- Game.OnEnterPlayer가 RModeEventFunction을 리턴
Game.OnEnterPlayer:Connect(EnterPlayer)	 
```
