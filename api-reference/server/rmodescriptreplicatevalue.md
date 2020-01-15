# RModeScriptReplicateValue

## **RModeScriptReplicateValue**

**유저가 Lua에서 서버, 클라이언트가 동기화 기능이 있는 값을 추가, 변경 할 수 있는 객체**

## \*\*\*\*

## **Function**

| **void AddReplicateValue\(string ValueName, DataType Data, ReplicateType Type, float Time, bool bSaveToStorage\)** |
| :--- |
| **해당 객체에 동기화 기능이 있는 값을 추가** |

| **void AddSaveValue\(string ValueName, DataType Data\)** |
| :--- |
| **해당 객체에 저장소에 저장가능한 값을 추가** |

## \*\*\*\*

## **Sample**

```lua
function SpawnCharacter( Character )

    Character:AddReplicateValue("HP", 500, Enum.ReplicateType.Changed) 
    Character:AddReplicateValue("MoveSpeed", 500, Enum.ReplicateType.Changed)
    Character:PlayFXAllUser("Resurrection",RESURRECTION)

end


local function EnterPlayer(Player)

    if Player == nil then 
        return 
    end 

    Player:AddSaveValue("TestSaveValue", 100)
    Player.TestSaveValue = 99

end
```

