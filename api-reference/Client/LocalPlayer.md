
클라이언트에서 캐릭터의 기본 동작을 설정 할 수 있는 객체에요. 
## **이벤트**

| **ProcessInputAxisEvent(string Event, protected_function ProcessFunc)** |
| :--- |

축 인풋 이벤트에요. (설정할 이벤트 이름, 연결 함수) 
| **ProcessInputActionEvent(string Event, RModeInputType InputType, protected_function ProcessFunc)** |
| :--- |

키 인풋 이벤트에요. (설정할 이벤트 이름, [Enum.KeyInputType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/keyinputtype), 연결 함수) 
| **OnChangedInventoryItem** |
| :--- |

인벤토리 아이템이 변화할 때 호출되는 이벤트에요. 
## **함수**

| **Move(FVector Dir, float Value)** |
| :--- |

주어진 방향으로 일정 값만큼 캐릭터를 이동시켜요. 설정된 이동 타입에 관계없이 동작해요. (원하는 이동방향 Vector 값, 이동할 크기) 
| **MoveForward(float Value)** |
| :--- |

설정된 이동 타입에 따라 앞으로 이동시켜요. (1 : 전진, -1 : 후진 이동) 
| **MoveRight(float Value)** |
| :--- |

좌, 우로 이동시켜요. (-1 : 좌측, 1 : 우측 이동) 
| **Turn(float Value)** |
| :--- |

캐릭터의 바라보는 좌우 방향을 설정해요. (-1 좌측 ~ 1 우측 방향 값) 
| **LookUp(float Value)** |
| :--- |

캐릭터의 바라보는 상하 방향을 설정해요. (-1 밑에 ~ 1 위에 방향 값) 
| **Jump()** |
| :--- |

점프동작을 실행해요. 
| **JumpRelease()** |
| :--- |

점프를 해제 한다.(삭제 예정) 
| **SetEnableMovementeControl(bool Enable)** |
| :--- |

자신의 캐릭터 움직임 컨트롤 가능 여부를 결정해요. (활성, 비활성 여부) 
| **SetEnableCameraControl(bool Enable)** |
| :--- |

자신의 카메라 움직임 컨트롤 가능 여부를 결정해요. (활성, 비활성 여부) 
| **SetForwardMoveType(ForwardMoveType Type)** |
| :--- |

MoveForward(float Value)의 작동 방식을 결정해요. (Enum.ForwardMoveType.타입) 

ForwardMoveType::XYPlane - 상, 하 이동이 되지않고 평면이동만 가능해요.(일반 적인 캐릭터의 이동 형태) 

ForwardMoveType::Free - 캐릭터가 바라보는 방향으로 이동해요. (프리 카메라의 이동 형태) 

ForwardMoveType::UpDown - 상, 하로만 이동해요. (엘리베이터, 사다리의 이동 형태) 
| **BeginDriving( int InVehicleModeObjectKey )** |
| :--- |

탈 것의 운전을 시작하는 함수에요. (탈 것의 키 값) 
| **EndDriving()** |
| :--- |

탈 것의 운전을 종료해요. 
| **FreeCamMoveUp(float Value)** |
| :--- |

프리캠을 위, 아래로 이동시켜요. (이동할 크기) 
| **Vector GetForwardVector()** |
| :--- |

캐릭터가 바라보는 방향을 얻을 수 있어요. 
| **Vector GetRightVector()** |
| :--- |

캐릭터의 오른쪽 벡터를 얻을 수 있어요. 
| **RModeRemotePlayer GetRemotePlayer()** |
| :--- |

자신의 플레이어를 얻을 수 있어요. 
| **int GetInventorySize()** |
| :--- |

인벤토리의 사이즈를 얻을 수 있어요. 
| **UseInventoryItem(int IventoryIndex)** |
| :--- |

지정된 칸의 인벤토리 아이템을 사용해요. (사용할 아이템칸) 
| **EquipInventoryItem(int IventoryIndex)** |
| :--- |

지정된 칸의 인벤토리 아이템을 착용해요. (착용할 아이템칸) 
| **UnEquipItem(string EquipSlotName)** |
| :--- |

장착되어 있는 Slot이름을 통하여 착용 아이템을 해제시켜요. (해제할 Slot이름) 
| **ActionItem(string EquipSlotName, string ActionName)** |
| :--- |

착용하고 있는 아이템의 액션을 설정하는 함수에요. (설정할 장착 Slot이름, 액션 이름) 
| **WorldDropInventoryItem(int InventoryIndex)** |
| :--- |

지정된 칸의 아이템을 월드에 드랍시켜요. (월드 드랍할 아이템칸) 
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

Object:ConnectChangeEventFunction("CurBullet", ChangeCurBullet)   

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
