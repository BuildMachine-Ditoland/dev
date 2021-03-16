
게임 전반적인 역할을 하는 객체에요. 여기 있는 기능들은 서버에서만 사용할 수 있어요. 
<br>
## **속성**

<br>
## **함수**

<br>
<br>
| **AddUserCollisionType(string UserCollisionType)** |
| :--- |

유저 충돌 타입 설정을 추가할 수 있어요. (충돌 타입 이름 설정) 

특정 오브젝트의 충돌 처리를 다른 오브젝트와 다르게 할 때 사용 

예) 특정 오브젝트만 통과하고, 캐릭터는 못 통과하는 오브젝트. 

<br>

샘플 

```lua
local cube = Workspace.Cube
Game:AddUserCollisionType("CollisionTag1") --유저 충돌 타입을 추가해요.
cube:SetCollisionType("CollisionTag1") --해당 오브젝트의 충돌 타입을 설정해요.
```
<br>
<br>
<br>
| **RSpawnPointGroup AddSpawnPointGroup(string SpawnPointGroupName)** |
| :--- |

게임에서 사용 할 스폰 포인트 그룹을 추가할 수 있어요. (추가할 스폰 포인트 그룹 이름) 

<br>

샘플 

```lua
local spawnList = Workspace.SpawnerList:GetChildList()
local spawnGroup = Game:AddSpawnPointGroup("SpawnGroup1") --이름으로 스폰 그룹을 등록해요.
for i = 1, #spawnList do
   local spawner = Game:AddSpawnPointAtGroup("SpawnGroup1", spawnList[i]) --스폰 그룹에서 사용할 스폰포인트를 등록해요.
   spawner:SetSpawnType(Enum.PointSpawnType.Area, 0) --스폰포인트의 작동방식을 설정해요.
end
Game:SetUsingSpawnPointGroup(spawnGroup) --게임에 적용할 스폰 그룹을 설정해요.
Game:SetSpawnType(Enum.SpawnType.UseSpawnGroup) --게임의 스폰타입을 설정해요.
```
<br>
<br>
<br>
| **RSpawnPoint AddSpawnPoint(RScriptWorldObject* RWorldObject)** |
| :--- |

게임에서 사용 할 스폰 포인트를 추가할 수 있어요. (스폰 포인트로 지정 할 오브젝트) 
<br>
<br>
| **RSpawnPoint AddSpawnPointAtGroup(string SpawnPointGroupName, RScriptWorldObject* RWorldObject)** |
| :--- |

스폰포인트 그룹에 스폰 포인트를 추가할 수 있어요. (스폰포인트를 추가할 그룹 이름, 이름, 스폰 포인트를 할 오브젝트) 

<br>

샘플 

```lua
local spawnList = Workspace.SpawnerList:GetChildList()
local spawnGroup = Game:AddSpawnPointGroup("SpawnGroup1") --이름으로 스폰 그룹을 등록해요.
for i = 1, #spawnList do
   local spawner = Game:AddSpawnPointAtGroup("SpawnGroup1", spawnList[i]) --스폰 그룹에서 사용할 스폰포인트를 등록해요.
   spawner:SetSpawnType(Enum.PointSpawnType.Area, 0) --스폰포인트의 작동방식을 설정해요.
end
Game:SetUsingSpawnPointGroup(spawnGroup) --게임에 적용할 스폰 그룹을 설정해요.
Game:SetSpawnType(Enum.SpawnType.UseSpawnGroup) --게임의 스폰타입을 설정해요.
```
<br>
<br>
<br>
| **SetSpawnType(ModeSpawnType InSpawnType)** |
| :--- |

게임의 스폰 타입을 설정할 수 있어요. ( [Enum.SpawnType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/spawntype)) 

<br>

샘플 

```lua
local spawnList = Workspace.SpawnerList:GetChildList()
local spawnGroup = Game:AddSpawnPointGroup("SpawnGroup1") --이름으로 스폰 그룹을 등록해요.
for i = 1, #spawnList do
   local spawner = Game:AddSpawnPointAtGroup("SpawnGroup1", spawnList[i]) --스폰 그룹에서 사용할 스폰포인트를 등록해요.
   spawner:SetSpawnType(Enum.PointSpawnType.Area, 0) --스폰포인트의 작동방식을 설정해요.
end
Game:SetUsingSpawnPointGroup(spawnGroup) --게임에 적용할 스폰 그룹을 설정해요.
Game:SetSpawnType(Enum.SpawnType.UseSpawnGroup) --게임의 스폰타입을 설정해요.
```
<br>
<br>
<br>
| **SetUsingSpawnPointGroup(RSpawnPointGroup* SpawnPointGroup)** |
| :--- |

게임에 적용 할 스폰 그룹을 설정할 수 있어요. (게임에 적용 할 스폰포인트 그룹 오브젝트) 

<br>

샘플 

