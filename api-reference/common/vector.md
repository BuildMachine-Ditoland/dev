# Vector

### **Function**

| **void Normalize\(\)** |
| :--- |
| **단위를 1로 정규화 시킨다.** |

### \*\*\*\*

### **Property**

**“X”, &RDataVector::X,**

**“Y”, &RDataVector::Y,**

**“Z”, &RDataVector::Z**

\*\*\*\*

### **Sample**

```lua
local Object = Script.Parent
Object:AddLocalMove("Move", Vector.new(X,Y, Z),5 , false)
Object:PlayTransformTrack("Move", 1, InfinityPlay) 
```

  




