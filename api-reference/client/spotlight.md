# SpotLight

클라이언트에서 사용되는 스포트라이트 개체에요.   


### **함수**

| **SetEnable\(bool bEnable\)** |
| :--- |


설정된 스포트 라이트의 작동 여부를 설정해요. \(작동 여부\)   
   


| **SetColor\(Color ChangedColor\)** |
| :--- |


스포트 라이트의 컬러를 변경할 수 있어요. \(스포트 라인트에 적용할 원하는 [Color](https://ditoland-utplus.gitbook.io/ditoland/api-reference/common/color)값 \)

샘플

```lua
Workspace.Cube:SetColor(Color.new(255, 0, 0, 255)) --오브젝트의 색상을 변경해요. (r, g, b, a)
```

| **ChangeIntensity\(float Intensity\)** |
| :--- |


스포트 라이트의 밝기 값을 변경할 수 있어요. \(원하는 밝기 값\)

샘플

```lua
local changeValue = 2
Workspace.SpotLight:ChangeIntensity(changeValue) --SpotLight의 밝기를 조절해요.
```

| **ChangeAttenuationRadius\(float radius\)** |
| :--- |


스포트 라이트의 가시 영향력 범위를 변경할 수 있어요.

샘플

```lua
Workspace.SpotLight:ChangeAttenuationRadius(700)
```

| **ChangeInnerConeAngle\(float angle\)** |
| :--- |


스포트 라이트의 안쪽 콘의 각도.

샘플

```lua
Workspace.SpotLight:ChangeInnerConeAngle(20)
```

| **ChangeOuterConeAngle\(float angle\)** |
| :--- |


스포트 라이트의 바깥쪽 콘의 각도

샘플

```lua
Workspace.SpotLight:ChangeOuterConeAngle(20)
```

## **상속받아 사용 가능한 기능들**

### **속성**

| **Parent** |
| :--- |


부모 객체를 얻을 수 있어요.   
 샘플

```lua
local parent = Workspace.Floor.Parent --오브젝트의 부모를 반환해요
print(parent:GetName())
```

### **이벤트**

| **OnCreateEvent** |
| :--- |


생성 시 호출되는 이벤트에요.   
 샘플

```lua
local cube = Workspace.Cube
local function CreateEvent()
    print("Create!")
end
cube.OnCreateEvent:Connect(CreateEvent) --오브젝트에 해당 오브젝트가 생성됐을때 호출되는 함수를 연결해요. 
Game:CreateObject(cube, Vector.new(0, 0, 0))
```

| **OnUpdateEvent** |
| :--- |


생성 후 매 프레임마다 호출되는 이벤트에요.   
 샘플

```lua
local cube = Workspace.Cube
local playTime = 0
local function UpdateEvent(updateTime) --OnUpdateEvent로 연결된 함수는 updateTime 인자가 고정적으로 들어가요.
    playTime = playTime + updateTime --시간을 기록해요.
end
cube.OnUpdateEvent:Connect(UpdateEvent) --Game이나 오브젝트에 매프레임마다 호출되는 함수를 연결해요.
```

| **OnDestroyEvent** |
| :--- |


삭제될 때 호출되는 이벤트에요.   
 샘플

```lua
local cube = Workspace.Cube
local function DestroyEvent()
    print("Destroy!")
end
cube.OnDestroyEvent:Connect(DestroyEvent) --오브젝트에 해당 오브젝트가 파괴됐을때 호출되는 함수를 연결해요.
Game:DeleteObject(cube)
```

| **OnCollisionEvent** |
| :--- |


다른 객체와 충돌할 때 호출되는 이벤트에요.   
 샘플

```lua
local cube = Workspace.Cube
local function CollisionEvent(self, target) --OnCollisionEvent로 연결된 함수는 self와 target 인자가 고정적으로 들어가요.
    if target ~= nil then
        print("CollisionEvent " .. target:GetName())
    end
end
cube.OnCollisionEvent:Connect(CollisionEvent) --Collision이 true인 오브젝트와 충돌중일때 호출되는 함수를 연결해요.
```

| **OnBeginOverlapEvent** |
| :--- |


다른 객체와 겹쳐질 때 호출되는 이벤트에요.   
 샘플

```lua
local cube = Workspace.Cube
local function BeginOverlapEvent(self, target) --OnBeginOverlapEvent 연결된 함수는 self와 target 인자가 고정적으로 들어가요.
    if target ~= nil then
        print("BeginOverlapEvent " .. target:GetName())
    end
end
cube.OnBeginOverlapEvent:Connect(BeginOverlapEvent) --Collision이 false인 오브젝트와 충돌을 시작할때 호출되는 함수를 연결해요.
```

| **OnEndOverlapEvent** |
| :--- |


다른 객체와 겹쳐짐이 끝날 때 호출되는 이벤트에요.   
 샘플

```lua
local cube = Workspace.Cube
local function EndOverlapEvent(self, target) --OnEndOverlapEvent 연결된 함수는 self와 target 인자가 고정적으로 들어가요.
    if target ~= nil then
        print("EndOverlapEvent " .. target:GetName())  
    end
end
cube.OnEndOverlapEvent:Connect(EndOverlapEvent) --Collision이 false인 오브젝트와 충돌이 끝날때 호출되는 함수를 연결해요.
```

| **OnOverlapUpdateEvent** |
| :--- |


다른 객체와 겹쳐있는 동안 매 프레임마다 호출되는 이벤트에요.   
 샘플

```lua
local cube = Workspace.Cube
local function OverlapUpdateEvent(self, target) --OnOverlapUpdateEvent로 연결된 함수는 self와 target 인자가 고정적으로 들어가요.
    if target ~= nil then
        print("OverlapUpdateEvent " .. target:GetName())
    end
end
cube.OnOverlapUpdateEvent:Connect(OverlapUpdateEvent) --Collision이 false인 오브젝트와 충돌중일때 호출되는 함수를 연결해요.
```

| **ConnectChangeEventFunction\(string ValueName, function FunctionName\)** |
| :--- |


추가된 값이 변경 될 때 호출되는 이벤트에요. \(Value 이름, 연결 함수\)   
 샘플

```lua
local cube = Workspace.Cube

wait(1)
cube.SomeValue = 1

local function ChangeSomeValue()
   print("ChangeSomeValue!")
end
cube:ConnectChangeEventFunction("SomeValue", ChangeSomeValue)  --오브젝트의 "SomeValue" 라는 Value가 변경되면 ChangeSomeValue 함수를 호출해요.
```

### **함수**

| **int GetModeObjectKey\(\)** |
| :--- |


객체의 키 값을 얻을 수 있어요.   
   


| **Matrix GetTransform\(\)** |
| :--- |


매트릭스를 얻을 수 있어요.   
 샘플

```lua
local targetTransform = Game:GetAllPlayer()[1]:GetTransform()
```

| **SetTransform\(Matrix\)** |
| :--- |


현재 매트릭스에서 설정 된 매트릭스로 보간이 되는 매트릭스를 설정할 수 있어요 설정할 수 있어요. \(Matrix 값, bool 충돌 처리 여부\)   
 샘플

```lua
local character = Game:GetAllPlayer()[1]:GetCharacter()
local targetTransform = character:GetTransform()
targetTransform:SetLocation(Vector.new(0, 100, 0))
targetTransform:SetRotation(Vector.new(0, 100, 0))
character:SetTransform(targetTransform) --오브젝트를 보간으로 이동시켜요. (캐릭터는 보간없이 움직여요.)
```

| **Teleport\(Matrix\)** |
| :--- |


순간이동 하는 매트릭스를 설정할 수 있어요. \(Matrix 값\)   
 샘플

```lua
local targetTransform = Workspace.Cube:GetTransform()    
targetTransform:SetLocation(Vector.new(0, 100, 0))   
Workspace.Cube:Teleport(targetTransform) --오브젝트를 보간없이 바로 이동시켜요.
```

| **Vector GetLocation\(\)** |
| :--- |


\(Deprecated\)객체의 현재 위치를 얻을 수 있어요.   
 샘플

```lua
local character = Game:GetAllPlayer()[1]:GetCharacter()
local characterPos = character:GetTransform():GetLocation() --캐릭터의 위치값을 Vector로 반환해요.
```

| **SetLocation\(Vector position, bool collisionCheck\)** |
| :--- |


\(Deprecated\)객체의 위치를 설정할 수 있어요. \(설정할 위치 Vector 값, 충돌 처리 여부\)   
   


| **Vector GetRotation\(\)** |
| :--- |


\(Deprecated\)각도를 얻을 수 있어요. \(Vector.X : Pitch, Vector.Y : Yaw, Vector.Z : Roll\)   
 샘플

```lua
local character = Game:GetAllPlayer()[1]:GetCharacter()
local characterRot = character:GetTransform():GetRotation() --캐릭터의 회전값을 Vector로 반환해요.
```

| **SetRotation\(Vector InValue\)** |
| :--- |


\(Deprecated\)주어진 값으로 각도를 설정해요. \(InValue.X : Roll, InValue.Y : Pitch, InValue.Z : Yaw\)   
 샘플

```lua
local character = Game:GetAllPlayer()[1]:GetCharacter()
local targetTransform = character:GetTransform()
targetTransform:SetLocation(Vector.new(0, 100, 0))
targetTransform:SetRotation(Vector.new(0, 100, 0))
character:SetTransform(targetTransform) --오브젝트를 보간으로 이동시켜요. (캐릭터는 보간없이 움직여요.)
```

| **Vector GetScale\(\)** |
| :--- |


\(Deprecated\)스케일을 얻을 수 있어요   
 샘플

```lua
local cube = Workspace.Cube
local scale = cube:GetScale() --해당 오브젝트의 크기를 100으로 나눠서 Vector로 반환해요.(예를 들어 x값이 100이면 1로 반한돼요.)
scale.Y = scale.Y + 0.5
cube:SetScale(scale) --오브젝트의 크기를 설정해요.
```

| **SetScale\(Vector scale\)** |
| :--- |


\(Deprecated\)주어진 값으로 스케일을 설정해요. \(설정할 스케일 값\)   
 샘플

```lua
local cube = Workspace.Cube
local scale = cube:GetScale() --해당 오브젝트의 크기를 100으로 나눠서 Vector로 반환해요.(예를 들어 x값이 100이면 1로 반한돼요.)
scale.Y = scale.Y + 0.5
cube:SetScale(scale) --오브젝트의 크기를 설정해요.
```

| **SetTag\(String Tag\)** |
| :--- |


객체의 tag를 설정해요. \(설정할 tag\)   
 샘플

```lua
print(Workspace.Floor:GetTag())
Workspace.Floor:SetTag("SomeTag")
print(Workspace.Floor:GetTag())
```

| **String GetTag\(\)** |
| :--- |


객체에 설정된 tag를 얻을 수 있어요.   
 샘플

```lua
print(Workspace.Floor:GetTag())
Workspace.Floor:SetTag("SomeTag")
print(Workspace.Floor:GetTag())
```

| **SetForward\(Vector Forward\)** |
| :--- |


\(Deprecated\)객체의 바라보는 방향을 설정할 수 있어요. \(설정할 방향 Vector 값\)   
   


| **Vector GetForward\(\)** |
| :--- |


\(Deprecated\)객체의 바라보는 방향을 얻을 수 있어요.   
   


| **Vector GetRight\(\)** |
| :--- |


\(Deprecated\)객체의 오른쪽 방향을 얻을 수 있어요.   
   


| **bool Enable** |
| :--- |


객체 활성화 여부   
 샘플

```lua
Workspace.Cube.Enable = false --오브젝트의 상태를 비활성화해요. (자식 오브젝트가 있다면 자식들의 상태도 모두 false가 되요. 단, 충돌영역에는 영향이 없어요.)
```

| **AddForce\(Vector Force\)** |
| :--- |


객체에 물리 힘을 추가할 수 있어요. \(힘을 가할 Vector 값\)   
 샘플

```lua
local toy = Script.Parent
local pushingForce = 400 --미는 힘이에요.
local upForce = 5000 --공중으로 띄울 힘이에요.

local function CharacterCollision(self, target)
   if target == nil or not target:IsCharacter() then
       return
   end

   local selfLocation = self:GetTransform():GetLocation()
   local targetLocation = target:GetTransform():GetLocation()

   --캐릭터를 밀 방향을 구한 다음 미는 힘을 곱해요.
   local force = Vector.new((targetLocation.X - selfLocation.X) * pushingForce, (targetLocation.Y - selfLocation.Y) * pushingForce, upForce)
   target:AddForce(force) --force값만큼 캐릭터를 밀어요.
end
toy.OnCollisionEvent:Connect(CharacterCollision) --오브젝트에 캐릭터가 닿으면 호출할 함수를 연결해요.
```

| **SetVisibility\(bool bNewVisibility\)** |
| :--- |


객체의 가시성 여부를 설정할 수 있어요. \(가시성 여부\)   
 샘플

```lua
Workspace.Cube.SetVisibility(false) --오브젝트를 보이지 않게 해요.
```

| **AddLocalMove\(string TrackName, Vector Pos, float Time, bool CheckCollision\)** |
| :--- |


로컬 좌표를 기준으로 이동 변화를 추가할 수 있어요. \(설정할 Track 이름, 이동 변화를 줄 값, 완료까지 걸리는 시간, 충돌 처리 여부\)   
 샘플

```lua
local cube = Workspace.Cube
local pos = Vector.new(0, 500, 0)
local moveSpeed = 2
local waitTime = 1

cube:AddLocalMove("Move", Vector.new(pos.X, pos.Y, pos.Z), moveSpeed, false) --이동 트랙을 등록해요. (이동 트랙은 여러개도 등록할 수 있어요.)
cube:AddEmpty("Move", waitTime) --대기 트랙을 등록해요.
cube:AddLocalMove("Move", Vector.new(-pos.X, -pos.Y, -pos.Z), moveSpeed, false)
cube:AddEmpty("Move", waitTime)cube:PlayTransformTrack("Move", Enum.TransformPlayType.Repeat, InfinityPlay) --이름에 해당하는 트랙을 재생해요.
```

| **AddLocalRot\(string TrackName, Vector Rot, float Time\)** |
| :--- |


로컬 좌표를 기준으로 회전 변화를 추가할 수 있어요. \(설정할 Track 이름, 회전 변화를 줄 값, 완료까지 걸리는 시간\)   
 샘플

```lua
local cube = Workspace.Cube
local moveSpeed = 2
cube:AddLocalRot("Rot", Vector.new(0, 0, 360), moveSpeed) --회전 트랙을 등록해요.
cube:AddLocalRot("Rot", Vector.new(0, 360, 0), moveSpeed) --회전 트랙은 여러개도 등록할 수 있어요.
cube:PlayTransformTrack("Rot", Enum.TransformPlayType.Repeat, InfinityPlay) --이름에 해당하는 트랙을 재생해요.
```

| **AddLocalScale\(string TrackName, Vector Scale, float Time\)** |
| :--- |


로컬 좌표를 기준으로 스케일 변화를 추가할 수 있어요. \(설정할 Track 이름, 스케일 변화를 줄 값, 완료까지 걸리는 시간\)   
 샘플

```lua
local cube = Workspace.Cube
local moveSpeed = 2
cube:AddLocalScale("Size", Vector.new(0.6, 0.6, 0.6), moveSpeed) --크기 트랙을 등록해요.
cube:AddLocalScale("Size", Vector.new(-0.6, -0.6, -0.6), moveSpeed) --크기 트랙은 여러개도 등록할 수 있어요.
cube:PlayTransformTrack("Size", Enum.TransformPlayType.Repeat, InfinityPlay) --이름에 해당하는 트랙을 재생해요.
```

| **AddWorldMove\(string TrackName, Vector Pos, float Time, bool CheckCollision\)** |
| :--- |


월드 좌표를 기준으로 이동 변화를 추가할 수 있어요. \(설정할 Track 이름, 이동 변화를 줄 값, 완료까지 걸리는 시간, 충돌 처리 여부\)   
 샘플

```lua
local cube = Workspace.Cube
local pos = Vector.new(0, 500, 0)
local moveSpeed = 2
local waitTime = 1

cube:AddWorldMove("Move", Vector.new(pos.X, pos.Y, pos.Z), moveSpeed, false) --이동 트랙을 등록해요. (이동 트랙은 여러개도 등록할 수 있어요.)
cube:AddEmpty("Move", waitTime) --대기 트랙을 등록해요.
cube:AddWorldMove("Move", Vector.new(-pos.X, -pos.Y, -pos.Z), moveSpeed, false)
cube:AddEmpty("Move", waitTime)cube:PlayTransformTrack("Move", Enum.TransformPlayType.Repeat, InfinityPlay) --이름에 해당하는 트랙을 재생해요.
```

| **AddWorldRot\(string TrackName, Vector Rot, float Time\)** |
| :--- |


월드 좌표를 기준으로 회전 변화를 추가할 수 있어요. \(설정할 Track 이름, 회전 변화를 줄 값, 완료까지 걸리는 시간\)   
 샘플

```lua
local cube = Workspace.Cube
local moveSpeed = 2
cube:AddWorldRot("Rot", Vector.new(0, 0, 360), moveSpeed) --회전 트랙을 등록해요.
cube:AddWorldRot("Rot", Vector.new(0, 360, 0), moveSpeed) --회전 트랙은 여러개도 등록할 수 있어요.
cube:PlayTransformTrack("Rot", Enum.TransformPlayType.Repeat, InfinityPlay) --이름에 해당하는 트랙을 재생해요.
```

| **AddEmpty\(string TrackName, float Time\)** |
| :--- |


객체 변환에 대기 시간을 추가할 수 있어요. \(추가할 Track 이름, 대기 시간\)   
 샘플

```lua
local cube = Workspace.Cube
local pos = Vector.new(0, 500, 0)
local moveSpeed = 2
local waitTime = 1

cube:AddLocalMove("Move", Vector.new(pos.X, pos.Y, pos.Z), moveSpeed, false) --이동 트랙을 등록해요. (이동 트랙은 여러개도 등록할 수 있어요.)
cube:AddEmpty("Move", waitTime) --대기 트랙을 등록해요.
cube:AddLocalMove("Move", Vector.new(-pos.X, -pos.Y, -pos.Z), moveSpeed, false)
cube:AddEmpty("Move", waitTime)cube:PlayTransformTrack("Move", Enum.TransformPlayType.Repeat, InfinityPlay) --이름에 해당하는 트랙을 재생해요.
```

| **PlayTransformTrack\(string TrackName, TransformPlayType Type, int PlayCount\)** |
| :--- |


설정된 변환 컨트롤러를 실행시켜요. \(실행할 Track 이름, [Enum.TransformPlayType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/transformplaytype), 실행 횟수\)   
 샘플

```lua
local cube = Workspace.Cube
local pos = Vector.new(0, 500, 0)
local moveSpeed = 2
local waitTime = 1

cube:AddLocalMove("Move", Vector.new(pos.X, pos.Y, pos.Z), moveSpeed, false) --이동 트랙을 등록해요.
cube:AddLocalMove("Move", Vector.new(0, 0, 0), waitTime, false) --이동 트랙은 여러개도 등록할 수 있어요.
cube:AddLocalMove("Move", Vector.new(-pos.X, -pos.Y, -pos.Z), moveSpeed, false)
cube:AddLocalMove("Move", Vector.new(0, 0, 0), waitTime, false)
cube:PlayTransformTrack("Move", Enum.TransformPlayType.Repeat, InfinityPlay) --이름에 해당하는 트랙을 재생해요.
```

| **StopTransformTrack\(string TrackName\)** |
| :--- |


변환 컨트롤러를 정지시켜요. \(정지할 Track 이름\)   
 샘플

```lua
local cube = Workspace.Cube
cube:StopTransformTrack("Move") --이름에 해당하는 트랙을 멈춰요.
```

| **PauseTransformTrack\(string TrackName\)** |
| :--- |


변환 컨트롤러를 일시 정지시켜요 \(일시 정지할 Track 이름\)   
 샘플

```lua
local cube = Workspace.Cube
cube:PauseTransformTrack("Move") --이름에 해당하는 트랙을 일시정지해요.
```

| **ResumeTransformTrack\(string TrackName\)** |
| :--- |


변환 컨트롤러를 다시 플레이시켜요. \(플레이할 Track 이름\)   
 샘플

```lua
local cube = Workspace.Cube
cube:ResumeTransformTrack("Move") --이름에 해당하는 일시정지된 트랙을 다시 재생해요.
```

| **bool IsPlayingTransformTrack\(string TrackName\)** |
| :--- |


해당 TransformTrack이 플레이 중인지 확인할 수 있어요. \(확인할 Track 이름\)   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsPlayingTransformTrack("Move") == true then --이름에 해당하는 트랙이 재생중이면 true를 반환해요.
    print("Track is Playing")
end
```

| **ResetTransformTrack\(string TrackName\)** |
| :--- |


해당 TransformTrack 이 적용되기 전의 Transform으로 리셋시켜요. \(리셋할 Track 이름\)   
 샘플

```lua
local cube = Workspace.Cube
cube:ResetTransformTrack("Move") --이름에 해당하는 트랙이 적용되기전의 트랜스폼으로 리셋해요. (트랙이 멈추진 않아요.)
```

| **RemoveTransformTrack\(String TrackName\)** |
| :--- |


해당 Track을 제거해요. \(제거할 Track 이름\)   
 샘플

```lua
local cube = Workspace.Cube
cube:RemoveTransformTrack("Move") --이름에 해당하는 트랙을 제거해요.
```

| **ResetTransform\(\)** |
| :--- |


TransformTrack 이 적용되기 전의 최초 Transform으로 리셋시켜요.   
 샘플

```lua
local cube = Workspace.Cube
cube:ResetTransform() --적용되기전의 트랜스폼으로 리셋해요. (트랙이 멈추진 않아요.)
```

| **SetEndEventTransformTrack\(String TrackName, LuaScriptFunction function\)** |
| :--- |


TransformTrack 이 끝나면 등록한 function 을 호출합니다.   
 샘플

```lua
local cube = Workspace.Cube
local pos = Vector.new(200, 0, 0)
local moveSpeed = 2

cube:AddLocalMove("Move", pos, moveSpeed, false)

local function EndMove()
    print("EndMove!")
end
cube:SetEndEventTransformTrack("Move", EndMove) --이름에 해당하는 트랙이 끝나면 호출되는 함수를 연결해요.

cube:PlayTransformTrack("Move", Enum.TransformPlayType.Repeat, 1)
```

| **SetFriction\( float value, float restitution, float density \)** |
| :--- |


오브젝트의 표면 물리 마찰력을 설정할 수 있어요. \(마찰 값, 탄성 값, 밀도 값\)   
   


| **MakeVehicleChassis\( VehicleCreationInfo Info \)** |
| :--- |


오브젝트를 VehicleChassis로 변경시켜요. \(변경할 [VehicleCreationInfo데이터](https://ditoland-utplus.gitbook.io/ditoland/api-reference/common/vehiclecreationinfo)\)   
   


| **SetName\(string NewName\)** |
| :--- |


오브젝트의 이름을 변경 할 수 있어요. \(새로운 이름\)   
 샘플

```lua
Workspace.Floor:SetName("NewFloor") --오브젝트의 이름을 변경해요.
```

| **FRModeVehicle GetVehicle\(\)** |
| :--- |


Vehicle 객체를 얻을 수 있어요.   
   


| **ConnectEventFunction\(string customevent, LuaScriptFunction function\)**  |
| :--- |


유저가 추가한 오브젝트 커스텀 이벤트에 함수를 연결할 수 있어요. \(이벤트 이름, 연결 함수\)   
 샘플

```lua
local cube = Workspace.cube
local function SomeFunc(playerName) --필요하다면 함수의 인자도 넣을 수 있어요. 단, 숫자나 문자열 인자만 넣을 수 있어요.
    print("Call SomeFunc from " .. playerName)
end
cube:ConnectEventFunction("SomeFunc", SomeFunc) --오브젝트에 "SomeFunc"라는 이벤트 이름으로 SomeFunc 함수를 연결해요.
                                                --오브젝트가 아닌 Game에도 연결할 수 있어요. 그러나 그룹과 폴더에는 연결할 수 없어요.
                                                --같은 대상에 등록된 이벤트만 호출할 수 있어요.
```

| **void LookAt\(vector location\)** |
| :--- |


오브젝트가 해당하는 위치를 바라보게 할 수 있어요. \(바라볼 위치 Vector\)  
  
   


| **string GetName\(\)** |
| :--- |


객체의 이름을 얻을 수 있어요.   
 샘플

```lua
print(Workspace.Floor:GetName()) --오브젝트의 이름을 문자열로 반환해요.
```

| **RModeObject GetParent\(string ParentName\)** |
| :--- |


이름으로 부모 객체를 얻을 수 있어요. \(찾고싶은 부모 객체 이름\)   
   


| **RModeObject GetChild\(string ChildName\)** |
| :--- |


이름으로 자식 객체를 얻을 수 있어요. \(찾고싶은 자식 객체 이름\)   
   


| **RModeObject GetGetSibling\(string Name\)** |
| :--- |


이름으로 형제 객체를 얻을 수 있어요. \(찾고싶은 형제 객체 이름\)   
   


| **List GetChildList\(\)** |
| :--- |


자식 객체의 리스트를 얻을 수 있어요.   
 샘플

```lua
local uiList = Workspace.HUD:GetChildList() --오브젝트의 자식 오브젝트를 리스트로 반환해요.
for i = 1, #uiList do --리스트앞에 #을 붙여 리스트의 길이를 가져올 수 있어요.
    print(uiList[i]:GetName())
end
```

| **bool IsCharacter\(\)** |
| :--- |


캐릭터인지 확인할 수 있어요.   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsCharacter() == true then --오브젝트가 Character면 true를 반환해요.
    print(cube:GetName() .. " Is Character")
end
```

| **bool IsStaticMesh\(\)** |
| :--- |


스테틱 메시인지 확인할 수 있어요.   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsStaticMesh() == true then --오브젝트가 StaticMesh면 true를 반환해요.
    print(cube:GetName() .. " Is StaticMesh")
end
```

| **bool IsFX\(\)** |
| :--- |


FX인지 확인할 수 있어요.   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsFX() == true then --오브젝트가 FX면 true를 반환해요.
    print(cube:GetName() .. " Is FX")
end
```

| **bool IsSound\(\)** |
| :--- |


Sound인지 확인할 수 있어요.   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsSound() == true then --오브젝트가 Sound면 true를 반환해요.
    print(cube:GetName() .. " Is Sound")
end
```

| **bool IsPointLight\(\)** |
| :--- |


포인트 라이트인지 확인할 수 있어요.   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsPointLight() == true then --오브젝트가 PointLight면 true를 반환해요.
    print(cube:GetName() .. " Is PointLight")
end
```

| **bool IsSpotLight\(\)** |
| :--- |


스포트 라이트인지 확인할 수 있어요.   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsSpotLight() == true then --오브젝트가 SpotLight면 true를 반환해요.
    print(cube:GetName() .. " Is SpotLight")
end
```

| **bool IsSurfaceUI\(\)** |
| :--- |


서피스 UI인지 확인할 수 있어요.   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsSurfaceUI() == true then --오브젝트가 SurfaceUI면 true를 반환해요.
    print(cube:GetName() .. " Is SurfaceUI")
end
```

| **bool IsScreenUI\(\)** |
| :--- |


스크린 UI인지 확인할 수 있어요.   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsScreenUI() == true then --오브젝트가 ScreenUI면 true를 반환해요.
    print(cube:GetName() .. " Is ScreenUI")
end
```

| **bool IsItem\(\)** |
| :--- |


아이템인지 확인할 수 있어요.   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsItem() == true then --오브젝트가 Item면 true를 반환해요.
    print(cube:GetName() .. " Is Item")
end
```

| **bool IsNPC\(\)** |
| :--- |


NPC인지 확인할 수 있어요.   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsNPC() == true then --오브젝트가 NPC면 true를 반환해요.
    print(cube:GetName() .. " Is NPC")
end
```

| **bool IsFolder\(\)** |
| :--- |


폴더인지 확인할 수 있어요.   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsFolder() == true then --오브젝트가 Folder면 true를 반환해요.
    print(cube:GetName() .. " Is Folder")
end
```

| **bool IsScript\(\)** |
| :--- |


스트립트인지 확인할 수 있어요.   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsScript() == true then --오브젝트가 Script면 true를 반환해요.
    print(cube:GetName() .. " Is Script")
end
```

| **bool IsCollider\(\)** |
| :--- |


Collider인지 확인할 수 있어요.   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsCollider() == true then --오브젝트가 Collider면 true를 반환해요.
    print(cube:GetName() .. " Is Collider")
end
```

| **bool IsWidget\(\)** |
| :--- |


Widget인지 확인할 수 있어요.   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsWidget() == true then --오브젝트가 Widget면 true를 반환해요.
    print(cube:GetName() .. " Is Widget")
end
```

| **bool IsCamera\(\)** |
| :--- |


Camera인지 확인할 수 있어요.   
 샘플

```lua
local cube = Workspace.Cube
if cube:IsCamera() == true then --오브젝트가 Camera면 true를 반환해요.
    print(cube:GetName() .. " Is Camera")
end
```

| **bool IsValid\(\)** |
| :--- |


해당 오브젝트가 유효한지 확인 할 수있어요.   
   


| **AddReplicateValue\(string ValueName, Vector Data, ReplicateType Type, float Time, bool bSaveToStorage\)** |
| :--- |


해당 객체에 서버, 클라이언트 간 동기화가 가능한 벡터를 추가해요. \(추가할 Value 이름, Vector 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부\)   
 샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeVector", Vector.new(0, 50, 0), Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeVector)

--클라 스크립트에서-------------
print(Game.SomeVector) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```

| **AddReplicateValue\(string ValueName, float Data, ReplicateType Type, float Time, bool bSaveToStorage\)** |
| :--- |


해당 객체에 서버, 클라이언트 간 동기화가 가능한 실수를 추가해요. \(추가할 Value 이름, float 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부\)   
 샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeNumber", 1, Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeNumber .. " in Server")

--클라 스크립트에서-------------
print(Game.SomeNumber .. " in Client") --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```

| **AddReplicateValue\(string ValueName, bool Data, ReplicateType Type, float Time, bool bSaveToStorage\)** |
| :--- |


해당 객체에 서버, 클라이언트 간 동기화가 가능한 bool를 추가해요. \(추가할 Value 이름, bool 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부\)   
 샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeBool", true, Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeBool)

--클라 스크립트에서-------------
print(Game.SomeBool) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```

| **AddReplicateValue\(string ValueName, string Data, ReplicateType Type, float Time, bool bSaveToStorage\)** |
| :--- |


해당 객체에 서버, 클라이언트 간 동기화가 가능한 문자열을 추가해요. \(추가할 Value 이름, string 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부\)   
 샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeString", "Hello World!", Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeString)

--클라 스크립트에서-------------
print(Game.SomeString) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```

| **AddReplicateValue\(string ValueName, Color Data, ReplicateType Type, float Time, bool bSaveToStorage\)** |
| :--- |


해당 객체에 서버, 클라이언트 간 동기화가 가능한 컬러를 추가해요. \(추가할 Value 이름, Color 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부\)   
 샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeColor", Color.new(255, 0, 0, 255), Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeColor)

--클라 스크립트에서-------------
print(Game.SomeColor) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```

| **AddSaveValue\(string ValueName, Vector Data\)** |
| :--- |


해당 객체 저장소에 벡터를 추가해요. \(Value 이름, Vector 데이터\)   
   


| **AddSaveValue\(string ValueName, float Data\)** |
| :--- |


해당 객체 저장소에 실수를 추가해요. \(Value 이름, float 데이터\)   
   


| **AddSaveValue\(string ValueName, bool Data\)** |
| :--- |


해당 객체 저장소에 bool을 추가해요. \(Value 이름, bool 데이터\)   
   


| **AddSaveValue\(string ValueName, string Data\)** |
| :--- |


해당 객체 저장소에 문자열을 추가해요. \(Value 이름, string 데이터\)   
   


| **AddSaveValue\(string ValueName, Color Data\)** |
| :--- |


해당 객체 저장소에 칼라를 추가해요. \(Value 이름, Color 데이터\)