```lua
local spawnList = Workspace.SpawnerList:GetChildList()
local spawnGroup = Game:AddSpawnPointGroup("SpawnGroup1") --이름으로 스폰 그룹을 등록해요.
for i = 1, #spawnList do
   local spawner = Game:AddSpawnPointAtGroup("SpawnGroup1", spawnList[i]) --스폰 그룹에서 사용할 스폰포인트를 등록해요.
   spawner:SetSpawnType(Enum.PointSpawnType.Area, 0) --스폰포인트의 작동방식을 설정해요.
end
Game:SetUsingSpawnPointGroup(spawnGroup) --게임에 적용할 스폰 그룹을 설정해요.
Game:SetSpawnType(Enum.SpawnType.UseSpawnGroup) --게임의 스폰타입을 설정해요.
```
<br>
<br>
<br>
| **SetUsingSpawnPoint(RSpawnPoint* SpawnPoint)** |
| :--- |

게임에 적용 할 스폰 포인트를 설정할 수 있어요. (게임에 적용 할 스폰포인트 오브젝트) 
<br>
<br>
| **SetDefaultSpawnPos(FVector Pos)** |
| :--- |

설정된 스폰 포인트가 없을 경우 지정한 위치에 스폰되도록 해요. (스폰할 위치 Vector) 
<br>
<br>
| **SetUsingCharacterSetting(RCharacterSetting CharacterSettingObject)** |
| :--- |

게임에서 적용 할 캐릭터 설정을 설정 할 수 있어요. (게임에 적용 할 캐릭터 설정 오브젝트) 
<br>
<br>
| **Team AddTeam(string TeamName)** |
| :--- |

게임에서 사용 할 팀 설정을 추가할 수 있어요. (팀 이름 설정) 

<br>

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
| **RModeNPCSetting AddNPCSetting(string NPCSettingName)** |
| :--- |

게임에서 사용 할 NPC 설정을 추가할 수 있어요. (NPC 이름 설정) 
<br>
<br>
| **Player GetPlayer(string PlayerName)** |
| :--- |

플레이어 이름으로 플레이어를 얻을 수 있어요. (얻고 싶은 플레이어 이름) 

<br>

샘플 

```lua
local player = Game:GetPlayer(PlayerName) --플레이어 이름에 해당하는 플레이어를 반환해요.
```
<br>
<br>
<br>
| **RModeServerCharacter GetPlayerCharacter(string PlayerName)** |
| :--- |

플레이어 이름으로 플레이어 캐릭터를 얻을 수 있어요. (얻고 싶은 플레이어 이름) 

<br>

샘플 

```lua
local playerName = Game:GetAllPlayer()[1]:GetName()
local character = Game:GetPlayerCharacter(playerName)
print(character:GetName())
```
<br>
<br>
<br>
| **SetTeamSetting(EModeTeamType TeamType, EDivideTeamType DivideTeamType)** |
| :--- |

게임의 팀전 여부, 팀 나누기 방식을 설정할 수 있어요. (팀 타입, [Enum.DivideTeamType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/divideteamtype)) 
<br>
<br>
| **int GetPlayerCount()** |
| :--- |

현재 게임에 참여하고 있는 플레이어 수를 얻을 수 있어요. 

<br>

샘플 

```lua
print(Game:GetPlayerCount())
```
<br>
<br>
<br>
| **ResetTeamSetting()** |
| :--- |

게임의 팀 설정을 모두 제거해요. 

<br>

샘플 

```lua
Game:ResetTeamSetting()
```
<br>
<br>
<br>
| **ApplyTeamSetting()** |
| :--- |

팀 설정 방식을 게임에 적용하는 함수에요. 

<br>

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
| **ReqResetGame()** |
| :--- |

게임 리셋을 요청하는 함수에요. 
<br>
<br>
| **SetCanEnterUser()** |
| :--- |

게임에 유저의 진입 가능 여부를 설정해요. (false로 설정 할 경우 해당 게임으로 더 이상 유저가 들어올 수 없어요.) 
<br>
<br>
| **BroadcastEvent(string CustomEventName, Args ...)** |
| :--- |

모든 클라이언트에게 이벤트를 보내는 함수에요. (이벤트 이름, 전달할 변수들 ...) 

<br>

샘플 

```lua
--서버 스크립트에서
local cube = Workspace.Cube
wait(1)
cube:BroadcastEvent("SomeFunc", 1) --모든 플레이어에게 SomeFunc() 함수를 호출해요.

--클라 스크립트에서
local cube = Workspace.cube
local function SomeFunc(id) --필요하다면 함수의 인자도 넣을 수 있어요. 단, 숫자나 문자열 인자만 넣을 수 있어요.
    print("Call SomeFunc (" .. id .. ")")
end
cube:ConnectEventFunction("SomeFunc", SomeFunc) --오브젝트에 "SomeFunc"라는 이벤트 이름으로 SomeFunc 함수를 연결해요.
                                                --오브젝트가 아닌 Game에도 연결할 수 있어요. 그러나 그룹과 폴더에는 연결할 수 없어요.
                                                --같은 대상에 등록된 이벤트만 호출할 수 있어요.
```
<br>
<br>
<br>
| **SendEventToClient(string PlayerName, string CustomEventName, Args ...)** |
| :--- |

해당 클라이언트에게만 이벤트를 보내는 함수에요. (이벤트 보낼 플레이어 이름, 이벤트 이름, 전달할 변수들 ...) 

<br>

샘플 

