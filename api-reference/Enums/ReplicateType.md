
객체에 추가된 값의 서버, 클라이언트 간 동기화 타입이에요. 
## **Enums**

 **이름** | **설명** |
 --- | --- |
**None** |동기화 방식이 없어요. |
**Changed** |값이 변경될 때마다 동기화해요. |
**ChangedTime** |값이 변경되고 나서 일정 시간마다 동기화해요. |

샘플 

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("GameID", 1, Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.GameID .. " in Server")

wait(0.5)
Game.GameID = 2

wait(0.5)
print(Game.GameID .. " in Server")

--클라 스크립트에서-------------
print(Game.GameID .. " in Client") --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.

wait(0.5)
wait(0.5)
print(Game.GameID .. " in Client") --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
