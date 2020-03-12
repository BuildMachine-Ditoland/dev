# **Game**

| **게임 전반적인 역할을 하는 객체. 여기 있는 기능들은 서버, 클라이언트에서 사용할 수 있다. ** |
| :--- |
## **속성**

| **OnEnterPlayer** |
| :--- |
| **새로운 플레이어 게임에 들어올 때 호출되는 이벤트** |

| **OnLeavePlayer** |
| :--- |
| **플레이어가 게임에서 나갈 때 호출되는 이벤트** |

| **OnDeathCharacter** |
| :--- |
| **캐릭터가 죽을 때 호출되는 이벤트** |

| **OnSpawnCharacter** |
| :--- |
| **캐릭터가 스폰 될 때 호출되는 이벤트** |

## **함수**

| **AddPhase(string phasename)** |
| :--- |
| **게임에 단계를 추가한다.** |

| **RModePhase GetPhaseByName(string phasename)** |
| :--- |
| **단계 이름으로 단계 가져오기** |

| **RModePhase GetCurPhase()** |
| :--- |
| **현재 단계 가져오기** |

| **RModePhase ChangePhaseByName(string changephasename)** |
| :--- |
| **단계 이름으로 단계 변경하기** |

| **RModePhase ChangeToNextPhase()** |
| :--- |
| **다음 단계로 변경하기.** |

| **ConnectEventFunction(string customevent, LuaScriptFunction function) ** |
| :--- |
| **유저가 추가하는 이벤트** |

| **float GetPassTime()** |
| :--- |
| **진행된 시간 얻기** |

| **DeleteObject(RModeObject)** |
| :--- |
| **오브젝트 삭제하기** |

