
캐릭터 본 타입이에요. 
<br>
## **Enums**

 **이름** | **설명** |
 --- | --- |
**Head** |머리 |
**Body** |몸통 |
**Chest** |가슴 |
**Pelvis** |골반 |
**RHand** |오른손 |
**LHand** |왼손 |
**RFoot** |오른발 |
**LFoot** |왼발 |
**Root** |바닥 |

샘플 

```lua
local character = LocalPlayer:GetRemotePlayer():GetCharacter()
character:CreateFX(Workspace.Effect, Enum.Bone.Body) --캐릭터의 특정 부위에 이펙트를 생성해요.
```
