# **UI**

| **클라이언트에서 UI를 제어하는 객체** |
| :--- |
## **함수**

| **RModeUIScene GetUIScene(string UISceneName)** |
| :--- |
| **이름으로 UI씬 얻기** |

| **SetVisible(string UISceneName, bool bVisible)** |
| :--- |
| **UI씬의 표시 여부를 설정** |

| **bool IsShow(string UISceneName)** |
| :--- |
| **UI가 보이는지 나타낸다.** |

| **void SetText(string UISceneName, string TextName, int Value)** |
| :--- |
| **UI씬의 위젯 텍스트 설정** |

| **void SetText(string UISceneName, string TextName, float Value)** |
| :--- |
| **UI씬의 위젯 텍스트 설정** |

| **void SetText(string UISceneName, string TextName, string InText)** |
| :--- |
| **UI씬의 위젯 텍스트 설정** |

| **void SetChangeTextEvent(string UISceneName, string TextName, protected_function InEventFunction)** |
| :--- |
| **위젯 텍스트의 변경 시 호출되는 이벤트 함수 설정** |

| **void SetImage(string UISceneName, string ImgName, string Img)** |
| :--- |
| **위젯 이미지 설정** |

| **void SetChangeImageEvent(string UISceneName, string ImgName, protected_function InEventFunction)** |
| :--- |
| **위젯 이미지 변경 시 호출되는 이벤트 함수 설정** |

| **void SetButtonUpEvent(string UISceneName, string ButtonName, protected_function InEventFunction)** |
| :--- |
| **버튼 위젯이 눌렸다 띄어질 때 호출되는 이벤트 함수 설정** |

| **void SetButtonPressEvent(string UISceneName, string ButtonName, protected_function InEventFunction)** |
| :--- |
| **버튼 위젯이 눌릴 때 호출되는 이벤트 함수 설정** |

| **RModeUIScene CreateModeUIScene(string UISceneName)** |
| :--- |
| **UI씬 생성(현재 작동하지 않음)** |

| **void AddChildUIScene(string ParentUISceneName, string UIName, string UISceneName)** |
| :--- |
| **UI씬 스크롤 위젯에 자식 위젯 추가** |

| **AddChildUIScene(string ParentUISceneName, string ParentWidgetName, string UIName, string UISceneName)** |
| :--- |
| **UI씬 스크롤 위젯에 자식 위젯 추가** |

| **RModeUIScene GetChildUIScene(string ParentUISceneName, string UIName)** |
| :--- |
| **UI씬 스크롤 위젯의 자식 위젯 얻기** |

| **RModeUIScene GetChildUIScene(string ParentUISceneName, string ParentWidgetName, string UIName)** |
| :--- |
| **UI씬 스크롤 위젯의 자식 위젯 얻기** |