```lua
--서버 스크립트에서
local cube = Workspace.Cube
local player = Game:GetAllPlayer()[1]
wait(1)
cube:SendEventToClient(player:GetName(), "SomeFunc", 1) --특정 플레이어에게 SomeFunc() 함수를 호출해요. (첫번째 인자로 플레이어 이름이 반드시 들어가야해요.)

--클라 스크립트에서
local cube = Workspace.cube
local function SomeFunc(id) --필요하다면 함수의 인자도 넣을 수 있어요. 단, 숫자나 문자열 인자만 넣을 수 있어요.
    print("Call SomeFunc (" .. id .. ")")
end
cube:ConnectEventFunction("SomeFunc", SomeFunc) --오브젝트에 "SomeFunc"라는 이벤트 이름으로 SomeFunc 함수를 연결해요.
                                                --오브젝트가 아닌 Game에도 연결할 수 있어요. 그러나 그룹과 폴더에는 연결할 수 없어요.
                                                --같은 대상에 등록된 이벤트만 호출할 수 있어요.
```
<br>
<br>
<br>
| **SetInventorySize(int XSize, int YSize)** |
| :--- |

인벤토리의 사이즈를 설정할 수 있어요. (가로 사이즈, 세로 사이즈) 
<br>
<br>
| **SetQuickSlotCount(int Count)** |
| :--- |

퀵 슬롯의 개수를 설정할 수 있어요. (설정할 개수 값) 
<br>
<br>
| **PickUpItem(RModeServerCharacter Character, ModeItem Item)** |
| :--- |

해당 케릭터에게 아이템을 획득시켜줘요. (아이템을 획득할 캐릭터, 아이템 객체) 
<br>
<br>
| **CreateSyncObject(RScriptWorldObject WorldObject, Vector Location)** |
| :--- |

지정한 위치에 클라이언트와 동기화되는 오브젝트를 생성할 수 있어요. (생성 할 오브젝트, 생성할 위치 Vector) 

<br>

샘플 

```lua
local cube = Workspace.Cube
local createPos = Vector.new(0, 0, 0)
local temp = Game:CreateSyncObject(cube, createPos) --오브젝트를 지정된 위치에 생성해요. (모든 플레이어에게 보여요.)
print(temp:GetName()) --CreateSyncObject로 생성한 오브젝트를 변수에 담은 뒤 후처리할 수 있어요.
```
<br>
<br>
<br>
| **CreateSyncObject(RScriptWorldObject WorldObject, Vector Location, string Name, RScriptWorldObject Parent)** |
| :--- |

지정한 위치에 클라이언트와 동기화되는 오브젝트를 생성할 수 있어요. (생성 할 오브젝트, 생성할 위치 Vector, 설정할 이름, 부모가 될 오브젝트) 

<br>

샘플 

```lua
local cube = Workspace.Cube
local createPos = Vector.new(0, 0, 0)
local temp = Game:CreateSyncObject(cube, createPos, obj:GetName(), Workspace) --오브젝트를 Workspace의 자식으로 지정된 위치에 특정 이름으로 생성해요. (모든 플레이어에게 보여요.)
print(temp:GetName()) --CreateSyncObject로 생성한 오브젝트를 변수에 담은 뒤 후처리할 수 있어요.
```
<br>
<br>
<br>
| **CreateNoneSyncObject(RScriptWorldObject WorldObject, Vector Location)** |
| :--- |

지정한 위치에 클라이언트와 동기화 되지 않는 오브젝트를 생성할 수 있어요. (생성 할 오브젝트, 생성 위치 Vector) 
<br>
<br>
| **ObjectSpawner AddObjectSpawner(RObjectScript RObjectScript, EObjectSelectType ObjectSelectType, float SpawnTime, int MaxCount)** |
| :--- |

오브젝트 스포너 생성할 수 있어요. (스폰 할 오브젝트, [Enum.ObjectSelectType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/spawntype), 스폰 시간, 최대 스폰 개수) 

<br>

샘플 

```lua
local toy = Script.Parent
local spawnTime = 1
local maxSpawnCount = 999
local spawner = Game:AddObjectSpawner(toy, Enum.ObjectSelectType.Random, spawnTime, maxSpawnCount) --오브젝트를 스폰할 스포너를 등록해요.

local spawnRate = 0.9
local spawnCount = 1
local spawnPos = Vector.new(0, 0, 0)
spawner:AddSpawnObject(Toybox.Cube, spawnRate, spawnCount, spawnPos) --스포너에서 스폰할 오브젝트를 등록해요.
```
<br>
<br>
<br>
| **ObjectSelector CreateObjectSelector(EObjectSelectType SelectType)** |
| :--- |

오브젝트 셀렉터를 생성할 수 있어요. ( [Enum.ObjectSelectType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/objectselecttype)) 
<br>
<br>
| **ObjectList GetObjectList(Vector Center, float Radius)** |
| :--- |

지정한 영역의 오브젝트를 얻을 수 있어요. (영역 중앙 포인트 Vector, 영역 반지름 값) 
<br>
<br>
| **bool UseWorldItem(RModeServerCharacter Character, ModeItem Item)** |
| :--- |

