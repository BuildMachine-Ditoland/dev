# RModeGame

## **RModeGame**

**유저에게 Game으로 제공되는 객체의 부모 객체로, 전체 게임의 틀을 제공**

**플레이어의 진입 떠남, 캐릭터의 죽음, 스폰됨 등 이벤트 함수 제공**

## **Property**

| **var OnSpawnCharacter** |
| :--- |
| **캐릭터가 스폰 될 때 호출되는 이벤트 연결 객체** |

| **var OnDeathCharacter** |
| :--- |
| **캐릭터가 죽을 때 호출되는 이벤트 연결 객체** |

| **var OnLeavePlayer** |
| :--- |
| **플레이어가 나갈 때 호출되는 이벤트 연결 객체** |

| **var OnEnterPlayer** |
| :--- |
| **새로운 플레이어 들어올 때 호출되는 이벤트 연결 객체** |

## **Functions**

| **RModePhase AddPhase\(string phasename\)** |
| :--- |
| **게임에 단계추가 하기** |

| **RModePhase GetPhaseByName\(string phasename\)** |
| :--- |
| **이름으로 단계 가져오기** |

| **RModePhase GetCurPhase\(\)** |
| :--- |
| **현재 단계 가져오기** |

| **RModePhase ChangePhaseByName\(string changephasename\)** |
| :--- |
| **이름으로 단계 변경하기** |

| **RModePhase ChangeToNextPhase\(\)** |
| :--- |
| **다음 단계로 변경하기** |

| **void ConnectEventFunction\(string customevent, LuaScriptFunction function\)** |
| :--- |
| **유저가 추가하는 이벤트** |

| **float GetPassTime\(\)** |
| :--- |
| **진행된 시간 얻기** |

| **void DeleteObject\(RModeObject\)** |
| :--- |
| **모드 오브젝트 삭제하기** |

