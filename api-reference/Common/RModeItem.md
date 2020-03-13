# **RModeItem**

| **월드트리의 아이템 객체** |
| :--- |
# **속성**

| **UseEvent** |
| :--- |
| **아이템 사용 시 호출되는 이벤트** |

| **EquipEvent** |
| :--- |
| **아이템 장착 시 호출되는 이벤트** |

| **UnEquipEvent** |
| :--- |
| **아이템 탈착 시 호출되는 이벤트** |

## **함수**

| **int GetItemCount()** |
| :--- |
| **아이템 개수 얻기** |

| **RResourceID GetIconImg()** |
| :--- |
| **아이템 아이콘 이미지 얻기** |

| **AddAction(string ActionName, LuaScriptFunction Function)** |
| :--- |
| **아이템 착용 후 액션 추가** |

| **AddToggleAction(string ActionName, LuaScriptFunction StartFunction, LuaScriptFunction EndFunction)** |
| :--- |
| **아이템 착용 후 토글 액션 추가** |