월드 아이템을 사용하게 할 수 있어요. (사용할 캐릭터, 사용할 아이템) 
<br>
<br>
| **DeleteWorldItem(ModeItem Item)** |
| :--- |

월드 아이템 삭제해요. (삭제할 아이템) 
<br>
<br>
| **SaveUserGameData(String PlayerName, String KeyString, Vector SaveValue)** |
| :--- |

해당 유저의 게임 데이터를 저장할 수 있어요. (저장할 플레이어 이름, 데이터 키 값, 저장할 Vector 값) 

<br>

샘플 

```lua
local player = Game:GetAllPlayer()[1]
local playerName = player:GetPlayerName()   
local saveDataName = "PlayerSomeData"
local saveDataValue = Vector.new(0, 0, 0)
Game:SaveUserGameData(playerName, saveDataName, saveDataValue)
```
<br>
<br>
<br>
| **SaveUserGameData(String PlayerName, String KeyString, float SaveValue)** |
| :--- |

해당 유저의 게임 데이터를 저장할 수 있어요. (저장할 플레이어 이름, 데이터 키 값, 저장할 float 값) 

<br>

샘플 

```lua
local player = Game:GetAllPlayer()[1]
local playerName = player:GetPlayerName()   
local saveDataName = "PlayerSomeData"
local saveDataValue = 1.5
Game:SaveUserGameData(playerName, saveDataName, saveDataValue)
```
<br>
<br>
<br>
| **SaveUserGameData(String PlayerName, String KeyString, bool SaveValue)** |
| :--- |

해당 유저의 게임 데이터를 저장할 수 있어요. (저장할 플레이어 이름, 데이터 키 값, 저장할 Bool 값) 

<br>

샘플 

```lua
local player = Game:GetAllPlayer()[1]
local playerName = player:GetPlayerName()   
local saveDataName = "PlayerSomeData"
local saveDataValue = true
Game:SaveUserGameData(playerName, saveDataName, saveDataValue)
```
<br>
<br>
<br>
| **SaveUserGameData(String PlayerName, String KeyString, int SaveValue)** |
| :--- |

해당 유저의 게임 데이터를 저장할 수 있어요. (저장할 플레이어 이름, 데이터 키 값, 저장할 Int 값) 

<br>

샘플 

```lua
local player = Game:GetAllPlayer()[1]
local playerName = player:GetPlayerName()   
local saveDataName = "PlayerSomeData"
local saveDataValue = 1
Game:SaveUserGameData(playerName, saveDataName, saveDataValue)
```
<br>
<br>
<br>
| **SaveUserGameData(String PlayerName, String KeyString, String SaveValue)** |
| :--- |

해당 유저의 게임 데이터를 저장할 수 있어요. (저장할 플레이어 이름, 데이터 키 값, 저장할 String 값) 

<br>

샘플 

```lua
local player = Game:GetAllPlayer()[1]
local playerName = player:GetPlayerName()   
local saveDataName = "PlayerSomeData"
local saveDataValue = "Hello"
Game:SaveUserGameData(playerName, saveDataName, saveDataValue)
```
<br>
<br>
<br>
| **SaveUserGameData(String PlayerName, String KeyString, Color SaveValue)** |
| :--- |

해당 유저의 게임 데이터를 저장할 수 있어요. (저장할 플레이어 이름, 데이터 키 값, 저장할 Color 값) 

<br>

샘플 

```lua
local player = Game:GetAllPlayer()[1]
local playerName = player:GetPlayerName()   
local saveDataName = "PlayerSomeData"
local saveDataValue = Color.new(255, 0, 0, 255)
Game:SaveUserGameData(playerName, saveDataName, saveDataValue)
```
<br>
<br>
<br>
| **Object GetSavedUserGameData(String PlayerName, String KeyString)** |
| :--- |

해당 유저의 게임 데이터를 얻을 수 있어요. (플레이어 이름, 데이터 키 값) 
<br>
<br>
| **SaveGameStatisticsData(String PlayerName, String KeyString, int SaveValue, bool Overwrite, bool Ascending)** |
| :--- |

해당 유저의 게임 통계 데이터를 저장할 수 있어요. (저장할 플레이어 이름, 데이터 키 값, 저장 값, 덮어씌우기 여부, 오름차순 정렬 여부) 
<br>
<br>
| **GetGameStatisticsData(String KeyString, bool Ascending, int Offset, int Count, LuaScriptFunction CallBack)** |
| :--- |

게임 통계 데이터를 얻을 수 있어요. (데이터 키 값, 오름차순 정렬 여부, Offset 값, Count 값, CallBack 연결 함수) 
<br>
<br>
| **SendToClient_GameStatisticsData(String PlayerName, String KeyString, bool Ascending, int Offset, int Count)** |
| :--- |

게임 통계 데이터를 클라이언트로 보내줄 수 있어요 (보내줄 플레이어 이름, 데이터 키 값, 오름차순 정렬 여부, Offset 값, Count 값) 
<br>
<br>
| **vector<Player> GetAllPlayer()** |
| :--- |

모든 플레이어 얻을 수 있어요. 

<br>

샘플 

