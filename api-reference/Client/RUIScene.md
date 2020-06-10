# **RUIScene**


클라이언트에서 보여지는 UI페이지이며, 설정되어 있는 위젯 객체를 제어하는 객체에요. 
## **이벤트**

| **OnInitEvent** |
| :--- |

UI가 초기화 되었을 때 호출되는 이벤트 
| **OnVisibleEvent** |
| :--- |

UI가 보여질 때 호출되는 이벤트 
| **OnUpdateEvent** |
| :--- |

UI가 보여지는 동안 호출되는 이벤트 
| **OnInVisibleEvent** |
| :--- |

UI가 안 보여질 때 호출되는 이벤트 객체 
## **함수**

| **SetVisible(bool bVisible)** |
| :--- |

UI의 표시 여부를 설정 (UI 표시 여부) 
| **SetWidgetVisible(string WidgetName, bool bVisible)** |
| :--- |

UI 위젯의 표시 여부를 설정 (설정 할 위젯 이름, UI 표시 여부) 
| **SetWidgetAnchor(string WidgetName, ERObjectUIAnchorType type)** |
| :--- |

UI 위젯의 고정 여부를 설정 (설정 할 위젯 이름, Anchor Type) 
| **SetWidgetOpacity(string WidgetName, float Opacity)** |
| :--- |

UI 위젯의 투명 값을 설정 (설정할 값) 
| **SetText(string WidgetName, int Value)** |
| :--- |

위젯의 텍스트를 주어진 정수로 변경 (텍스트를 변경할 위젯 이름, 변경할 정수 값) 
| **SetText(string WidgetName, float Value)** |
| :--- |

위젯의 텍스트를 주어진 실수로 변경 (텍스트를 변경할 위젯 이름, 변경할 실수 값) 
| **SetText(string WidgetName, string InText)** |
| :--- |

위젯의 텍스트를 주어진 문자열로 변경 (텍스트를 변경할 위젯 이름, 변경할 문자열) 
| **SetTextColor(string WidgetName, Color color)** |
| :--- |

