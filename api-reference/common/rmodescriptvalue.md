# RModeScriptValue

## **RModeScriptValue**

**유저가 Lua에서 값을, 추가 변경 할 수 있는 객체**

\*\*\*\*

## **Functions**

| **void ConnectChangeEventFunction\(string valuename, function\_name\)** |
| :--- |
| **추가된 값이 변경될 때 호출되는 이벤트를 반환한다.** |

\*\*\*\*

## **Sample**

```lua
local function FunctionName(Character, Value)

    Logger:Log(“Hello”)
    -- value = HP value

end


local function SpawnCharacter(Character)

   Character:ConnectChangeEventFunction("HP", FunctionName)

end

Game.OnSpawnCharacter:Connect(SpawnCharacter)
```

