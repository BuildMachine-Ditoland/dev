
게임 전반적인 역할을 하는 객체에요. 여기 있는 기능들은 서버에서만 사용할 수 있어요. 
## **속성**

| **MaxUserCount** |
| :--- |

게임 최대 인원을 설정할 수 있어요. 디폴트 값은 10 이에요. 
## **함수**

| **AddUserCollisionType(string UserCollisionType)** |
| :--- |

유저 충돌 타입 설정을 추가할 수 있어요. (충돌 타입 이름 설정) 

특정 오브젝트의 충돌 처리를 다른 오브젝트와 다르게 할 때 사용 

예) 특정 오브젝트만 통과하고, 캐릭터는 못 통과하는 오브젝트. 
| **RSpawnPointGroup AddSpawnPointGroup(string SpawnPointGroupName)** |
| :--- |

게임에서 사용 할 스폰 포인트 그룹을 추가할 수 있어요. (추가할 스폰 포인트 그룹 이름) 
| **RSpawnPoint AddSpawnPoint(RScriptWorldObject* RWorldObject)** |
| :--- |

게임에서 사용 할 스폰 포인트를 추가할 수 있어요. (스폰 포인트로 지정 할 오브젝트) 
| **RSpawnPoint AddSpawnPointAtGroup(string SpawnPointGroupName, RScriptWorldObject* RWorldObject)** |
| :--- |

스폰포인트 그룹에 스폰 포인트를 추가할 수 있어요. (스폰포인트를 추가할 그룹 이름, 이름, 스폰 포인트를 할 오브젝트) 
| **SetSpawnType(ModeSpawnType InSpawnType)** |
| :--- |

게임의 스폰 타입을 설정할 수 있어요. ( [Enum.SpawnType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/spawntype)) 
| **SetUsingSpawnPointGroup(RSpawnPointGroup* SpawnPointGroup)** |
| :--- |

게임에 적용 할 스폰 그룹을 설정할 수 있어요. (게임에 적용 할 스폰포인트 그룹 오브젝트) 
| **SetUsingSpawnPoint(RSpawnPoint* SpawnPoint)** |
| :--- |

게임에 적용 할 스폰 포인트를 설정할 수 있어요. (게임에 적용 할 스폰포인트 오브젝트) 
| **SetDefaultSpawnPos(FVector Pos)** |
| :--- |

설정된 스폰 포인트가 없을 경우 지정한 위치에 스폰되도록 해요. (스폰할 위치 Vector) 
| **RModeCharacterSetting AddCharacterSetting(string SettingName)** |
| :--- |

게임에서 사용 할 캐릭터 설정을 추가할 수 있어요. (추가할 이름 설정) 
| **Team AddTeam(string TeamName)** |
| :--- |

게임에서 사용 할 팀 설정을 추가할 수 있어요. (팀 이름 설정) 
| **RModeNPCSetting AddNPCSetting(string NPCSettingName)** |
| :--- |

게임에서 사용 할 NPC 설정을 추가할 수 있어요. (NPC 이름 설정) 
| **Player GetPlayer(string PlayerName)** |
| :--- |

플레이어 이름으로 플레이어를 얻을 수 있어요. (얻고 싶은 플레이어 이름) 
| **RModeServerCharacter GetPlayerCharacter(string PlayerName)** |
| :--- |

플레이어 이름으로 플레이어 캐릭터를 얻을 수 있어요. (얻고 싶은 플레이어 이름) 
| **SetTeamSetting(EModeTeamType TeamType, EDivideTeamType DivideTeamType)** |
| :--- |

게임의 팀전 여부, 팀 나누기 방식을 설정할 수 있어요. (팀 타입, [Enum.DivideTeamType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/divideteamtype)) 
| **int GetPlayerCount()** |
| :--- |

현재 게임에 참여하고 있는 플레이어 수를 얻을 수 있어요. 
| **ResetTeamSetting()** |
| :--- |

게임의 팀 설정을 모두 제거해요. 
| **ApplyTeamSetting()** |
| :--- |

