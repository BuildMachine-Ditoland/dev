
게임 전반적인 역할을 하는 객체에요. 여기 있는 기능들은 클라이언트에서만 사용할 수 있어요. 
## **이벤트**

| **ReceiveGameStatisticsDataEvent** |
| :--- |

서버로 부터 게임 통계 데이터 받았을 때 발생하는 이벤트에요. 
## **함수**

| **RModeRemotePlayer GetRemotePlayer(string PlayerName);** |
| :--- |

이름으로 플레이어를 얻을 수 있어요. (찾고싶은 플레이어 이름) 
| **RGameClientCharacter GetRemotePlayerCharacter(string PlayerName)** |
| :--- |

플레이어 이름으로 해당 플레이어의 캐릭터를 얻을 수 있어요. (캐릭터를 찾고싶은 플레이어 이름) 
| **int GetPlayerCount** |
| :--- |

현재 게임에 참여하고 있는 플레이어의 수를 얻을 수 있어요. 
| **SendEventToServer(string EventName, Args ... )** |
| :--- |

서버에 커스텀 이벤트를 보내는 함수에요. (이벤트 이름, 전달하고 싶은 변수들 ...) 
| **RModeSequenceAnimStateSetting AddAnimStateMachineSetting(string StateMachineName)** |
| :--- |

캐릭터에 사용될 애니메이션 상태머신 설정을 추가할 수 있어요. (설정할 상태머신 이름) 
| **RModeSequenceAnimStateSetting GetAnimStateMachineSetting(string StateMachineName)** |
| :--- |

설정된 애니메이션 상태머신을 얻을 수 있어요. (얻고 싶은 상태머신 이름) 
| **SetCharacterAnimStateMachine(string CharacterSettingName, string AnimStateMachineSettingName)** |
| :--- |

해당 캐릭터의 애니메이션 상태 머신을 사용하게 할 수 있어요. (설정한 캐릭터세팅 이름, 애니메이션 상태 머신 이름) 
| **SetNPCAnimStateMachine(string NPCSettingName, string AnimStateMachineSettingName)** |
| :--- |

해당 NPC의 애니메이션 상태 머신 사용하게 할 수 있어요. (설정한 NPC 이름, 애니메이션 상태 머신 이름) 
| **ChangeCameraOffsetDelta(Vector Offset, float Time)** |
| :--- |

카메라를 주어진 시간 동안 해당 값만큼 이동 시킬 수 있어요. (이동 시킬 Vector 값, 이동 시간) 
| **ChangeCameraOffsetAbs(Vector Offset, float Time)** |
| :--- |

카메라를 주어진 시간 동안 해당 값으로 이동시켜요. (이동 할 Vector 값, 이동 시간) 
| **RestoreCameraOffset(float Time)** |
| :--- |

카메라를 초기 Offset으로 주어진 시간 동안 이동 시켜요. (이동 시간) 
| **ObjectFXClient CreateFX(ObjectFXClient FXObject, Vetor Location)** |
| :--- |

FX를 생성할 수 있어요. (생성 할 FX 오브젝트, 생성할 위치) 
| **ObjectFXClient CreateFX(String FXName, Vetor Location)** |
| :--- |

FX를 생성할 수 있어요. (생성 할 FX 이름, 생성할 위치) 
| **DeleteFX(ObjectFXClient Object)** |
| :--- |

FX를 제거시켜요. (제거할 FX 오브젝트) 
| **ObjectSoundClient PlaySound(ObjectSoundClient SoundObject, Vetor Location)** |
| :--- |

사운드를 플레이해요. (플레이 할 Sound 오브젝트, 플레이 할 위치 Vector) 
| **ObjectSoundClient PlaySound(String SoundObjectName)** |
| :--- |

사운드를 플레이해요. (플레이 할 Sound 이름) 
| **ObjectSoundClient PlaySound(String SoundObjectName, Vector Location)** |
| :--- |

사운드를 플레이해요. (플레이 할 Sound 이름, 플레이 할 위치 Vector) 
| **StopSound(String SoundName)** |
| :--- |

플레이 중인 사운드를 정지시켜요. (정지할 Sound 이름) 
| **CreateObject(string ObjectName, Vector Location)** |
| :--- |

지정된 위치에 오브젝트를 생성 시켜요. (생성 할 Object 이름, 생성 할 위치 Vector) 
| **CreateObject(RScriptWorldObject Object, Vector Location)** |
| :--- |

지정된 위치에 오브젝트를 생성 시켜요. (생성 할 Object, 생성 할 위치 Vector) 
| **CreateUIScene(RScriptUISceneClient Source)** |
| :--- |

Source와 같은 UIScene을 생성한다. 
| **CreateUIScene(string UISceneName, RScriptUISceneClient Source)** |
| :--- |

Source와 같은 UIScene을 생성 후, UISceneName을 생성된 오브젝트 이름으로 설정한다. (생성할 오브젝트의 이름 UISceneName, 생성 할 오브젝트 Source) 
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
