# NPC

클라이언트에서 사용되는 NPC 개체에요.

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

| **SetLocation\(Vector position\)** |
| :--- |


\(Deprecated\)위치를 설정할 수 있어요. \(위치 값\)   
 샘플

```lua
local character = Game:GetAllPlayer()[1]:GetCharacter()
local targetTransform = character:GetTransform()
targetTransform:SetLocation(Vector.new(0, 100, 0))
targetTransform:SetRotation(Vector.new(0, 100, 0))
character:SetTransform(targetTransform) --오브젝트를 보간으로 이동시켜요. (캐릭터는 보간없이 움직여요.)
```

| **SetRotation\(Vector Rotator\)** |
| :--- |


\(Deprecated\)회전을 설정할 수 있어요. \(회전 값\)   
 샘플

```lua
local character = Game:GetAllPlayer()[1]:GetCharacter()
local targetTransform = character:GetTransform()
targetTransform:SetLocation(Vector.new(0, 100, 0))
targetTransform:SetRotation(Vector.new(0, 100, 0))
character:SetTransform(targetTransform) --오브젝트를 보간으로 이동시켜요. (캐릭터는 보간없이 움직여요.)
```

| **Matrix GetTransform\(\)** |
| :--- |


매트릭스를 얻을 수 있어요.   
 샘플

```lua
local targetTransform = Game:GetAllPlayer()[1]:GetTransform()
```

| **SetTransform\(Matrix\)** |
| :--- |


매트릭스를 설정할 수 있어요. \(Matrix 값\)   
 샘플

```lua
local character = Game:GetAllPlayer()[1]:GetCharacter()
local targetTransform = character:GetTransform()
targetTransform:SetLocation(Vector.new(0, 100, 0))
targetTransform:SetRotation(Vector.new(0, 100, 0))
character:SetTransform(targetTransform) --오브젝트를 보간으로 이동시켜요. (캐릭터는 보간없이 움직여요.)
```

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