팀 설정 방식을 게임에 적용하는 함수에요. 
| **ReqResetGame()** |
| :--- |

게임 리셋을 요청하는 함수에요. 
| **SetCanEnterUser()** |
| :--- |

게임에 유저의 진입 가능 여부를 설정해요. (false로 설정 할 경우 해당 게임으로 더 이상 유저가 들어올 수 없어요.) 
| **BroadcastEvent(string CustomEventName, Args ...)** |
| :--- |

모든 클라이언트에게 이벤트를 보내는 함수에요. (이벤트 이름, 전달할 변수들 ...) 
| **SendEventToClient(string PlayerName, string CustomEventName, Args ...)** |
| :--- |

해당 클라이언트에게만 이벤트를 보내는 함수에요. (이벤트 보낼 플레이어 이름, 이벤트 이름, 전달할 변수들 ...) 
| **SetInventorySize(int XSize, int YSize)** |
| :--- |

인벤토리의 사이즈를 설정할 수 있어요. (가로 사이즈, 세로 사이즈) 
| **SetQuickSlotCount(int Count)** |
| :--- |

퀵 슬롯의 개수를 설정할 수 있어요. (설정할 개수 값) 
| **PickUpItem(RModeServerCharacter Character, ModeItem Item)** |
| :--- |

해당 케릭터에게 아이템을 획득시켜줘요. (아이템을 획득할 캐릭터, 아이템 객체) 
| **CreateSyncObject(string ObjectName, Vector Location)** |
| :--- |

지정한 위치에 클라이언트와 동기화되는 오브젝트를 생성할 수 있어요. (생성 할 오브젝트 이름, 생성할 위치 Vector) 
| **CreateSyncObject(RScriptWorldObject WorldObject, Vector Location)** |
| :--- |

지정한 위치에 클라이언트와 동기화되는 오브젝트를 생성할 수 있어요. (생성 할 오브젝트, 생성할 위치 Vector) 
| **CreateNoneSyncObject(string ObjectName, Vector Location)** |
| :--- |

지정한 위치에 클라이언트와 동기화 되지 않는 오브젝트를 생성할 수 있어요. (생성 할 오브젝트 이름, 생성 위치 Vector) 
| **CreateNoneSyncObject(RScriptWorldObject WorldObject, Vector Location)** |
| :--- |

지정한 위치에 클라이언트와 동기화 되지 않는 오브젝트를 생성할 수 있어요. (생성 할 오브젝트, 생성 위치 Vector) 
| **ObjectSpawner AddObjectSpawner(RObjectScript RObjectScript, EObjectSelectType SpawnType, float SpawnTime, int MaxCount)** |
| :--- |

오브젝트 스포너 생성할 수 있어요. (스폰 할 오브젝트, [Enum.SpawnType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/spawntype), 스폰 시간, 최대 스폰 개수) 
| **ObjectSelector CreateObjectSelector(EObjectSelectType SelectType)** |
| :--- |

오브젝트 셀렉터를 생성할 수 있어요. ( [Enum.ObjectSelectType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/objectselecttype)) 
| **ObjectList GetObjectList(Vector Center, float Radius)** |
| :--- |

지정한 영역의 오브젝트를 얻을 수 있어요. (영역 중앙 포인트 Vector, 영역 반지름 값) 
| **UseWorldItem(RModeServerCharacter Character, ModeItem Item)** |
| :--- |

월드 아이템을 사용하게 할 수 있어요. (사용할 캐릭터, 사용할 아이템) 
| **DeleteWorldItem(ModeItem Item)** |
| :--- |

월드 아이템 삭제해요. (삭제할 아이템) 
| **SaveUserGameData(String PlayerName, String KeyString, Vector SaveValue)** |
| :--- |

해당 유저의 게임 데이터를 저장할 수 있어요. (저장할 플레이어 이름, 데이터 키 값, 저장할 Vector 값) 
| **SaveUserGameData(String PlayerName, String KeyString, float SaveValue)** |
| :--- |

