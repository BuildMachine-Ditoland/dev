
물리 적용방식을 결정하는 타입이에요. 
## **Enums**

 **이름** | **설명** |
 --- | --- |
**Off** |물리를 사용하지 않는 타입이에요. |
**On_NonSync** |클라이언트에서만 물리 사용이 가능한 타입이에요. |
**On_Sync** |서버와 클라이언트 모두 사용이 가능한 타입이에요. |

샘플 

```lua
local cube = Workspace.Cube
cube:SetSimulatePhysics(Enum.SimulatePhysicsType.On_Sync) --오브젝트의 물리를 설정해요.
```
