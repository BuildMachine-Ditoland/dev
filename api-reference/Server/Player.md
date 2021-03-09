
게임에 참여한 플레이어 객체에요. 이 기능들은 서버에서만 사용 가능해요. 
## **함수**

<br>
<br>
<br>
  RModeServerCharacter GetCharacter()

플레이어의 캐릭터를 얻을 수 있어요. 

샘플 

```lua
local player = Game:GetAllPlayer()[1]
local character = player:GetCharacter() --플레이어의 캐릭터를 반환해요.
```
<br>
<br>
<br>
  string GetPlayerName()

플레이어의 이름을 얻을 수 있어요. 

샘플 

```lua
local character = Game:GetAllPlayer()[1]:GetCharacter()
print(character:GetPlayerName()) --캐릭터의 플레이어 이름을 문자열로 반환해요.
```
<br>
<br>
<br>
  string GetTeamName()

플레이어가 속해있는 팀 이름을 얻을 수 있어요. 

샘플 

```lua
local teamName = "Blue Team"
local team = Game:AddTeam(teamName) --이름으로 팀을 추가한뒤, 추가한 팀을 반환해요.
local spawnGroup = Game:AddSpawnPointGroup(teamName) --이름으로 스폰 그룹을 등록해요.
local spawnRadius = 50 --팀별 캐릭터 스폰 반경을 설정해요.
            
team:AddUsingCharacter(Workspace.Character) --팀별로 사용하는 캐릭터를 따로 지정할 수도 있어요.            
team:SetUsingSpawnPointGroup(teamName) --팀에서 사용할 스폰 그룹을 설정해요.     

local spawner = Game:AddSpawnPointAtGroup(teamName, Workspace.SpawnPoint) --스폰 그룹에서 사용할 스폰포인트를 등록해요.
spawner:SetSpawnType(Enum.PointSpawnType.Area, spawnRadius) --팀의 스폰타입을 설정해요.

Game:SetTeamSetting(Enum.DivideTeamType.Order) --팀에 플레이어를 분배하는 방식을 설정해요.
Game:SetSpawnType(Enum.SpawnType.UseTeamSpawn) --게임의 캐릭터 스폰 방식을 설정해요.
Game:ApplyTeamSetting() --팀 설정을 적용해요.

local function SpawnCharacter(character) 
    print(character:GetName() .. "'s' Team : " .. character:GetPlayer():GetTeamName()) --팀 이름을 반환해요.
end
Game.OnSpawnCharacter:Connect(SpawnCharacter) 
```
<br>
<br>
<br>
  int GetLifeCount()

플레이어의 남은 목숨 개수를 얻을 수 있어요. 

샘플 

```lua
local player = Game:GetAllPlayer()[1] 
print(player:GetLifeCount())
```
<br>
<br>
<br>
  KillCharacter()

플레이어 캐릭터를 죽게 하는 함수에요. 

샘플 

```lua
local player = Game:GetAllPlayer()[1]
player:KillCharacter() --플레이어의 캐릭터를 죽여요.
```
<br>
<br>
<br>
  RespawnCharacter()

플레이어 캐릭터를 리스폰 시키는 함수에요. 

샘플 

```lua
local player = Game:GetAllPlayer()[1]
player:RespawnCharacter() --플레이어의 캐릭터를 리스폰해요.
```
<br>
<br>
<br>
  SetCheckPoint(RSpawnPoint SpawnPointObject)

플레이어의 체크 포인트를 설정할 수 있어요 (설정할 스폰 포인트 오브젝트) 
<br>
<br>
<br>
  SetCheckPoint(RWorldObject WorldObject)

플레이어의 체크 포인트를 설정할 수 있어요 (설정할 월드 오브젝트) 
<br>
<br>
<br>
  SetFreeCamMode(bool bFreeCam)

플레이어의 프리캠 모드 사용여부를 설정할 수 있어요. (프리캠 사용 여부) 

샘플 

```lua
local player = Game:GetAllPlayer()[1]
player:SetFreeCamMode(true)
```
<br>
<br>
<br>
  RequestFreeCam(float WaitTime)

지정된 시간이 지난 후에 플레이어의 프리캠 모드를 요청해요. (대기 시간) 

샘플 

```lua
local player = Game:GetAllPlayer()[1]
player:RequestFreeCam(3) --3초후 프리캠이 시작되요.
```
<br>
<br>
<br>
  int GiveItem(ModeItemServer Item, int Count)

플레이어에게 아이템을 줄 수 있어요. (줄 아이템, 개수) return 인벤토리 인텍스 
<br>
<br>
<br>
  int GiveItem(ModeItemServer Item)

플레이어에게 아이템을 줄 수 있어요. (줄 아이템) return 인벤토리 인텍스 

샘플 

```lua
local player = Game:GetAllPlayer()[1]
local item = Script.Parent

wait(2)
player:GiveItem(item) --플레이어에게 아이템을 지급해요.
```
<br>
<br>
<br>
  int GetInventorySize()

플레이어의 인벤토리 사이즈를 얻을 수 있어요. 

샘플 

```lua
local player = Game:GetAllPlayer()[1]
print(player:GetInventorySize()) --플레이어의 인벤토리 사이즈를 숫자로 반환해요.
```
<br>
<br>
<br>
  ClearItem()

