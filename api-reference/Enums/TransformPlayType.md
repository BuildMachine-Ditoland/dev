
변환 컨트롤러 실행방식을 결정하는 타입이에요. 
<br>
## **Enums**

 **이름** | **설명** |
 --- | --- |
**Repeat** |변환 컨트롤러를 반복해서 실행하는 타입이에요. |
**Tween** |변환 컨트롤러를 왕복해서 실행하는 타입이에요. |

샘플 

```lua
local cube = Workspace.Cube
local moveSpeed = 2
cube:AddLocalRot("Rot", Vector.new(0, 0, 360), moveSpeed) --회전 트랙을 등록해요.
cube:AddLocalRot("Rot", Vector.new(0, 360, 0), moveSpeed) --회전 트랙은 여러개도 등록할 수 있어요.
cube:PlayTransformTrack("Rot", Enum.TransformPlayType.Repeat, InfinityPlay) --이름에 해당하는 트랙을 재생해요.
```
