# **RBlendAnimState**


[RAnimStateBase](https://ditoland-utplus.gitbook.io/ditoland/api-reference/client/ranimstatebase)의 자식 객체로, 여러 애니메이션을 특정 값에 따라 블랜딩하는 애니메이션 상태 객체에요. 
## **함수**

| **AddBlendAnimation(float BlendValue, string AnimResourceID)** |
| :--- |

블랜드 애니메이션 추가 (블렌드 값, 리소스 ID) 
| **AddBlendAnimation(float BlendValue, string AnimResourceID, float InPlaySpeed)** |
| :--- |

블랜드 애니메이션 추가 (블렌드 값, 리로스 ID, 플레이 횟수) 
# **상속받아 사용 가능한 기능들**

## **속성**

| **Parent** |
| :--- |

부모 오브젝트 
## **이벤트**

| **EnterEvent** |
| :--- |

해당 애니메이션 상태로 변경 될 때 호출되는 이벤트 
| **UpdateEvent** |
| :--- |

해당 애니메이션 상태 일 때 호출되는 이벤트 
| **ExitEvent** |
| :--- |

해당 애니메이션에서 다른 상태로 변경 될 때 호출되는 이벤트 
| **ConnectChangeEventFunction(string ValueName, function FunctionName)** |
| :--- |

추가된 값이 변경 될 때 호출되는 이벤트 (Value 이름, 연결 함수) 

샘플 

```lua

local function ChangeCurBullet(value) 

Logger:Log(“Hello”) 

end 

 

-- Object의 "CurBullet" 라는 Value가 변경되면 ChangeCurBullet 함수에 연결 

Object:ConnectChangeEventFunction("CurBullet", ChangeCurBullet)   

``` 
## **함수**

| **string GetName()** |
| :--- |

이름 얻기 
| **float GetPlayTime()** |
| :--- |

애니메이션 상태 플레이 시간 얻기 
| **AddTransition(RModeAnimTransition InTransition)** |
| :--- |

다른 애니메이션 상태로의 전이 추가 (전이 할 다른 애니메이션) 
| **RGameClientCharacter GetOwnerCharacter()** |
| :--- |

설정되어 있는 캐릭터 얻기 
| **SetNeedReplicate(bool NeedReplicate)** |
| :--- |

동기화 필요 여부 설정 (필요 여부) 
| **string GetName()** |
| :--- |

이름 얻기 
| **RModeObject GetParent(string ParentName)** |
| :--- |

이름으로 부모 객체 얻기 (찾고싶은 부모 객체 이름) 
| **RModeObject GetChild(string ChildName)** |
| :--- |

이름으로 자식 객체 얻기 (찾고싶은 자식 객체 이름) 
| **RModeObject GetGetSibling(string Name)** |
| :--- |

이름으로 형제 객체 얻기 (찾고싶은 형제 객체 이름) 
| **bool IsCharacter()** |
| :--- |

캐릭터인지 확인 
| **bool IsStaticMesh()** |
| :--- |

스테틱 메시인지 확인 
| **bool IsFX()** |
| :--- |

FX인지 확인 
| **bool IsSound()** |
| :--- |

Sound인지 확인 
| **bool IsPointLight()** |
| :--- |

포인트 라이트인지 확인 
| **bool IsSurfaceUI()** |
| :--- |

서피스 UI인지 확인 
| **bool IsScreenUI()** |
| :--- |

스크린 UI인지 확인 
| **bool IsItem()** |
| :--- |

아이템인지 확인 
| **bool IsNPC()** |
| :--- |

NPC인지 확인 
| **bool IsFolder()** |
| :--- |

폴더인지 확인 
| **bool IsScript()** |
| :--- |

스트립트인지 확인 
| **bool IsCollider()** |
| :--- |

Collider인지 확인 
| **bool IsWidget()** |
| :--- |

Widget인지 확인 
| **AddReplicateValue(string ValueName, Vector Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화 기능이 있는 벡터를 추가 (추가할 Value 이름, Vector 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, float Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화 기능이 있는 실수를 추가 (추가할 Value 이름, float 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, bool Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화 기능이 있는 bool를 추가 (추가할 Value 이름, bool 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, string Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화 기능이 있는 문자열을 추가 (추가할 Value 이름, string 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, Color Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화 기능이 있는 칼라를 추가 (추가할 Value 이름, Color 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddSaveValue(string ValueName, Vector Data)** |
| :--- |

해당 객체 저장소에 벡터를 추가 (Value 이름, Vector 데이터) 
| **AddSaveValue(string ValueName, float Data)** |
| :--- |

해당 객체 저장소에 실수를 추가 (Value 이름, float 데이터) 
| **AddSaveValue(string ValueName, bool Data)** |
| :--- |

해당 객체 저장소에 bool을 추가 (Value 이름, bool 데이터) 
| **AddSaveValue(string ValueName, string Data)** |
| :--- |

해당 객체 저장소에 문자열을 추가 (Value 이름, string 데이터) 
| **AddSaveValue(string ValueName, Color Data)** |
| :--- |

해당 객체 저장소에 칼라를 추가 (Value 이름, Color 데이터) 