```lua
local allPlayerList = Game:GetAllPlayer() --모든 플레이어를 리스트로 반환해요.
for i = 1, #allPlayerList do
    print(allPlayerList[i]:GetName())
end
```
<br>
<br>
<br>
| **NPC CreateNPC(String NPCName, String NPCSetting, Vector Location)** |
| :--- |

NPC를 새롭게 생성할 수 있어요. (생성할 NPC 이름 설정, 지정할 [NPC세팅](https://ditoland-utplus.gitbook.io/ditoland/api-reference/server/npcsetting), 생성 위치 Vector) 
<br>
<br>
| **DeleteNPC(String NPCName)** |
| :--- |

해당 NPC를 삭제해요. (삭제할 NPC 이름) 
<br>
<br>
| **TeleportToPublicServer(LandID, PlayerNameList, LoadingUI)** |
| :--- |
<br>
<br>
| **TeleportToPrivateServer(LandID, PlayerNameList, LoadingUI)** |
| :--- |
<br>
<br>
| **TeleportToServerURL(URL, LoadingUI)** |
| :--- |
# **상속받아 사용 가능한 기능들**

<br>
## **속성**

<br>
<br>
| **Parent** |
| :--- |

부모 객체를 얻을 수 있어요. 
<br>
샘플

```lua
local parent = Workspace.Floor.Parent --오브젝트의 부모를 반환해요
print(parent:GetName()) 
```
<br>
<br>
## **이벤트**

<br>
<br>
| **OnUpdateEvent** |
| :--- |

매 프레임마다 호출되는 이벤트에요. 
<br>
샘플

```lua
local cube = Workspace.Cube
local playTime = 0
local function UpdateEvent(updateTime) --OnUpdateEvent로 연결된 함수는 updateTime 인자가 고정적으로 들어가요.
    playTime = playTime + updateTime --시간을 기록해요.
end
cube.OnUpdateEvent:Connect(UpdateEvent) --Game이나 오브젝트에 매프레임마다 호출되는 함수를 연결해요.
```
<br>
<br>
<br>
| **OnEnterPlayer** |
| :--- |

플레이어가 게임에 입장 시 호출되는 이벤트에요. 
<br>
샘플

```lua
local function EnterPlayer(player) --OnEnterPlayer로 연결된 함수는 player 인자가 고정적으로 들어가요.
    print("Enter " .. player:GetName()) 
end
Game.OnEnterPlayer:Connect(EnterPlayer) --Game에 플레이어가 게임에 입장하면 호출되는 함수를 연결해요.
```
<br>
<br>
<br>
| **OnLeavePlayer** |
| :--- |

플레이어가 게임에서 나갈 때 호출되는 이벤트에요. 
<br>
샘플

```lua
local function LeavePlayer(player) --OnLeavePlayer로 연결된 함수는 player 인자가 고정적으로 들어가요.
    print("Leave " .. player:GetName()) 
end
Game.OnLeavePlayer:Connect(LeavePlayer) --Game에 플레이어가 게임을 종료하면 호출되는 함수를 연결해요.
```
<br>
<br>
<br>
| **OnDeathCharacter** |
| :--- |

케릭터가 죽을 때 호출되는 이벤트에요. 
<br>
샘플

```lua
local function DeathCharacter(character) --OnDeathCharacter로 연결된 함수는 character 인자가 고정적으로 들어가요.
    print("Death " .. character:GetName()) 
end
Game.OnDeathCharacter:Connect(DeathCharacter) --Game에 캐릭터가 죽으면 호출되는 함수를 연결해요.
```
<br>
<br>
<br>
| **OnSpawnCharacter** |
| :--- |

케릭터가 스폰 될 때 호출되는 이벤트에요. 
<br>
샘플

```lua
local function SpawnCharacter(character) --OnSpawnCharacter로 연결된 함수는 character 인자가 고정적으로 들어가요.
    print("Spawn " .. character:GetName()) 
end
Game.OnSpawnCharacter:Connect(SpawnCharacter) --Game에 캐릭터가 생성되면 호출되는 함수를 연결해요.
```
<br>
<br>
샘플

```lua
local function EnterPlayer(Player)
	local Character = Player:GetCharacter()
	local PlayerName = Character:GetPlayerName()
	print(PlayerName.." Join Game !")
end
--게임에 플레이어가 들어올 시 EnterPlayer함수에 연결
Game.OnEnterPlayer:Connect(EnterPlayer)
```
<br>
<br>
<br>
| **ConnectChangeEventFunction(string ValueName, function FunctionName)** |
| :--- |

추가된 값이 변경 될 때 호출되는 이벤트에요. (Value 이름, 연결 함수) 
<br>
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
<br>
<br>
<br>
| **AddTimeEvent(String EventName, float Time, LuaScriptFunction EventFuunction)** |
| :--- |

일정 시간뒤에 연결 함수가 호출되는 이벤트를 추가해요. (추가할 이벤트 이름, 시간, 연결 함수) 
<br>
샘플

```lua
local waitTime = 2
local function PrintMessage() --AddTimeEvent로 등록된 함수는 일정시간을 기다린뒤, 호출돼요.
    print("Call PrintMessage!") 
end
Game:AddTimeEvent("PrintMessage", waitTime, PrintMessage) --일정시간을 기다린뒤 호출되는 함수를 문자열로 등록해요.
```
<br>
<br>
<br>
| **DeleteTimeEvent(String EventName)** |
| :--- |

등록된 시간 이벤트를 삭제해요. (삭제할 이벤트 이름) 
<br>
샘플

```lua
local waitTime = 2
local function PrintMessage() --AddTimeEvent로 등록된 함수는 일정시간을 기다린뒤, 호출돼요.
    print("Call PrintMessage!") 
end
Game:AddTimeEvent("PrintMessage", waitTime, PrintMessage) --일정시간을 기다린뒤 호출되는 함수를 문자열로 등록해요.
Game:DeleteTimeEvent("PrintMessage") --AddTimeEvent로 등록한 함수를 삭제해서 호출되지 않게 해요.
```
<br>
<br>
## **함수**

<br>
<br>
| **RModePhase AddPhase(string phasename)** |
| :--- |

게임에 단계를 추가할 수 있어요. (추가할 단계 이름) 
<br>
샘플

```lua
--서버 스크립트에서-------------
local LobbyState = Game:AddPhase("Lobby") --사용할 Phase를 등록해요.
local PlayState = Game:AddPhase("Play") --Phase는 여러개도 등록할 수 있어요.
local ResultState = Game:AddPhase("Result")
Game:AddReplicateValue("GameState", "Lobby", Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.

--각 Phase로 전환되었을때 처리할 이벤트 함수를 추가해요.
local function EnterLobbyState()
    Game.GameState = "Lobby" 
    print("Enter Lobby State")
end
LobbyState.EnterEvent:Connect(EnterLobbyState) --해당 Phase로 변경됐을때 호출되는 이벤트를 연결해요.

local function UpdateLobbyState(UpdateTime)                    
    print("Update Lobby State")
end
LobbyState.UpdateEvent:Connect(UpdateLobbyState)  --해당 Phase일때 매프레임마다 호출되는 이벤트를 연결해요.

local function ExitLobbyState()
    print("End Lobby State")
end
LobbyState.ExitEvent:Connect(ExitLobbyState) --해당 Phase가 끝날때 호출되는 이벤트를 연결해요.

local function EnterPlayState()
    Game.GameState = "Play" 
    print("Enter Play State")
end
PlayState.EnterEvent:Connect(EnterPlayState)

local function EnterResultState()
    Game.GameState = "Result" 
    print("Enter Result State")
end
ResultState.EnterEvent:Connect(EnterResultState)

wait(1)
Game:ChangePhaseByName("Game") --이름으로 Phase를 전환해요.
wait(1)
Game:ChangeToNextPhase() --다음 Phase로 전환해요. (만약 마지막 Phase면 처리되지 않아요.)
     
--클라 스크립트에서-------------
local LobbyState = Game:AddPhase("Lobby") --서버 스크립트에서 추가한 Phase를 똑같이 등록해요.
local PlayState = Game:AddPhase("Play") 
local ResultState = Game:AddPhase("Result")

--각 Phase로 전환되었을때 처리할 이벤트 함수를 추가해요.
--서버 스크립트와 동일하게 작성하되, Game.GameState = "Lobby" 같은 Phase 변경은 제외해요. (서버에서만 처리해야 해요.)
local function EnterLobbyState()     
    print("Enter Lobby State")
end
LobbyState.EnterEvent:Connect(EnterLobbyState)

local function EnterPlayState()
    print("Enter Play State")
end
PlayState.EnterEvent:Connect(EnterPlayState)

local function EnterResultState()
    print("Enter Result State")
end
ResultState.EnterEvent:Connect(EnterResultState)

--스크립트 제일 아래에 상태가 바뀔때마다 관련된 Phase 함수가 호출될 수 있도록 연결해요.
Game:ConnectChangeEventFunction("GameState", function() 
    Game:ChangePhaseByName(Game.GameState) 
end)
```
<br>
<br>
<br>
| **RModePhase GetPhaseByName(string phasename)** |
| :--- |

단계 이름으로 단계를 불러올 수 있어요. (불러올 단계 이름) 
<br>
<br>
| **RModePhase GetCurPhase()** |
| :--- |

현재 단계를 얻을 수 있어요. 
<br>
<br>
| **RModePhase ChangePhaseByName(string changephasename)** |
| :--- |

단계 이름을 통해 해당 단계로 변경할 수 있어요. (변경할 단계 이름) 
<br>
<br>
| **RModePhase ChangeToNextPhase()** |
| :--- |

다음 단계로 변경할 수 있어요. 
<br>
<br>
| **ConnectEventFunction(string customevent, LuaScriptFunction function) ** |
| :--- |

유저가 추가한 이벤트에 함수를 연결할 수 있어요. (이벤트 이름, 연결 함수) 
<br>
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
<br>
<br>
<br>
| **float GetPassTime()** |
| :--- |

단계가 진행된 시간을 얻을 수 있어요. 
<br>
<br>
| **DeleteObject(RScriptWorldObject)** |
| :--- |

오브젝트를 삭제할 수 있어요. (삭제할 오브젝트) 

서버에서 사용하면 서버와 클라 오브젝트 모두 삭제되고 클라에서 사용하면 클라 오브젝트만 삭제해요 
<br>
샘플

```lua
local cube = Workspace.Cube
Game:DeleteObject(cube) --오브젝트를 파괴해요.
```
<br>
<br>
<br>
| **List<HitResult> LineTraceList(Vector Start, Vector Dir, float Distance)** |
| :--- |

설정된 시작 지점에서 원하는 방향으로 지정된 거리 만큼의 충돌 리스트들을 가져올 수 있어요. (시작 지점 Vector, 목표 지점 Vector, 거리 값) 
<br>
<br>
| **List<HitResult> LineTraceList(Vector Start, Vector Dir, float Distance, string UserCollisionName)** |
| :--- |

설정된 시작 지점에서 원하는 방향으로 지정된 거리 만큼의 유저가 추가한 충돌 타입과의 충돌 리스트들을 가져올 수 있어요. (시작 지점 Vector, 목표 지점 Vector, 거리 값) 
<br>
샘플

```lua
local startPos = Workspace.Cube:GetTransform():GetLocation()
local dir = Vector.new(1, 0, 0)
local distance = 1000
local targetList = Game:LineTraceList(startPos, dir, distance) --시작 위치에서 특정 방향으로 거리만큼의 충돌 리스트가 반환돼요.
for i = 1, #targetList do 
    print(targetList[i].HitObject:GetName()) --충돌한 오브젝트에요.
    print(targetList[i].HitLocation) --충돌한 오브젝트의 위치에요.
end
```
<br>
<br>
<br>
| **string GetName()** |
| :--- |

객체의 이름을 얻을 수 있어요. 
<br>
샘플

```lua
print(Workspace.Floor:GetName()) --오브젝트의 이름을 문자열로 반환해요.
```
<br>
<br>
<br>
| **RModeObject GetParent(string ParentName)** |
| :--- |

이름으로 부모 객체를 얻을 수 있어요. (찾고싶은 부모 객체 이름) 
<br>
<br>
| **RModeObject GetChild(string ChildName)** |
| :--- |

이름으로 자식 객체를 얻을 수 있어요. (찾고싶은 자식 객체 이름) 
<br>
<br>
| **RModeObject GetGetSibling(string Name)** |
| :--- |

이름으로 형제 객체를 얻을 수 있어요. (찾고싶은 형제 객체 이름) 
<br>
<br>
| **List<RScriptObject> GetChildList()** |
| :--- |

자식 객체의 리스트를 얻을 수 있어요. 
<br>
샘플

```lua
local uiList = Workspace.HUD:GetChildList() --오브젝트의 자식 오브젝트를 리스트로 반환해요.
for i = 1, #uiList do --리스트앞에 #을 붙여 리스트의 길이를 가져올 수 있어요.
    print(uiList[i]:GetName())
end
```
<br>
<br>
<br>
| **bool IsCharacter()** |
| :--- |

캐릭터인지 확인할 수 있어요. 
<br>
샘플

```lua
local cube = Workspace.Cube
if cube:IsCharacter() == true then --오브젝트가 Character면 true를 반환해요.
    print(cube:GetName() .. " Is Character")
end
```
<br>
<br>
<br>
| **bool IsStaticMesh()** |
| :--- |

스테틱 메시인지 확인할 수 있어요. 
<br>
샘플

```lua
local cube = Workspace.Cube
if cube:IsStaticMesh() == true then --오브젝트가 StaticMesh면 true를 반환해요.
    print(cube:GetName() .. " Is StaticMesh")
end
```
<br>
<br>
<br>
| **bool IsFX()** |
| :--- |

FX인지 확인할 수 있어요. 
<br>
샘플

```lua
local cube = Workspace.Cube
if cube:IsFX() == true then --오브젝트가 FX면 true를 반환해요.
    print(cube:GetName() .. " Is FX")
end
```
<br>
<br>
<br>
| **bool IsSound()** |
| :--- |

Sound인지 확인할 수 있어요. 
<br>
샘플

```lua
local cube = Workspace.Cube
if cube:IsSound() == true then --오브젝트가 Sound면 true를 반환해요.
    print(cube:GetName() .. " Is Sound")
end
```
<br>
<br>
<br>
| **bool IsPointLight()** |
| :--- |

포인트 라이트인지 확인할 수 있어요. 
<br>
샘플

```lua
local cube = Workspace.Cube
if cube:IsPointLight() == true then --오브젝트가 PointLight면 true를 반환해요.
    print(cube:GetName() .. " Is PointLight")
end
```
<br>
<br>
<br>
| **bool IsSpotLight()** |
| :--- |

스포트 라이트인지 확인할 수 있어요. 
<br>
샘플

```lua
local cube = Workspace.Cube
if cube:IsSpotLight() == true then --오브젝트가 SpotLight면 true를 반환해요.
    print(cube:GetName() .. " Is SpotLight")
end
```
<br>
<br>
<br>
| **bool IsSurfaceUI()** |
| :--- |

서피스 UI인지 확인할 수 있어요. 
<br>
샘플

```lua
local cube = Workspace.Cube
if cube:IsSurfaceUI() == true then --오브젝트가 SurfaceUI면 true를 반환해요.
    print(cube:GetName() .. " Is SurfaceUI")
end
```
<br>
<br>
<br>
| **bool IsScreenUI()** |
| :--- |

스크린 UI인지 확인할 수 있어요. 
<br>
샘플

```lua
local cube = Workspace.Cube
if cube:IsScreenUI() == true then --오브젝트가 ScreenUI면 true를 반환해요.
    print(cube:GetName() .. " Is ScreenUI")
end
```
<br>
<br>
<br>
| **bool IsItem()** |
| :--- |

아이템인지 확인할 수 있어요. 
<br>
샘플

```lua
local cube = Workspace.Cube
if cube:IsItem() == true then --오브젝트가 Item면 true를 반환해요.
    print(cube:GetName() .. " Is Item")
end
```
<br>
<br>
<br>
| **bool IsNPC()** |
| :--- |

NPC인지 확인할 수 있어요. 
<br>
샘플

```lua
local cube = Workspace.Cube
if cube:IsNPC() == true then --오브젝트가 NPC면 true를 반환해요.
    print(cube:GetName() .. " Is NPC")
end
```
<br>
<br>
<br>
| **bool IsFolder()** |
| :--- |

폴더인지 확인할 수 있어요. 
<br>
샘플

```lua
local cube = Workspace.Cube
if cube:IsFolder() == true then --오브젝트가 Folder면 true를 반환해요.
    print(cube:GetName() .. " Is Folder")
end
```
<br>
<br>
<br>
| **bool IsScript()** |
| :--- |

스트립트인지 확인할 수 있어요. 
<br>
샘플

```lua
local cube = Workspace.Cube
if cube:IsScript() == true then --오브젝트가 Script면 true를 반환해요.
    print(cube:GetName() .. " Is Script")
end
```
<br>
<br>
<br>
| **bool IsCollider()** |
| :--- |

Collider인지 확인할 수 있어요. 
<br>
샘플

```lua
local cube = Workspace.Cube
if cube:IsCollider() == true then --오브젝트가 Collider면 true를 반환해요.
    print(cube:GetName() .. " Is Collider")
end
```
<br>
<br>
<br>
| **bool IsWidget()** |
| :--- |

Widget인지 확인할 수 있어요. 
<br>
샘플

```lua
local cube = Workspace.Cube
if cube:IsWidget() == true then --오브젝트가 Widget면 true를 반환해요.
    print(cube:GetName() .. " Is Widget")
end
```
<br>
<br>
<br>
| **bool IsCamera()** |
| :--- |

Camera인지 확인할 수 있어요. 
<br>
샘플

```lua
local cube = Workspace.Cube
if cube:IsCamera() == true then --오브젝트가 Camera면 true를 반환해요.
    print(cube:GetName() .. " Is Camera")
end
```
<br>
<br>
<br>
| **bool IsValid()** |
| :--- |

해당 오브젝트가 유효한지 확인 할 수있어요. 
<br>
<br>
| **AddReplicateValue(string ValueName, Vector Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 벡터를 추가해요. (추가할 Value 이름, Vector 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
<br>
샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeVector", Vector.new(0, 50, 0), Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeVector)

--클라 스크립트에서-------------
print(Game.SomeVector) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
<br>
<br>
<br>
| **AddReplicateValue(string ValueName, float Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 실수를 추가해요. (추가할 Value 이름, float 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
<br>
샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeNumber", 1, Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeNumber .. " in Server")

--클라 스크립트에서-------------
print(Game.SomeNumber .. " in Client") --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
<br>
<br>
<br>
| **AddReplicateValue(string ValueName, bool Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 bool를 추가해요. (추가할 Value 이름, bool 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
<br>
샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeBool", true, Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeBool)

--클라 스크립트에서-------------
print(Game.SomeBool) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
<br>
<br>
<br>
| **AddReplicateValue(string ValueName, string Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 문자열을 추가해요. (추가할 Value 이름, string 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
<br>
샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeString", "Hello World!", Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeString)

--클라 스크립트에서-------------
print(Game.SomeString) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
<br>
<br>
<br>
| **AddReplicateValue(string ValueName, Color Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 컬러를 추가해요. (추가할 Value 이름, Color 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
<br>
샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeColor", Color.new(255, 0, 0, 255), Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeColor)

--클라 스크립트에서-------------
print(Game.SomeColor) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
<br>
<br>
<br>
| **AddSaveValue(string ValueName, Vector Data)** |
| :--- |

해당 객체 저장소에 벡터를 추가해요. (Value 이름, Vector 데이터) 
<br>
<br>
| **AddSaveValue(string ValueName, float Data)** |
| :--- |

해당 객체 저장소에 실수를 추가해요. (Value 이름, float 데이터) 
<br>
<br>
| **AddSaveValue(string ValueName, bool Data)** |
| :--- |

해당 객체 저장소에 bool을 추가해요. (Value 이름, bool 데이터) 
<br>
<br>
| **AddSaveValue(string ValueName, string Data)** |
| :--- |

해당 객체 저장소에 문자열을 추가해요. (Value 이름, string 데이터) 
<br>
<br>
| **AddSaveValue(string ValueName, Color Data)** |
| :--- |

해당 객체 저장소에 칼라를 추가해요. (Value 이름, Color 데이터) 
