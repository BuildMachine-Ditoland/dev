
월드 트리에서 UI페이지에 설정된 ScreenUI 객체에요. 
# **상속받아 사용 가능한 기능들**

## **속성**

| **Parent** |
| :--- |

부모 객체를 얻을 수 있어요. 
## **이벤트**

| **OnInitEvent** |
| :--- |

UI가 초기화 되었을 때 호출되는 이벤트에요. 
| **OnVisibleEvent** |
| :--- |

UI가 보여질 때 호출되는 이벤트에요. 
| **OnUpdateEvent** |
| :--- |

UI가 보여지는 동안 매 프라임마다 호출되는 이벤트에요. 
| **OnInVisibleEvent** |
| :--- |

UI가 안 보여질 때 호출되는 이벤트에요. 
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

| **SetVisible(bool bVisible)** |
| :--- |

UI의 표시 여부를 설정할 수 있어요. (UI 표시 여부) 
| **SetWidgetVisible(string WidgetName, bool bVisible)** |
| :--- |

UI 위젯의 표시 여부를 설정할 수 있어요. (설정 할 위젯 이름, UI 표시 여부) 
| **SetWidgetAnchor(string WidgetName, ERObjectUIAnchorType type)** |
| :--- |

UI 위젯의 고정 여부를 설정할 수 있어요. (설정 할 위젯 이름, Anchor Type) 
| **SetWidgetOpacity(string WidgetName, float Opacity)** |
| :--- |

UI 위젯의 투명 값을 설정할 수 있어요. (설정할 값) 
| **SetText(string WidgetName, int Value)** |
| :--- |

위젯의 텍스트를 주어진 정수로 변경해요. (텍스트를 변경할 위젯 이름, 변경할 정수 값) 
| **SetText(string WidgetName, float Value)** |
| :--- |

위젯의 텍스트를 주어진 실수로 변경해요. (텍스트를 변경할 위젯 이름, 변경할 실수 값) 
| **SetText(string WidgetName, string InText)** |
| :--- |

위젯의 텍스트를 주어진 문자열로 변경해요. (텍스트를 변경할 위젯 이름, 변경할 문자열) 
| **SetTextColor(string WidgetName, Color color)** |
| :--- |