텍스트 색 설정 (텍스트 색을 변경할 위젯 이름, 변경할 [Color](https://ditoland-utplus.gitbook.io/ditoland/api-reference/common/color)값) 
| **SetChangeTextEvent(string TextName, protected_function InEventFunction)** |
| :--- |

위젯의 텍스트 변경 시 호출되는 이벤트 함수 설정 (변경을 감지할 Text위젯 이름, 연결 함수) 
| **SetImage(string ImgName, ResoureID TextureID)** |
| :--- |

위젯의 이미지 설정 (변경할 Image위젯 이름, 변경할 리소스 ID) 
| **SetChangeImageEvent(string ImgName, protected_function InEventFunction)** |
| :--- |

위젯의 이미지 변경 시 호출되는 이벤트 함수 설정 (변경을 감지할 Image위젯 이름, 연결 함수) 
| **SetButtonUpEvent(string ButtonName, protected_function InEventFunction)** |
| :--- |

버튼 위젯이 눌렸다 띄어질 때 호출되는 이벤트 함수 설정 (이벤트를 감지할 Button위젯 이름, 연결 함수) 
| **SetButtonPressEvent(string ButtonName, protected_function InEventFunction)** |
| :--- |

버튼 위젯이 눌릴 때 호출되는 이벤트 함수 설정 (이벤트를 감지할 Button위젯 이름, 연결 함수) 
| **SetWidgetLocation(string WidgetName, float X, float Y)** |
| :--- |

위젯의 위치 변경 (위치를 변경할 위젯 이름, X좌표 값, Y좌표 값) 
| **AddChildUIScene(string ChildUISceneName, FRUIScene* Element)** |
| :--- |

UI씬에 자식 UI씬 추가 (자식이 될 UI씬 이름, 자식으로 추가할 UI씬) 
| **AddChildUIScene(string ParentWidgetName, string ChildUISceneName, FRUIScene* Element)** |
| :--- |

UI씬에 자식 UI씬 추가 (부모 UI 이름, 자식이 될 UI씬 이름, 자식으로 추가할 UI씬) 
| **RModeUIScene GetChildUIScene(string ChildUISceneName)** |
| :--- |

스크롤 위젯의 자식 위젯 얻기 (찾을 자식 위젯 이름) 
| **RModeUIScene GetChildUIScene(string ParentWidgetName, string ChildUISceneName)** |
| :--- |

스크롤 위젯의 자식 위젯 얻기 (부모 위젯 이름, 찾을 자식 위젯 이름) 
| **string GetText(string WidgetName)** |
| :--- |

텍스트 내용 얻기 (내용을 얻을 위젯 이름) 
| **bool IsWidgetVisible(string WidgetName)** |
| :--- |

위젯이 보이는지를 나타낸다. (판단할 위젯 이름) 
| **AddUIMove(string WidgetName, string TrackName, Vector Pos, float Time)** |
| :--- |

해당 Scene안에 있는 WidgetName의 이름을 가진 위젯의 이동 변화를 추가한다. (이동 변화를 줄 위젯 이름, 트랙 이름, 이동 Vector, 변화 완료까지의 시간) 
| **AddWorldRot(string WidgetName, string TrackName, FVector Rot, float Time)** |
| :--- |

해당 Scene안에 있는 WidgetName의 이름을 가진 위젯의 회전 변화를 추가한다. (회전 변화를 줄 위젯 이름, 트랙 이름, 회전 Vector, 변화 완료까지의 시간) 
| **AddUIScale(string WidgetName, string TrackName, FVector Size, float Time)** |
| :--- |

해당 Scene안에 있는 WidgetName의 이름을 가진 위젯의 크기 변화를 추가한다. (크기 변화를 줄 위젯 이름, 트랙 이름, 크기 Vector, 변화 완료까지의 시간) 
| **AddUIOpacity(string WidgetName, string TrackName, float opacity, float Time)** |
| :--- |

해당 Scene안에 있는 WidgetName의 이름을 가진 위젯의 투명도 변화를 추가한다. (투명도 변화를 줄 위젯 이름, 트랙 이름, 투명도 값, 변화 완료까지의 시간) 
| **AddUIEmpty(string TrackName, string TrackName, float Time)** |
| :--- |

해당 Scene안에 있는 WidgetName의 이름을 가진 위젯의 변환 대기 시간을 추가한다. (트랙 이름, 변환 대기 시간) 
| **PlayUIActionTrack(string TrackName, TransformPlayType Type, int PlayCount)** |
| :--- |

설정된 변환 컨트롤러 실행 (트랙 이름, [Enum.TransformPlayType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/transformplaytype), 실행 횟수) 
| **StopUIActionTrack(string TrackName)** |
| :--- |

변환 컨트롤러 정지 (정지 할 트랙 이름) 
| **PauseUIActionTrack(string TrackName)** |
| :--- |

변환 컨트롤러 일시 정지 (일시 정지 할 트랙 이름) 
| **ResumeUIActionTrack(string TrackName)** |
| :--- |

변환 컨트롤러 다시 플레이 (다시 플레이 할 트랙 이름) 
| **IsPlayingUIActionTrack(string TrackName)** |
| :--- |

해당 TransformTrack이 플레이 중인지 확인 (확인 할 트랙 이름) 
| **ResetUIActionTrack(string TrackName)** |
| :--- |

해당 TransformTrack를 적용되기 전의 Transform으로 리셋 (리셋 할 트랙 이름) 
| **RemoveUIActionTrack(String TrackName)** |
| :--- |

해당 Track 제거 (제거 할 트랙 이름) 
| **ResetUIActionTrack()** |
| :--- |

TransformTrack 이 적용되기 전의 최초 Transform으로 설정 
