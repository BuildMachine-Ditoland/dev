# **RModeUIScene**

| **클라이언트에서 보여지는 UI페이지이며, 설정되어 있는 위젯 객체를 제어하는 객체** |
| :--- |
# **속성**

| **OnInitEvent** |
| :--- |
| **UI가 초기화 되었을 때 호출되는 이벤트** |

| **OnVisibleEvent** |
| :--- |
| **UI가 보여질 때 호출되는 이벤트** |

| **OnUpdateEvent** |
| :--- |
| **UI가 보여지는 동안 호출되는 이벤트** |

| **OnInVisibleEvent** |
| :--- |
| **UI가 안 보여질 때 호출되는 이벤트 객체** |

## **함수**

| **SetVisible(bool bVisible)** |
| :--- |
| **UI의 표시 여부를 설정** |

| **SetWidgetVisible(const std::string&WidgetName, bool bVisible)** |
| :--- |
| **UI 위젯의 표시 여부를 설정** |

| **SetText(string WidgetName, int Value)** |
| :--- |
| **위젯의 정수 값을 설정** |

| **SetText(string WidgetName, float Value)** |
| :--- |
| **위젯의 실수 값을 설정** |

| **SetText(string WidgetName, string InText)** |
| :--- |
| **위젯의 문자열을 설정** |

| **SetTextColor(string WidgetName, Color color)** |
| :--- |
| **텍스트 색 설정** |

| **SetChangeTextEvent(string TextName, protected_function InEventFunction)** |
| :--- |
| **위젯의 텍스트 변경 시 호출되는 이벤트 함수 설정** |

| **SetImage(string ImgName, ResoureID TextureID)** |
| :--- |
| **위젯의 이미지 설정** |

| **SetChangeImageEvent(string ImgName, protected_function InEventFunction)** |
| :--- |
| **위젯의 이미지 변경 시 호출되는 이벤트 함수 설정** |

| **SetButtonUpEvent(string ButtonName, protected_function InEventFunction)** |
| :--- |
| **버튼 위젯이 눌렸다 띄어질 때 호출되는 이벤트 함수 설정** |

| **SetButtonPressEvent(string ButtonName, protected_function InEventFunction)** |
| :--- |
| **버튼 위젯이 눌릴 때 호출되는 이벤트 함수 설정** |

| **SetWidgetLocation(string WidgetName, float X, float Y)** |
| :--- |
| **위젯의 위치 변경** |

| **AddChildUIScene(string ChildUISceneName, FRUIScene* Element)** |
| :--- |
| **UI씬에 자식 UI씬 추가** |

| **AddChildUIScene(string ParentWidgetName, string ChildUISceneName, FRUIScene* Element)** |
| :--- |
| **UI씬에 자식 UI씬 추가** |

| **RModeUIScene GetChildUIScene(string ChildUISceneName)** |
| :--- |
| **자식 UI씬 얻기** |

| **RModeUIScene GetChildUIScene(string ParentWidgetName, string ChildUISceneName)** |
| :--- |
| **자식 UI씬 얻기** |

| **string GetText(string WidgetName)** |
| :--- |
| **텍스트 내용 얻기** |

| **bool IsWidgetVisible(string WidgetName)** |
| :--- |
| **위젯이 보이는지를 나타낸다.** |

