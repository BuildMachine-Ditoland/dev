# RObjectScript

## **RObjectScript**

**월드에 생성되는 R오브젝트에 제공되는 객체**

## **Property**

| **[var OnCreateEvent](../../api-reference/function/test.md)** |
| :--- |
|**생성 시 호출되는 이벤트 객체**|

### **var OnUpdateEvent**
**생성 후 매 프레임에 호출되는 이벤트 객체**

### **var OnDestoryEvent** 
**없어 질 때 호출되는 이벤트 객체**

### **var OnCollisionEvent**
 **물체가 부딪 힐 때 호출되는 이벤트 객체** 

### **var OnBeginOverlapEvent** 
**겹처지기 시작 될 때 호출되는 이벤트 객체** 

### **var OnEndOverlapEvent** 
**겹처짐이 끝 날 때 호출되는 이벤트 객체** 
 
### **var OnOverlapUpdateEvent** 
**겹처져 있는 동안 매 프레임 호출되는 이벤트 객체** 

### **var OnChildCreateEvent**  
 **자식 생성 시 호출되는 이벤트 객체** 

### **var OnChildDestoryEvent**  
**자식 없어 질 때 호출되는 이벤트 객체** 

### **var OnChildCollisionEvent**
 **자식에 물체가 부딪 힐 때 호출되는 이벤트 객체** 

### **var OnChildBeginOverlapEvent** 
**자식에 겹처지기 시작 될 때 호출되는 이벤트 객체** 

### **var OnChildEndOverlapEvent** 
 **자식에 겹처짐이 끝 날 때 호출되는 이벤트 객체** 

 

## **Sample**

```lua
local Object = Script.Parent

function FunctionName(Character) 

    Logger:Log(“Hello”)

end

Object.OnBeginOverlapEvent:Connect(FunctionName)
```

## **Functions**

### RModeObject GetChild\(string childName\)**  
**자식 오브젝트 얻기** 

###  **RModeObject GetParent\(string childName\)** 
 **부모 오브젝트 얻기** 

###  **void AddLocalMove\(string TrackName, FVector Pos, float Time, bool CheckCollision\)** |
 **오브젝트를 로컬 축 이동 변화를 추가한다.** 

### **void AddLocalRot\(string TrackName, FVector Rot, float Time\)**  
**오브젝트를 로컬 축 회전 변화를 추가한다**

###  **void AddScale\(string TrackName, FVector Scale, float Time\)** 
 **오브젝트를 로컬 축 스케일 변화를 추가한다** 

###  **void AddLocalMove\(string TrackName, FVector Pos, float Time, bool CheckCollision\)** 
 **오브젝트를 월드 축 이동 변화를 추가한다.** 

### **void AddLocalRot\(string TrackName, FVector Rot, float Time\)** 
**오브젝트를 월드 축 회전 변화를 추가한다** 

### **void AddEmpty\(string TrackName, float Time\)** 
 **오브젝트를 변환에 대기를 추가한다** 

### **void PlayTransformTrack\(string TrackName, ERObjectTransformPlayType Type, int PlayCount\)** |
**설정된 변환 컨트롤러 실행** 

### **void StopTransformTrack\(string TrackName\)** 
**설정된 변환 컨트롤러 실행** 

### **void PauseTransformTrack\(string TrackName\)** 
 **변환 컨트롤러 일시 정지** 

### **void ResumeTransformTrack\(string TrackName\)** 
 **변환 컨트롤러 다시 플레이** 

###  **bool IsPlayingTransformTrack\(string TrackName\)** 
 **해당 TransformTrack이 플레이 중인지 확인** 

###  **void ResetTransformTrack\(string TrackName\)**  
**해당 TransformTrack 리셋\(적용되기 전의 Transform 으로 설정\)**  

###  **void ResetTransform\(\)** 
**TransformTrack 이 적용되기 전의 최초 Transform으로 설정**  

### **Vector GetLocation\(\)** 
 **현재 위치 얻기** 

## **Sample**

```lua
local Object = Script.Parent

Object:AddLocalRot("Rot", Vector.new(0, 0, 360), 8)  

Object:PlayTransformTrack("Rot", 0, InfinityPlay)
```

