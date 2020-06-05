# **RItem**


아이템 객체에요. 
# **이벤트**

| **UseEvent** |
| :--- |

아이템 사용 시 호출되는 이벤트 
| **EquipEvent** |
| :--- |

아이템 장착 시 호출되는 이벤트 
| **UnEquipEvent** |
| :--- |

아이템 탈착 시 호출되는 이벤트 
## **함수**

| **GetItemCount()** |
| :--- |

아이템 개수 얻기 
| **RResourceID GetIconImg()** |
| :--- |

아이템 아이콘 이미지 얻기 
| **AddAction(string ActionName, LuaScriptFunction Function)** |
| :--- |

아이템 착용 후 액션 추가 (액션 이름, 연결 함수) 
| **AddToggleAction(string ActionName, LuaScriptFunction StartFunction, LuaScriptFunction EndFunction)** |
| :--- |

아이템 착용 후 토글 액션 추가 (액션 이름, 액션 시작 시 연결 함수, 액션 종료 시 연결 함수) 
