---
description: 오브젝트 이동 튜토리얼
---

# ObjectMove

```lua
local Object = Script.Parent
Object:AddLocalMove("Move", Vector.new(100,0, 0),5 , false)
Object:PlayTransformTrack("Move", 1, InfinityPlay)
```