텍스트의 색을 설정할 수 있어요. (텍스트 색을 변경할 위젯 이름, 변경할 [Color](https://ditoland-utplus.gitbook.io/ditoland/api-reference/common/color)값) 
| **SetChangeTextEvent(string TextName, protected_function InEventFunction)** |
| :--- |

위젯의 텍스트 변경 시 호출되는 이벤트 함수를 설정해요. (변경을 감지할 Text위젯 이름, 연결 함수) 
| **SetImage(string ImgName, ResoureID TextureID)** |
| :--- |

위젯의 이미지를 설정할 수 있어요. (변경할 Image위젯 이름, 변경할 리소스 ID) 
| **SetChangeImageEvent(string ImgName, protected_function InEventFunction)** |
| :--- |

위젯의 이미지 변경 시 호출되는 이벤트 함수를 설정해요. (변경을 감지할 Image위젯 이름, 연결 함수) 
| **SetButtonUpEvent(string ButtonName, protected_function InEventFunction)** |
| :--- |

버튼 위젯이 눌렸다 띄어질 때 호출되는 이벤트 함수를 설정해요. (이벤트를 감지할 Button위젯 이름, 연결 함수) 
| **SetButtonPressEvent(string ButtonName, protected_function InEventFunction)** |
| :--- |

버튼 위젯이 눌릴 때 호출되는 이벤트 함수를 설정해요. (이벤트를 감지할 Button위젯 이름, 연결 함수) 
| **SetWidgetLocation(string WidgetName, float X, float Y)** |
| :--- |

위젯의 위치를 변경할 수 있어요. (위치를 변경할 위젯 이름, X좌표 값, Y좌표 값) 
| **AddChildUIScene(string ChildUISceneName, FRUIScene* Element)** |
| :--- |

UI씬에 자식 UI씬 추가할 수 있어요. (자식이 될 UI씬 이름, 자식으로 추가할 UI씬) 
| **AddChildUIScene(string ParentWidgetName, string ChildUISceneName, FRUIScene* Element)** |
| :--- |

UI씬에 자식 UI씬 추가할 수 있어요. (부모 UI 이름, 자식이 될 UI씬 이름, 자식으로 추가할 UI씬) 
| **RModeUIScene GetChildUIScene(string ChildUISceneName)** |
| :--- |

스크롤 위젯의 자식 위젯 얻을 수 있어요. (찾을 자식 위젯 이름) 
| **RModeUIScene GetChildUIScene(string ParentWidgetName, string ChildUISceneName)** |
| :--- |

스크롤 위젯의 자식 위젯 얻을 수 있어요. (부모 위젯 이름, 찾을 자식 위젯 이름) 
| **string GetText(string WidgetName)** |
| :--- |

텍스트의 내용을 얻을 수 있어요. (내용을 얻을 위젯 이름) 
| **bool IsWidgetVisible(string WidgetName)** |
| :--- |

위젯이 보이는지를 확인할 수 있어요. (판단할 위젯 이름) 
| **AddUIMove(string WidgetName, string TrackName, Vector Pos, float Time)** |
| :--- |

해당 Scene안에 있는 WidgetName의 이름을 가진 위젯의 이동 변화를 추가할 수 있어요. (이동 변화를 줄 위젯 이름, 트랙 이름, 이동 Vector, 변화 완료까지의 시간) 
| **AddWorldRot(string WidgetName, string TrackName, FVector Rot, float Time)** |
| :--- |

해당 Scene안에 있는 WidgetName의 이름을 가진 위젯의 회전 변화를 추가할 수 있어요. (회전 변화를 줄 위젯 이름, 트랙 이름, 회전 Vector, 변화 완료까지의 시간) 
| **AddUIScale(string WidgetName, string TrackName, FVector Size, float Time)** |
| :--- |

해당 Scene안에 있는 WidgetName의 이름을 가진 위젯의 크기 변화를 추가할 수 있어요. (크기 변화를 줄 위젯 이름, 트랙 이름, 크기 Vector, 변화 완료까지의 시간) 
| **AddUIOpacity(string WidgetName, string TrackName, float opacity, float Time)** |
| :--- |

해당 Scene안에 있는 WidgetName의 이름을 가진 위젯의 투명도 변화를 추가할 수 있어요. (투명도 변화를 줄 위젯 이름, 트랙 이름, 투명도 값, 변화 완료까지의 시간) 
| **AddUIEmpty(string TrackName, string TrackName, float Time)** |
| :--- |

해당 Scene안에 있는 WidgetName의 이름을 가진 위젯의 변환 대기 시간을 추가할 수 있어요. (트랙 이름, 변환 대기 시간) 
| **PlayUIActionTrack(string TrackName, TransformPlayType Type, int PlayCount)** |
| :--- |

설정된 변환 컨트롤러 실행해요. (트랙 이름, [Enum.TransformPlayType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/transformplaytype), 실행 횟수) 
| **StopUIActionTrack(string TrackName)** |
| :--- |

변환 컨트롤러를 정지시켜요. (정지 할 트랙 이름) 
| **PauseUIActionTrack(string TrackName)** |
| :--- |

변환 컨트롤러를 일시 정지시켜요. (일시 정지 할 트랙 이름) 
| **ResumeUIActionTrack(string TrackName)** |
| :--- |

변환 컨트롤러를 다시 플레이해요. (다시 플레이 할 트랙 이름) 
| **IsPlayingUIActionTrack(string TrackName)** |
| :--- |

해당 TransformTrack이 플레이 중인지 확인할 수 있어요. (확인 할 트랙 이름) 
| **ResetUIActionTrack(string TrackName)** |
| :--- |

해당 TransformTrack를 적용되기 전의 Transform으로 리셋시켜요. (리셋 할 트랙 이름) 
| **RemoveUIActionTrack(String TrackName)** |
| :--- |

해당 Track을 제거해요. (제거 할 트랙 이름) 
| **ResetUIActionTrack()** |
| :--- |

TransformTrack 이 적용되기 전의 최초 Transform으로 리셋 시켜요. 
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
