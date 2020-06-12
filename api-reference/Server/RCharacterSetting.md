# **RCharacterSetting**


게임에서 사용 될 캐릭터를 설정 할 때 사용되는 객체에요.  

[Game:AddCharacterSetting](https://ditoland-utplus.gitbook.io/ditoland/api-reference/server/rgameserver)함수로 추가해요. 
## **속성**

| **UseSelfcharacter** |
| :--- |

자신의 캐릭터의 사용 여부 

true로 설정하면 자신의 아바타 사용, false시 ResourcePath 에 설정된 캐릭터 사용- 현재는 무조건 false 처리됨 
| **string ResourcePath** |
| :--- |

캐릭터 리소스 경로 (현재 언리얼 리소스 참조경로, 추후 리소스 아이디로 대체) 
| **int MaxLife** |
| :--- |

최대 생명 설정 

캐릭터는 해당 생명만큼 리스폰된다. -1로 설정 시 무한 리스폰 디폴트 값은 -1 
| **float RespawnTime** |
| :--- |

리스폰 타임 
| **float MoveSpeed** |
| :--- |

이동 스피드 
| **float JumpSpeed** |
| :--- |

점프 높이 
| **float FlyControlRate** |
| :--- |

공중에서 컨트롤 비율 
# **상속받아 사용 가능한 기능들**

## **속성**

| **Parent** |
| :--- |

부모 오브젝트 
## **이벤트**

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
