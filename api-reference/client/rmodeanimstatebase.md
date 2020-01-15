# RModeAnimStateBase

### **RModeAnimStateBase**

**애니메이션 상태 타입**  


### **Property**

| **var EnterEvent** |
| :--- |
| **해당 애니메이션 상태로 변경 될 때 호출되는 이벤트 객체** |

| **var UpdateEvent** |
| :--- |
| **해당 애니메이션 상태 일 때 호출되는 이벤트 객체** |

| **var ExitEvent** |
| :--- |
| **해당 애니메이션에서 다른 상태로 변경 될 때 호출되는 이벤트 객체** |

### \*\*\*\*

### **Function**

| **string GetName\(\)** |
| :--- |
| **이름 얻기** |

| **number GetPlayTime\(\)** |
| :--- |
| **애니메이션 상태 플레이 시간 얻기** |

| **void AddTransition\(RModeAnimTransition InTransition\)** |
| :--- |
| **다른 애니메이션 상태로의 전이 추가** |

| **RModeClientCharacter GetOwnerCharacter\(\)** |
| :--- |
| **설정되어 있는 캐릭터 얻기** |

| **void SetNeedReplicate\(bool NeedReplicate\)** |
| :--- |
| **동기화 필요 여부 설정** |

