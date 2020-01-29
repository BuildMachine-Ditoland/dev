# RModeEventFunction

## **RModeEventFunction**

**유저가 작성한 Lua 함수를 연결, 특정 상황에 연결된 함수를 호출해 주는 객체**

 

## **Functions**

| **bool Connect\( function\_name \)** |
| :--- |
| **작성한 Lua 함수를 해당 이벤트에 연결하는 함수** |

## **Sample**

```lua
local function EnterPlayer (Player)
    Logger:Log(“Hello”)
end

Game.OnEnterPlayer:Connect(EnterPlayer)
```

