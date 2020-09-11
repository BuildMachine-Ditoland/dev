
클라이언트에서 사용되는 캐릭터에 대한 개체에요. 
## **함수**

| **Player GetPlayer()** |
| :--- |

해당 캐릭터의 플레이어를 얻을 수 있어요. 
| **string GetPlayerName()** |
| :--- |

플레이어의 이름을 얻을 수 있어요. 
| **FRModeAnimStateMachine AddAnimStateMachine(string StateMachineName)** |
| :--- |

Game:AddAnimStateMachineSetting로 추가된 상태 머신 중 애니메이션 상태 머신을 추가해요. (추가할 상태 머신 이름) 
| **FRModeAnimStateMachine GetAnimStateMachine(string StateMachineName)** |
| :--- |

해당 애니메이션 상태 머신을 얻을 수 있어요. (얻고싶은 상태 머신 이름) 
| **RModeAnimStateBase GetCurAnimState()** |
| :--- |

현재 애니메이션의 상태를 얻을 수 있어요. 
| **ChangeAnimState(string AnimState)** |
| :--- |

해당하는 애니메이션의 상태로 변경할 수 있어요. (변경하고 싶은 애니메이션 상태 이름) 
| **ChangeAnimStateMachine(string ChangeStateMacnine)** |
| :--- |

해당 애니메이션 상태 머신을 변경할 수 있어요. (변경하고 싶은 상태 머신 이름) 
| **bool IsDie()** |
| :--- |

캐릭터가 죽어있는 상태인지 아닌지 얻을 수 있어요. 
| **bool IsFly()** |
| :--- |

캐릭터가 공중에 떠 있는지 아닌지 얻을 수 있어요. 
| **bool IsDriving()** |
| :--- |

캐릭터가 탈 것을 운전 중인지 아닌지 얻을 수 있어요. 
| **float GetMoveSpeed()** |
| :--- |

현재의 캐릭터 이동 속도를 얻을 수 있어요. 
| **ObjectFXClient CreateFX(ObjectFXClient FXObject, Bone BoneType)** |
| :--- |

캐릭터 특정 위치에 FX를 생성할 수 있어요. (생성 하고싶은 FX 오브젝트, [Enum.BoneType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/bone)) 
| **ObjectFXClient CreateFX(String FXName, Bone BoneType)** |
| :--- |

캐릭터 특정 위치에 FX를 생성할 수 있어요. (생성 하고싶은 FX 이름, [Enum.BoneType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/bone)) 
| **ObjectSoundClient CreateSound(ObjectSoundClient SoundObject)** |
| :--- |

캐릭터의 위치에 Sound를 생성할 수 있어요. (생성 하고싶은 Sound 오브젝트) 
| **AddPlayerHUD(string UIName, UISceen UI)** |
| :--- |

UI HUD를 붙일 수 있어요. (붙혀 질 UI 이름, 붙일 UI Sceen) 
| **RemovePlayerHUD(string UIName)** |
| :--- |

UI HUD를 제거해요. (제거하고 싶은 UI 이름) 
| **GetPlayerHUD(string UIName)** |
| :--- |

UI HUD를 얻을 수 있어요. (얻고싶은 UI 이름) 
| **bool IsMyCharacter()** |
| :--- |

플레이어 자신의 캐릭터인지 아닌지 확인할 수 있어요. 
| **SetTransform(Matrix)** |
| :--- |

캐릭터의 위치, 회전을 설정할 수 있어요. (설정할 [Matrix](https://ditoland-utplus.gitbook.io/ditoland/api-reference/common/matrix)값 ) 
| **GetTransform(Matrix)** |
| :--- |

매트릭스를 얻을 수 있어요. (설정할 [Matrix](https://ditoland-utplus.gitbook.io/ditoland/api-reference/common/matrix)값 ) 
| **Vector GetLocation()** |
| :--- |

(Deprecated)현재 캐릭터의 위치를 얻을 수 있어요. 
| **Vector GetForwardVector()** |
| :--- |

(Deprecated)현재 캐릭터의 바라보는 방향을 수 있어요. 
| **SetOrientRotationToMovement(bool bEnable)** |
| :--- |

캐릭터가 바라보는 방향을 이동하는 방향으로 바라 보게 설정해요. (설정 여부) 
# **상속받아 사용 가능한 기능들**

## **속성**

| **Parent** |
| :--- |

부모 객체를 얻을 수 있어요. 
## **이벤트**

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
