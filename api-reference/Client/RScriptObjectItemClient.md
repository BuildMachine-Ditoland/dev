# **RScriptObjectItemClient**


클라이언트에서 사용되는 아이템 개체에요 
## **함수**

| **AttachTo(RModeRemotePlayer Player, Bone BoneType)** |
| :--- |

아이템을 플레이어에 붙이기 (아이템을 붙일 플레이어, [Enum.Bone.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/bone)) 
| **Detach()** |
| :--- |

플레이어에 붙어 있는 아이템 해제 
| **AddAction(string ActionName, Key ActionKey, bool bAutoAction, LuaScriptFunction Function)** |
| :--- |

아이템 착용 후 액션 추가 (액션 이름, 액션 실행 할 [Enum.Key.키](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/key), 자동 액션 여부, 연결 함수) 
| **AddToggleAction(string ActionName, Key ActionKey, LuaScriptFunction StartFunction, LuaScriptFunction EndFunction)** |
| :--- |

아이템 착용 후 토글 액션 추가 (액션 이름, 액션 실행 할 [Enum.Key.키](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/key), 키 입력 시 연결 함수, 키 입력 종료 시 연결 함수) 
