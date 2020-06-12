# **UI**


클라이언트에서 UI를 제어하는 객체에요. 
## **함수**

| **RModeUIScene GetUIScene(string UISceneName)** |
| :--- |

이름으로 UI씬을 얻을 수 있어요. (얻고 싶은 UI씬 이름) 
| **SetVisible(string UISceneName, bool bVisible)** |
| :--- |

UI씬의 표시 여부를 설정할 수 있어요. (설정 할 UI씬 이름, 표시 여부) 
| **bool IsShow(string UISceneName)** |
| :--- |

UI가 보이는지 알 수 있어요. (확인 할 UI씬 이름) 
| **SetText(string UISceneName, string TextName, int Value)** |
| :--- |

UI씬안에 있는 텍스트위젯의 텍스트를 설정할 수 있어요. (위젯의 UI씬 이름, 텍스트를 설정 할 위젯 이름, 정수 값) 
| **SetText(string UISceneName, string TextName, float Value)** |
| :--- |

UI씬안에 있는 텍스트위젯의 텍스트를 설정할 수 있어요. (위젯의 UI씬 이름, 텍스트를 설정 할 위젯 이름, 실수 값) 
| **SetText(string UISceneName, string TextName, string InText)** |
| :--- |

UI씬안에 있는 텍스트위젯의 텍스트를 설정할 수 있어요. (위젯의 UI씬 이름, 텍스트를 설정 할 위젯 이름, 문자열) 
| **SetChangeTextEvent(string UISceneName, string TextName, protected_function InEventFunction)** |
| :--- |

위젯 텍스트의 변경 시 호출되는 이벤트 함수를 설정할 수 있어요. (위젯의 UI씬 이름, 텍스트 위젯 이름, 연결 함수) 
| **SetImage(string UISceneName, string ImgName, string Img)** |
| :--- |

이미지위젯의 이미지를 설정할 수 있어요. (위젯의 UI씬 이름, 이미지 위젯 이름, 이미지 주소) 
| **SetChangeImageEvent(string UISceneName, string ImgName, protected_function InEventFunction)** |
| :--- |

위젯 이미지 변경 시 호출되는 이벤트 함수를 설정할 수 있어요. (위젯의 UI씬 이름, 이미지 위젯 이름, 연결 함수) 
| **SetButtonUpEvent(string UISceneName, string ButtonName, protected_function InEventFunction)** |
| :--- |

버튼 위젯이 눌렸다 띄어질 때 호출되는 이벤트 함수를 설정할 수 있어요. (위젯의 UI씬 이름, 버튼 위젯 이름, 연결 함수) 
| **SetButtonPressEvent(string UISceneName, string ButtonName, protected_function InEventFunction)** |
| :--- |

버튼 위젯이 눌릴 때 호출되는 이벤트 함수를 설정할 수 있어요. (위젯의 UI씬 이름, 버튼 위젯 이름, 연결 함수) 
| **RModeUIScene CreateModeUIScene(string UISceneName)** |
| :--- |

UI씬을 생성할 수 있어요. (현재 작동하지 않음) (생성할 UI씬 이름) 
| **AddChildUIScene(string ParentUISceneName, string UIName, string UISceneName)** |
| :--- |

UI씬안에 있는 위젯에 자식 위젯을 추가할 수 있어요. (부모 UI씬 이름, 위젯 이름, 추가 할 UI 이름) 
| **AddChildUIScene(string ParentUISceneName, string ParentWidgetName, string UIName, string UISceneName)** |
| :--- |

UI씬안에 있는 위젯에 자식 위젯을 추가할 수 있어요. (부모 UI씬 이름, 부모 위젯 이름, 위젯 이름, 추가할 UI 이름) 
| **RModeUIScene GetChildUIScene(string ParentUISceneName, string UIName)** |
| :--- |

UI씬안에 있는 자식 위젯을 얻을 수 있어요. (UI씬 부모 이름, 찾을 위젯 이름) 
| **RModeUIScene GetChildUIScene(string ParentUISceneName, string ParentWidgetName, string UIName)** |
| :--- |

UI씬안에 있는 위젯의 자식 위젯을 얻을 수 있어요. (부모 UI씬 이름, 부모 위젯 이름, 찾을 위젯 이름) 
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
