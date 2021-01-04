
애니메이션 상태 머신을 다루는 객체에요. [RGameClient](https://ditoland-utplus.gitbook.io/ditoland/api-reference/client/rgameclient#undefined-1)의 Game:AddAnimStateMachineSetting 함수로 생성 가능해요. 

Game:AddAnimStateMachineSetting 로 상태머신 생성한 후 Game:SetCharacterAnimStateMachine 로 해당 애니메이션 상태머신을 사용 할 캐릭터로 설정하면, 

해당 캐릭터 셋팅으로 캐릭터 생성 될 때 해당 애니메이션 상태머신이 설정 돼요. 
## **함수**

| **RModeSequenceAnimState AddAnimState(string StateName, string ResourceID)** |
| :--- |

단일 애니메이션을 플레이하는 애니메이션 상태를 추가해요. (추가할 상태 이름, 리소스 ID) 
| **RModeSequenceAnimState AddAnimState(string StateName, string ResourceID, int PlayCount)** |
| :--- |

단일 애니메이션을 플레이하는 애니메이션 상태를 추가해요. (추가할 상태 이름, 리소스 ID, 플레이 횟수) 
| **RModeSequenceAnimState AddAnimState(string StateName, string ResourceID, int Playcount, float PlaySpeed)** |
| :--- |

단일 애니메이션을 플레이하는 애니메이션 상태를 추가해요. (추가할 상태 이름, 리소스 ID, 플레이 횟수, 플레이 속도) 
| **RModeBlendAnimState AddBlendAnimState(string StateName, protected_function BlendFunction)** |
| :--- |

블렌드 애니메이션 상태를 추가해요. (추가할 상태 이름, 연결 함수) 
| **RModeBlendAnimState AddBlendAnimState(string StateName, protected_function BlendFunction, int PlayCount)** |
| :--- |

블렌드 애니메이션 상태를 추가해요. (추가할 상태 이름, 연결 함수, 플레이할 횟수) 
| **AddTransition(string FromState, string ToState)** |
| :--- |

애니메이션 상태 전이를 추가해요. (시작 상태 이름, 전이할 상태 이름) 
| **AddTransition(string FromState, string ToState, float BlendTime)** |
| :--- |

애니메이션 상태 전이를 추가해요. (시작 상태 이름, 전이할 상태 이름, 블렌딩 시간) 
| **AddTransition(string FromState, string ToState, protected_function Condition)** |
| :--- |

애니메이션 상태 전이를 추가해요. (시작 상태 이름, 전이할 상태 이름, 연결 함수) 
| **AddTransition(string FromState, string ToState, protected_function Condition, float BlendTime)** |
| :--- |

애니메이션 상태 전이를 추가해요. (시작 상태 이름, 전이할 상태 이름, 연결 함수, 블렌딩 시간) 
| **SetStartStateName(string StateName)** |
| :--- |

애니메이션 상태 머신이 활성화 될 때 시작 애니메이션 상태를 설정할 수 있어요. (설정할 상태 이름) 
| **ChangeAnimStateDirect_ForScript(string ChangeStateName)** |
| :--- |

해당 이름의 애니메이션 상태로 전이해요. (변경할 상태 이름) 
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
| **bool IsSpotLight()** |
| :--- |

스포트 라이트인지 확인할 수 있어요. 
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
