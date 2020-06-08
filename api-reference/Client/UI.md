# **UI**


클라이언트에서 UI를 제어하는 객체에요. 
## **함수**

| **RModeUIScene GetUIScene(string UISceneName)** |
| :--- |

이름으로 UI씬 얻기 (얻고 싶은 UI씬 이름) 
| **SetVisible(string UISceneName, bool bVisible)** |
| :--- |

UI씬의 표시 여부를 설정 (설정 할 UI씬 이름, 표시 여부) 
| **bool IsShow(string UISceneName)** |
| :--- |

UI가 보이는지 나타낸다. (확인 할 UI씬 이름) 
| **SetText(string UISceneName, string TextName, int Value)** |
| :--- |

UI씬안에 있는 위젯의 텍스트를 설정 (위젯의 UI씬 이름, 텍스트를 설정 할 위젯 이름, 정수 값) 
| **SetText(string UISceneName, string TextName, float Value)** |
| :--- |

UI씬안에 있는 위젯의 텍스트를 설정 (위젯의 UI씬 이름, 텍스트를 설정 할 위젯 이름, 실수 값) 
| **SetText(string UISceneName, string TextName, string InText)** |
| :--- |

UI씬안에 있는 위젯의 텍스트를 설정 (위젯의 UI씬 이름, 텍스트를 설정 할 위젯 이름, 문자열) 
| **SetChangeTextEvent(string UISceneName, string TextName, protected_function InEventFunction)** |
| :--- |

위젯 텍스트의 변경 시 호출되는 이벤트 함수 설정 (위젯의 UI씬 이름, 텍스트 위젯 이름, 연결 함수) 
| **SetImage(string UISceneName, string ImgName, string Img)** |
| :--- |

위젯 이미지 설정 (위젯의 UI씬 이름, 이미지 위젯 이름, 이미지 주소) 
| **SetChangeImageEvent(string UISceneName, string ImgName, protected_function InEventFunction)** |
| :--- |

위젯 이미지 변경 시 호출되는 이벤트 함수 설정 (위젯의 UI씬 이름, 이미지 위젯 이름, 연결 함수) 
| **SetButtonUpEvent(string UISceneName, string ButtonName, protected_function InEventFunction)** |
| :--- |

버튼 위젯이 눌렸다 띄어질 때 호출되는 이벤트 함수 설정 (위젯의 UI씬 이름, 버튼 위젯 이름, 연결 함수) 
| **SetButtonPressEvent(string UISceneName, string ButtonName, protected_function InEventFunction)** |
| :--- |

버튼 위젯이 눌릴 때 호출되는 이벤트 함수 설정 (위젯의 UI씬 이름, 버튼 위젯 이름, 연결 함수) 
| **RModeUIScene CreateModeUIScene(string UISceneName)** |
| :--- |

UI씬 생성(현재 작동하지 않음) (생성할 UI씬 이름) 
| **AddChildUIScene(string ParentUISceneName, string UIName, string UISceneName)** |
| :--- |

UI씬안에 있는 위젯에 자식 위젯 추가 (부모 UI씬 이름, 위젯 이름, 추가 할 UI 이름) 
| **AddChildUIScene(string ParentUISceneName, string ParentWidgetName, string UIName, string UISceneName)** |
| :--- |

UI씬안에 있는 위젯에 자식 위젯 추가 (부모 UI씬 이름, 부모 위젯 이름, 위젯 이름, 추가할 UI 이름) 
| **RModeUIScene GetChildUIScene(string ParentUISceneName, string UIName)** |
| :--- |

UI씬안에 있는 자식 위젯 얻기 (UI씬 부모 이름, 찾을 위젯 이름) 
| **RModeUIScene GetChildUIScene(string ParentUISceneName, string ParentWidgetName, string UIName)** |
| :--- |

UI씬 스크롤 위젯의 자식 위젯 얻기 (부모 UI씬 이름, 부모 위젯 이름, 찾을 위젯 이름) 
