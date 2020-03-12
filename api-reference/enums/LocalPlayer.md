# **LocalPlayer**

| **캐릭터의 기본 동작을 설정 할 수 있는 객체. 클라이언트에서 사용 가능.** |
| :--- |
## **속성**

| **ProcessInputAxisEvent(string Event, protected_function ProcessFunc)** |
| :--- |
| **축 인풋 이벤트** |

| **ProcessInputActionEvent(string Event, RModeInputType InputType, protected_function ProcessFunc)** |
| :--- |
| **키 인풋 이벤트** |

| **OnChangedInventoryItem** |
| :--- |
| **인벤토리 아이템 변화 시 호출되는 이벤트** |

## **함수**

| **Move(FVector Dir, float Value)** |
| :--- |
| **주어진 방향으로 일정 값만큼 캐릭터 이동. 설정된 이동 타입에 상관없이 동작한다.** |

| **MoveForward(float Value)** |
| :--- |
| **설정된 이동 타입에 따른 앞으로 이동** |

| **MoveRight(float Value)** |
| :--- |
| **좌, 우 이동** |

| **Turn(float Value)** |
| :--- |
| **캐릭터의 바라보는 좌우 방향 설정** |

| **LookUp(float Value)** |
| :--- |
| **캐릭터의 바라보는 상하 방향 설정** |

| **Jump()** |
| :--- |
| **점프를 한다.** |

| **SetForwardMoveType(ForwardMoveType Type)** |
| :--- |
| **MoveForward(float Value)의 작동 방식 설정** |

| **FreeCamMoveUp(float Value)** |
| :--- |
| **프리캠 위, 아래로 이동** |

| **Vector GetForwardVector()** |
| :--- |
| **바라보는 방향 얻기** |

| **Vector GetRightVector()** |
| :--- |
| **오른쪽 벡터 얻기** |

| **RModeRemotePlayer GetRemotePlayer()** |
| :--- |
| **자신의 플레이어 얻기** |

| **int GetInventorySize()** |
| :--- |
| **UseInventoryItem(int IventoryIndex)** |

| **인벤토리 아이템 사용** |
| :--- |
| **EquipInventoryItem(int IventoryIndex)** |

| **인벤토리 아이템 착용** |
| :--- |
| **UnEquipItem(string EquipSlotName)** |

| **착용 아이템 해지** |
| :--- |
| **UnEquipItem(string EquipSlotName, string ActionName)** |

| **착용 아이템 액션** |
| :--- |
| **WorldDropInventoryItem(int InventoryIndex)** |

| **인벤토리 아이템 월드 드랍** |
| :--- |