해당 유저의 게임 데이터를 저장할 수 있어요. (저장할 플레이어 이름, 데이터 키 값, 저장할 float 값) 
| **SaveUserGameData(String PlayerName, String KeyString, bool SaveValue)** |
| :--- |

해당 유저의 게임 데이터를 저장할 수 있어요. (저장할 플레이어 이름, 데이터 키 값, 저장할 Bool 값) 
| **SaveUserGameData(String PlayerName, String KeyString, int SaveValue)** |
| :--- |

해당 유저의 게임 데이터를 저장할 수 있어요. (저장할 플레이어 이름, 데이터 키 값, 저장할 Int 값) 
| **SaveUserGameData(String PlayerName, String KeyString, String SaveValue)** |
| :--- |

해당 유저의 게임 데이터를 저장할 수 있어요. (저장할 플레이어 이름, 데이터 키 값, 저장할 String 값) 
| **SaveUserGameData(String PlayerName, String KeyString, Color SaveValue)** |
| :--- |

해당 유저의 게임 데이터를 저장할 수 있어요. (저장할 플레이어 이름, 데이터 키 값, 저장할 Color 값) 
| **Object GetSavedUserGameData(String PlayerName, String KeyString)** |
| :--- |

해당 유저의 게임 데이터를 얻을 수 있어요. (플레이어 이름, 데이터 키 값) 
| **SaveGameStatisticsData(String PlayerName, String KeyString, int SaveValue, bool Overwrite, bool Ascending)** |
| :--- |

해당 유저의 게임 통계 데이터를 저장할 수 있어요. (저장할 플레이어 이름, 데이터 키 값, 저장 값, 덮어씌우기 여부, 오름차순 정렬 여부) 
| **GetGameStatisticsData(String KeyString, bool Ascending, int Offset, int Count, LuaScriptFunction CallBack)** |
| :--- |

게임 통계 데이터를 얻을 수 있어요. (데이터 키 값, 오름차순 정렬 여부, Offset 값, Count 값, CallBack 연결 함수) 
| **SendToClient_GameStatisticsData(String PlayerName, String KeyString, bool Ascending, int Offset, int Count)** |
| :--- |

게임 통계 데이터를 클라이언트로 보내줄 수 있어요 (보내줄 플레이어 이름, 데이터 키 값, 오름차순 정렬 여부, Offset 값, Count 값) 
| **vector<Player> GetAllPlayer()** |
| :--- |

모든 플레이어 얻을 수 있어요. 
| **NPC CreateNPC(String NPCName, String NPCSetting, Vector Location)** |
| :--- |

