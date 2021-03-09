
스폰 포인트가 작동하는 방식을 결정하는 타입이에요. 
<br>
## **Enums**

 **이름** | **설명** |
 --- | --- |
**Point** |지정된 Point 위치에 스폰시켜요. |
**Area** |지정된 범위에 스폰시켜요. |

샘플 

```lua
local spawner = Game:AddSpawnPointAtGroup("SpawnGroup", Workspace.SpawnPoint) --스폰 그룹에서 사용할 스폰포인트를 등록해요.
local spawnRadius = 50 --캐릭터 스폰 반경을 설정해요.
spawner:SetSpawnType(Enum.PointSpawnType.Area, spawnRadius) --팀의 스폰타입을 설정해요.
```
