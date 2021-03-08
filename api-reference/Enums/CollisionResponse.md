오브젝트의 충돌 처리 타입이에요. 
## **Enums**

 **이름** | **설명** |
 --- | --- |
**Ignore** |오브젝트가 충돌하지 않고 통과되며, 이벤트가 발생하지 않게 해요. |
**Overlap** |오브젝트가 충돌하지 않고, 겹쳐지며 이벤트가 발생해요. (겹쳐짐 시작, 겹쳐지고 있음, 겹쳐짐 종료) |
**Block** |오브젝트가 충돌하고, 충돌할 때 이벤트가 발생해요. |
샘플 

```lua
Workspace.Cube1:SetCharacterCollisionResponse(Enum.CollisionResponse.Block) --오브젝트가 캐릭터와 충돌했을때 통과되지 않고 연결된 이벤트가 발생되게 설정해요.
Workspace.Cube2:SetCharacterCollisionResponse(Enum.CollisionResponse.Overlap) --오브젝트가 캐릭터와 충돌했을때 통과되고 연결된 이벤트되게 설정해요..
Workspace.Cube3:SetCharacterCollisionResponse(Enum.CollisionResponse.Ignore) --오브젝트가 캐릭터와 충돌했을때 통과되고 연결된 이벤트가 발생되지 않게 설정해요.
```