NPC를 새롭게 생성할 수 있어요. (생성할 NPC 이름 설정, 지정할 [NPC세팅](https://ditoland-utplus.gitbook.io/ditoland/api-reference/server/npcsetting), 생성 위치 Vector) 
| **DeleteNPC(String NPCName)** |
| :--- |

해당 NPC를 삭제해요. (삭제할 NPC 이름) 
# **상속받아 사용 가능한 기능들**

## **속성**

| **Parent** |
| :--- |

부모 객체를 얻을 수 있어요. 
## **이벤트**

| **OnUpdateEvent** |
| :--- |

매 프레임마다 호출되는 이벤트에요. 
| **OnEnterPlayer** |
| :--- |

플레이어가 게임에 입장 시 호출되는 이벤트에요. 
| **OnLeavePlayer** |
| :--- |

플레이어가 게임에서 나갈 때 호출되는 이벤트에요. 
| **OnDeathCharacter** |
| :--- |

케릭터가 죽을 때 호출되는 이벤트에요. 
| **OnSpawnCharacter** |
| :--- |

케릭터가 스폰 될 때 호출되는 이벤트에요. 

샘플 

```lua

local function EnterPlayer(Player) 

local Character = Player:GetCharacter() 

local PlayerName = Character:GetPlayerName() 

Logger:Log(PlayerName.." Join Game !") 

end 

--게임에 플레이어가 들어올 시 EnterPlayer함수에 연결 

Game.OnEnterPlayer:Connect(EnterPlayer) 

``` 
| **ConnectChangeEventFunction(string ValueName, function FunctionName)** |
| :--- |

추가된 값이 변경 될 때 호출되는 이벤트에요. (Value 이름, 연결 함수) 

샘플 

```lua

local function ChangeCurBullet(value) 

Logger:Log(“Hello”) 

end 

 

-- Object의 "CurBullet" 라는 Value가 변경되면 ChangeCurBullet 함수에 연결 

Object:ConnectChangeEventFunction("CurBullet", LuaScriptFunction ChangeCurBullet)   

``` 
| **AddTimeEvent(String EventName, float Time, LuaScriptFunction EventFuunction)** |
| :--- |

일정 시간뒤에 연결 함수가 호출되는 이벤트를 추가해요. (추가할 이벤트 이름, 시간, 연결 함수) 
| **DeleteTimeEvent(String EventName)** |
| :--- |

등록된 시간 이벤트를 삭제해요. (삭제할 이벤트 이름) 
## **함수**

| **RModePhase AddPhase(string phasename)** |
| :--- |

게임에 단계를 추가할 수 있어요. (추가할 단계 이름) 
| **RModePhase GetPhaseByName(string phasename)** |
| :--- |

단계 이름으로 단계를 불러올 수 있어요. (불러올 단계 이름) 
| **RModePhase GetCurPhase()** |
| :--- |

현재 단계를 얻을 수 있어요. 
| **RModePhase ChangePhaseByName(string changephasename)** |
| :--- |

단계 이름을 통해 해당 단계로 변경할 수 있어요. (변경할 단계 이름) 
| **RModePhase ChangeToNextPhase()** |
| :--- |

다음 단계로 변경할 수 있어요. 
| **ConnectEventFunction(string customevent, LuaScriptFunction function) ** |
| :--- |

유저가 추가한 이벤트에 함수를 연결할 수 있어요. (이벤트 이름, 연결 함수) 
| **float GetPassTime()** |
| :--- |

단계가 진행된 시간을 얻을 수 있어요. 
| **DeleteObject(RScriptWorldObject)** |
| :--- |

오브젝트를 삭제할 수 있어요. (삭제할 오브젝트) 
| **string GetName()** |
| :--- |

객체의 이름을 얻을 수 있어요. 
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
| **bool IsCharacter()** |
| :--- |

캐릭터인지 확인할 수 있어요. 
| **bool IsStaticMesh()** |
| :--- |

스테틱 메시인지 확인할 수 있어요. 
| **bool IsFX()** |
| :--- |

FX인지 확인할 수 있어요. 
| **bool IsSound()** |
| :--- |

Sound인지 확인할 수 있어요. 
| **bool IsPointLight()** |
| :--- |

포인트 라이트인지 확인할 수 있어요. 
| **bool IsSurfaceUI()** |
| :--- |

서피스 UI인지 확인할 수 있어요. 
| **bool IsScreenUI()** |
| :--- |

스크린 UI인지 확인할 수 있어요. 
| **bool IsItem()** |
| :--- |

아이템인지 확인할 수 있어요. 
| **bool IsNPC()** |
| :--- |

NPC인지 확인할 수 있어요. 
| **bool IsFolder()** |
| :--- |

폴더인지 확인할 수 있어요. 
| **bool IsScript()** |
| :--- |

스트립트인지 확인할 수 있어요. 
| **bool IsCollider()** |
| :--- |

Collider인지 확인할 수 있어요. 
| **bool IsWidget()** |
| :--- |

Widget인지 확인할 수 있어요. 
| **bool IsCamera()** |
| :--- |

Widget인지 확인할 수 있어요. 
| **bool IsValid()** |
| :--- |

해당 오브젝트가 유효한지 확인 할 수있어요. 
| **AddReplicateValue(string ValueName, Vector Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 벡터를 추가해요. (추가할 Value 이름, Vector 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, float Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 실수를 추가해요. (추가할 Value 이름, float 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, bool Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 bool를 추가해요. (추가할 Value 이름, bool 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, string Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 문자열을 추가해요. (추가할 Value 이름, string 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, Color Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 컬러를 추가해요. (추가할 Value 이름, Color 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
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
