# **RModeServerCharacter**

| **서버 플레이어 캐릭터** |
| :--- |
## **함수**

| **bool IsDie()** |
| :--- |
| **현재 죽어있는 상태를 나타낸다.** |

| **string GetPlayerName()** |
| :--- |
| **해당 캐릭터를 소유 하고 있는 플레이어 이름 얻기. 캐릭터에서 플레이어를 얻기위해서는 Game.GetPlayer(string PlayerName) 를 이용** |

| **SetMaxSpeed(float Speed)** |
| :--- |
| **최대 이동 속도 설정** |

| **SetMaxJump(float Jump)** |
| :--- |
| **최대 점프 속도 설정** |

| **SetFlyControl(float ControlRate);** |
| :--- |
| **공중에서 컨트롤 비율 설정** |

| **MoveToSpawnPoint(String SpawnPointName, bool ResetRot)** |
| :--- |
| **특정 스폰 위치로 이동** |

| **Vector GetLocation()** |
| :--- |
| **현재 캐릭터의 위치 얻기** |

