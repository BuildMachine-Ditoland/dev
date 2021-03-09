
여러 애니메이션을 특정 값에 따라 블렌딩하는 애니메이션 상태를 설정하는 객체에요. 

예) 이동 속도에 따른 평상시, 걷기, 달리기 애니메이션 블랜딩 등 이에요 

AddBlendAnimState 함수로 생성해요. 
## **함수**





  ModeBlendAnimationDataSetting AddBlendAnimation(float BlendValue, string AnimResourceID)

블렌딩 애니메이션을 추가해요. (블렌드 값, 리소스 ID) 




  ModeBlendAnimationDataSetting AddBlendAnimation(float BlendValue, string AnimResourceID, float PlaySpeed)

블렌딩 애니메이션을 추가해요. (블렌드 값, 리소스 ID, 플레이 속도) 
# **상속받아 사용 가능한 기능들**

## **속성**

| **Parent** |
| :--- |

부모 객체를 얻을 수 있어요. 
샘플

```lua
local parent = Workspace.Floor.Parent --오브젝트의 부모를 반환해요
print(parent:GetName()) 
```
## **이벤트**

| **OnEnter** |
| :--- |
해당 애니메이션 상태가 시작될 때 호출되는 이벤트에요.
| **OnUpdate** |
| :--- |
해당 애니메이션 상태가 실행중일 때 매프레임마다 호출되는 이벤트에요.
| **OnExit** |
| :--- |
해당 애니미에션 상태가 종료될 때 호출되는 이벤트에요.
| **ConnectChangeEventFunction(string ValueName, function FunctionName)** |
| :--- |
추가된 값이 변경 될 때 호출되는 이벤트에요. (Value 이름, 연결 함수)
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
## **함수**

| **SetNeedReplicate(bool NeedReplicate)** |
| :--- |
서버 클라이언트 간 동기화가 필요한 애니메이션 여부를 설정할 수 있어요. (동기화 여부)
서버, 클라이언트 간 동기화 되고 있는 값을 기반으로 애니메이션이 변경되는 경우 동기화 설정을 할 필요는 없어요.
예) 디폴트 애니메이션 설정의 점프 모션은 캐릭터가 현재 공중에 떠있는가를 가지고 애니메이션 상태가 변경되고 있을 때에요.
해당 판단은 서버와 클라이언트가 동기화 하고 있어 따로 동기화를 설정하지 않아도 다른 클라이언트에서도 같은 애니메이션 상태로 설정돼요.
게임 제작자가 조준 애니메이션 상태를 만들고 클라이언트 입력을 받아 조준 상태로 변경한 경우, 다른 클라이언트에서는 
조준 모션을 하지 않음 이경우 해당 값을 true로 설정하면 다른 클라이언트도 해당 애니메이션을 실행해요.
| **string GetName()** |
| :--- |
객체의 이름을 얻을 수 있어요.
샘플

```lua
print(Workspace.Floor:GetName()) --오브젝트의 이름을 문자열로 반환해요.
```
| **RModeObject GetParent(string ParentName)** |
| :--- |
이름으로 부모 객체를 얻을 수 있어요. (찾고싶은 부모 객체 이름)
| **RModeObject GetChild(string ChildName)** |
| :--- |
이름으로 자식 객체를 얻을 수 있어요. (찾고싶은 자식 객체 이름)
| **RModeObject GetGetSibling(string Name)** |
| :--- |
이름으로 형제 객체를 얻을 수 있어요. (찾고싶은 형제 객체 이름)
| **List<RScriptObject> GetChildList()** |
| :--- |
자식 객체의 리스트를 얻을 수 있어요.
샘플

```lua
local uiList = Workspace.HUD:GetChildList() --오브젝트의 자식 오브젝트를 리스트로 반환해요.
for i = 1, #uiList do --리스트앞에 #을 붙여 리스트의 길이를 가져올 수 있어요.
    print(uiList[i]:GetName())
end
```
| **bool IsCharacter()** |
| :--- |
캐릭터인지 확인할 수 있어요.
샘플

```lua
local cube = Workspace.Cube
if cube:IsCharacter() == true then --오브젝트가 Character면 true를 반환해요.
    print(cube:GetName() .. " Is Character")
end
```
| **bool IsStaticMesh()** |
| :--- |
스테틱 메시인지 확인할 수 있어요.
샘플

```lua
local cube = Workspace.Cube
if cube:IsStaticMesh() == true then --오브젝트가 StaticMesh면 true를 반환해요.
    print(cube:GetName() .. " Is StaticMesh")
end
```
| **bool IsFX()** |
| :--- |
FX인지 확인할 수 있어요.
샘플

```lua
local cube = Workspace.Cube
if cube:IsFX() == true then --오브젝트가 FX면 true를 반환해요.
    print(cube:GetName() .. " Is FX")
end
```
| **bool IsSound()** |
| :--- |
Sound인지 확인할 수 있어요.
샘플

```lua
local cube = Workspace.Cube
if cube:IsSound() == true then --오브젝트가 Sound면 true를 반환해요.
    print(cube:GetName() .. " Is Sound")
end
```
| **bool IsPointLight()** |
| :--- |
포인트 라이트인지 확인할 수 있어요.
샘플

```lua
local cube = Workspace.Cube
if cube:IsPointLight() == true then --오브젝트가 PointLight면 true를 반환해요.
    print(cube:GetName() .. " Is PointLight")
end
```
| **bool IsSpotLight()** |
| :--- |
스포트 라이트인지 확인할 수 있어요.
샘플

```lua
local cube = Workspace.Cube
if cube:IsSpotLight() == true then --오브젝트가 SpotLight면 true를 반환해요.
    print(cube:GetName() .. " Is SpotLight")
end
```
| **bool IsSurfaceUI()** |
| :--- |
서피스 UI인지 확인할 수 있어요.
샘플

