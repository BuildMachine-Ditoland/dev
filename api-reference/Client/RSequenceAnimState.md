
단일 애니메이션을 플레이하는 애니메이션 상태 객체에요 
## **함수**

| **ChangeAnimation(string ResourceID)** |
| :--- |

애니메이션 변경 (변경할 애니메이션 리소스 ID값) 
# **상속받아 사용 가능한 기능들**

## **속성**

| **Parent** |
| :--- |

부모 객체를 얻을 수 있어요. 
## **이벤트**

| **EnterEvent** |
| :--- |

해당 애니메이션 상태가 시작될 때 호출되는 이벤트에요. 
| **UpdateEvent** |
| :--- |

해당 애니메이션이 실행중 일 때 호출되는 이벤트에요. 
| **ExitEvent** |
| :--- |

해당 애니메이션상태가 끝날 때 호출되는 이벤트에요. 
| **ConnectChangeEventFunction(string ValueName, function FunctionName)** |
| :--- |

추가된 값이 변경 될 때 호출되는 이벤트에요. (Value 이름, 연결 함수) 

샘플 

```lua

local function ChangeCurBullet(value) 

Logger:Log(“Hello”) 

end 

 

-- Object의 "CurBullet" 라는 Value가 변경되면 ChangeCurBullet 함수에 연결 

Object:ConnectChangeEventFunction("CurBullet", ChangeCurBullet)   

``` 
## **함수**

| **float GetPlayTime()** |
| :--- |

애니메이션 상태가 진행된 시간을 얻을 수 있어요. 
| **AddTransition(RModeAnimTransition InTransition)** |
| :--- |

다른 애니메이션 상태로의 전이를 추가해요. (전이 할 다른 애니메이션) 
| **RGameClientCharacter GetOwnerCharacter()** |
| :--- |

설정되어 있는 캐릭터를 얻을 수 있어요. 
| **SetNeedReplicate(bool NeedReplicate)** |
| :--- |

동기화 필요 여부를 설정할 수 있어요. (필요 여부) 
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