플레이어의 아이템을 모두 제거해요. 

샘플 

```lua
local function ClearItem(character)
    if character:IsCharacter() ~= true then
        return
    end   
   
    character:GetPlayer():ClearItem() --플레이어의 아이템을 모두 제거해요.
end
Game.OnDeathCharacter:Connect(ClearItem)
```
<br>
<br>
<br>
  EquipInventoryItem(int InventoryIndex)

플레이어 캐릭터에 아이템을 장착시킬 수 있어요. (장착 할 인벤토리 칸) 

샘플 

```lua
local item = Script.Parent
local collider = Item.BoxCollider

local function GetItem(self, character)
    if not character:IsCharacter() then
        return   
    end

    local player = character:GetPlayer()
    local size = player:GetInventorySize()
   
    player:GiveItem(item) --플레이어에게 아이템을 지급해요.

    for i = 0, size do
        if player:GetInventoryItem(i) ~= nil and player:GetInventoryItem(i):GetName() == item:GetName() then --플레이어 인벤토리에서 이름으로 아이템을 찾아요.
            player:EquipInventoryItem(i) --플레이어 캐릭터에 아이템을 장착시켜요.
            Game:DeleteObject(item)
        end 
    end   
end
collider.OnBeginOverlapEvent:Connect(GetItem)
```
<br>
<br>
<br>
  SetEnableCollisionBetweenCharacters(bool Enable)

플레이어간의 충돌 여부를 설정할 수 있어요. (충돌 여부) 

샘플 

```lua
local player = Game:GetAllPlayer()[1]
player:SetEnableCollisionBetweenCharacters(false) --특정 플레이어가 다른 캐릭터와 충돌되지 않게 설정해요.
```
<br>
<br>
<br>
  SetUserCollisionTypeResponse(string UserCollisionType, CollisionResponse Response)

유저가 충돌 시 발생 타입을 설정할 수 있어요. (충돌 타입 이름 설정, [Enum.CollisionResponse.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/collisionresponse)) 

샘플 

```lua
local cube = Workspace.Cube
Game:AddUserCollisionType("CollisionTag1") --유저 충돌 타입을 추가해요.
cube:SetUserCollisionTypeResponse("CollisionTag1", Enum.CollisionResponse.Overlap) --유저 타입 충돌 물체의 충돌 시 처리를 변경하는 함수에요.
```
<br>
<br>
<br>
  bool HaveInventorySaveData()

저장소에 인번토리에 대한 데이터가 저장되어 있는지 확인할 수 있어요. 

샘플 

```lua
local player = Game:GetAllPlayer()[1]
print(player:HaveInventorySaveData()) --저장소에 인번토리에 대한 데이터가 저장되어 있으면 true를 반환해요.
```
<br>
<br>
<br>
  RModeHitResult LineTrace(Vector Start, Vector Dir, float Distance)

설정된 시작 지점에서 원하는 방향으로 지정된 거리 만큼 충돌이 있는지 체크할 수 있어요. (시작 지점 Vector, 목표 지점 Vector, 거리 값) 
<br>
<br>
<br>
  ModeItemServer GetInventoryItem(int InventoryIndex)

지정된 칸의 인벤토리 아이템을 얻을 수 있어요. (인벤토리 칸) 

샘플 

```lua
local player = Game:GetAllPlayer()[1]
if player:GetInventoryItem(0) ~= nil then
    print(player:GetInventoryItem(0):GetName()) --지정된 칸의 인벤토리 아이템을 반환해요.
end
```
<br>
<br>
<br>
  ModeItemServer GetEquipItem(String EquipSlot)

플레이어 캐릭터가 착용중인 아이템을 얻을 수 있어요. (장착 중인 아이템 슬롯) 

샘플 

```lua
local player = Game:GetAllPlayer()[1]
if player:GetEquipItem("EquipSlot_1") ~= nil then
    print(player:GetEquipItem("EquipSlot_1"):GetName()) --플레이어 캐릭터가 착용중인 아이템을 반환해요.
end
```
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
| **AddTimeEvent(String EventName, float Time, LuaScriptFunction EventFuunction)** |
| :--- |
일정 시간뒤에 연결 함수가 호출되는 이벤트를 추가해요. (추가할 이벤트 이름, 시간, 연결 함수)
샘플

```lua
local waitTime = 2
local function PrintMessage() --AddTimeEvent로 등록된 함수는 일정시간을 기다린뒤, 호출돼요.
    print("Call PrintMessage!") 
end
Game:AddTimeEvent("PrintMessage", waitTime, PrintMessage) --일정시간을 기다린뒤 호출되는 함수를 문자열로 등록해요.
```
| **DeleteTimeEvent(String EventName)** |
| :--- |
등록된 시간 이벤트를 삭제해요. (삭제할 이벤트 이름)
샘플

```lua
local waitTime = 2
local function PrintMessage() --AddTimeEvent로 등록된 함수는 일정시간을 기다린뒤, 호출돼요.
    print("Call PrintMessage!") 
end
Game:AddTimeEvent("PrintMessage", waitTime, PrintMessage) --일정시간을 기다린뒤 호출되는 함수를 문자열로 등록해요.
Game:DeleteTimeEvent("PrintMessage") --AddTimeEvent로 등록한 함수를 삭제해서 호출되지 않게 해요.
```
## **함수**

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