```lua
local cube = Workspace.Cube
if cube:IsSurfaceUI() == true then --오브젝트가 SurfaceUI면 true를 반환해요.
    print(cube:GetName() .. " Is SurfaceUI")
end
```
| **bool IsScreenUI()** |
| :--- |
스크린 UI인지 확인할 수 있어요.
샘플

```lua
local cube = Workspace.Cube
if cube:IsScreenUI() == true then --오브젝트가 ScreenUI면 true를 반환해요.
    print(cube:GetName() .. " Is ScreenUI")
end
```
| **bool IsItem()** |
| :--- |
아이템인지 확인할 수 있어요.
샘플

```lua
local cube = Workspace.Cube
if cube:IsItem() == true then --오브젝트가 Item면 true를 반환해요.
    print(cube:GetName() .. " Is Item")
end
```
| **bool IsNPC()** |
| :--- |
NPC인지 확인할 수 있어요.
샘플

```lua
local cube = Workspace.Cube
if cube:IsNPC() == true then --오브젝트가 NPC면 true를 반환해요.
    print(cube:GetName() .. " Is NPC")
end
```
| **bool IsFolder()** |
| :--- |
폴더인지 확인할 수 있어요.
샘플

```lua
local cube = Workspace.Cube
if cube:IsFolder() == true then --오브젝트가 Folder면 true를 반환해요.
    print(cube:GetName() .. " Is Folder")
end
```
| **bool IsScript()** |
| :--- |
스트립트인지 확인할 수 있어요.
샘플

```lua
local cube = Workspace.Cube
if cube:IsScript() == true then --오브젝트가 Script면 true를 반환해요.
    print(cube:GetName() .. " Is Script")
end
```
| **bool IsCollider()** |
| :--- |
Collider인지 확인할 수 있어요.
샘플

```lua
local cube = Workspace.Cube
if cube:IsCollider() == true then --오브젝트가 Collider면 true를 반환해요.
    print(cube:GetName() .. " Is Collider")
end
```
| **bool IsWidget()** |
| :--- |
Widget인지 확인할 수 있어요.
샘플

```lua
local cube = Workspace.Cube
if cube:IsWidget() == true then --오브젝트가 Widget면 true를 반환해요.
    print(cube:GetName() .. " Is Widget")
end
```
| **bool IsCamera()** |
| :--- |
Camera인지 확인할 수 있어요.
샘플

```lua
local cube = Workspace.Cube
if cube:IsCamera() == true then --오브젝트가 Camera면 true를 반환해요.
    print(cube:GetName() .. " Is Camera")
end
```
| **bool IsValid()** |
| :--- |
해당 오브젝트가 유효한지 확인 할 수있어요.
| **AddReplicateValue(string ValueName, Vector Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |
해당 객체에 서버, 클라이언트 간 동기화가 가능한 벡터를 추가해요. (추가할 Value 이름, Vector 데이터, //@[] Enum.ReplicateType.타입 https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype , 동기화 시간, 스토리지 저장 여부)
샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeVector", Vector.new(0, 50, 0), Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeVector)

--클라 스크립트에서-------------
print(Game.SomeVector) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
| **AddReplicateValue(string ValueName, float Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |
해당 객체에 서버, 클라이언트 간 동기화가 가능한 실수를 추가해요. (추가할 Value 이름, float 데이터, //@[] Enum.ReplicateType.타입 https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype , 동기화 시간, 스토리지 저장 여부)
샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeNumber", 1, Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeNumber .. " in Server")

--클라 스크립트에서-------------
print(Game.SomeNumber .. " in Client") --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
| **AddReplicateValue(string ValueName, bool Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |
해당 객체에 서버, 클라이언트 간 동기화가 가능한 bool를 추가해요. (추가할 Value 이름, bool 데이터, //@[] Enum.ReplicateType.타입 https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype , 동기화 시간, 스토리지 저장 여부)
샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeBool", true, Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeBool)

--클라 스크립트에서-------------
print(Game.SomeBool) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
| **AddReplicateValue(string ValueName, string Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |
해당 객체에 서버, 클라이언트 간 동기화가 가능한 문자열을 추가해요. (추가할 Value 이름, string 데이터, //@[] Enum.ReplicateType.타입 https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype , 동기화 시간, 스토리지 저장 여부)
샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeString", "Hello World!", Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeString)

--클라 스크립트에서-------------
print(Game.SomeString) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
| **AddReplicateValue(string ValueName, Color Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |
해당 객체에 서버, 클라이언트 간 동기화가 가능한 컬러를 추가해요. (추가할 Value 이름, Color 데이터, //@[] Enum.ReplicateType.타입 https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype , 동기화 시간, 스토리지 저장 여부)
샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeColor", Color.new(255, 0, 0, 255), Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeColor)

--클라 스크립트에서-------------
print(Game.SomeColor) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
| **AddSaveValue(string ValueName, Vector Data)** |
| :--- |
해당 객체 저장소에 벡터를 추가해요. (Value 이름, Vector 데이터)
| **AddSaveValue(string ValueName, float Data)** |
| :--- |
해당 객체 저장소에 실수를 추가해요. (Value 이름, float 데이터)
| **AddSaveValue(string ValueName, bool Data)** |
| :--- |
해당 객체 저장소에 bool을 추가해요. (Value 이름, bool 데이터)
| **AddSaveValue(string ValueName, string Data)** |
| :--- |
해당 객체 저장소에 문자열을 추가해요. (Value 이름, string 데이터)
| **AddSaveValue(string ValueName, Color Data)** |
| :--- |
해당 객체 저장소에 칼라를 추가해요. (Value 이름, Color 데이터)
