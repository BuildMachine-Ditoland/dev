# **RModeAnimStateSettingBase**

| **게임에서 사용되는 애니메이션 상태를 설정 할 때 사용되는 베이스 객체.** |
| :--- |
## **속성**

| **OnEnter** |
| :--- |
| **해당 애니메이션 상태로 변경될 때 호출되는 이벤트** |

| **OnUpdate** |
| :--- |
| **해당 애니메이션 상태일 때 매프레임 호출되는 이벤트** |

| **OnExit** |
| :--- |
| **해당 애니미에션 상태에서 다른 애니메이션 상태로 변경 될 때 호출되는 이벤트** |

## **함수**

| **SetNeedReplicate(bool NeedReplicate)** |
| :--- |
| **서버 클라이언트 간 동기화가 필요한 애니메이션 여부를 설정** |

| **AddTransition(RModeAnimTransitionSetting Transition)** |
| :--- |
| **다른 애니메이션 상태로 변경하는 전이 설정 추가** |

