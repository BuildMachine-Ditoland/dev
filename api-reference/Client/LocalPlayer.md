# **LocalPlayer**


캐릭터의 기본 동작을 설정 할 수 있는 객체에요. 클라이언트에서 사용 가능해요. 
## **이벤트**

| **ProcessInputAxisEvent(string Event, protected_function ProcessFunc)** |
| :--- |

축 인풋 이벤트 (이벤트 이름, 연결 함수) 
| **ProcessInputActionEvent(string Event, RModeInputType InputType, protected_function ProcessFunc)** |
| :--- |

키 인풋 이벤트 (이벤트 이름, [Enum.KeyInputType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/keyinputtype), 연결 함수) 
| **OnChangedInventoryItem** |
| :--- |

인벤토리 아이템 변화 시 호출되는 이벤트 
## **함수**

| **Move(FVector Dir, float Value)** |
| :--- |

주어진 방향으로 일정 값만큼 캐릭터 이동. 설정된 이동 타입에 상관없이 동작한다. (이동 방향 Vector 값, 이동할 크기) 
| **MoveForward(float Value)** |
| :--- |

설정된 이동 타입에 따른 앞으로 이동 (이동할 크기) 
| **MoveRight(float Value)** |
| :--- |

좌, 우 이동 (이동할 크기) 
| **Turn(float Value)** |
| :--- |

캐릭터의 바라보는 좌우 방향 설정 (이동할 크기) 
| **LookUp(float Value)** |
| :--- |

캐릭터의 바라보는 상하 방향 설정 (이동할 크기) 
| **Jump()** |
| :--- |

점프를 한다. 
| **JumpRelease()** |
| :--- |

점프를 해제 한다.(삭제 예정) 
| **SetEnableMovementeControl(bool Enable)** |
| :--- |

자신의 캐릭터의 움직임 컨트롤을 활성화, 비활성화 한다 (활성, 비활성 여부) 
| **SetEnableCameraControl(bool Enable)** |
| :--- |

자신의 카메라 움직임 컨트롤을 활성화, 비활성화 한다 (활성, 비활성 여부) 
| **SetForwardMoveType(ForwardMoveType Type)** |
| :--- |

MoveForward(float Value)의 작동 방식 설정 (Enum.ForwardMoveType.타입) 

ForwardMoveType::XYPlane - 상, 하 이동되지 않는 평면 이동(일반 적인 캐릭터의 이동 형태) 

ForwardMoveType::Free - 캐릭터가 바라보는 방향으로 이동(프리 카메라의 이동 형태) 

ForwardMoveType::UpDown - 상, 하로만 이동(엘리베이터, 사다리의 이동 형태) 
| **BeginDriving( int InVehicleModeObjectKey )** |
| :--- |

탈 것의 운전을 시작한다 (탈 것의 키 값) 
| **EndDriving()** |
| :--- |

탈 것의 운전을 종료 한다. 
| **FreeCamMoveUp(float Value)** |
| :--- |

프리캠 위, 아래로 이동 (이동할 크기) 
| **Vector GetForwardVector()** |
| :--- |

바라보는 방향 얻기 
| **Vector GetRightVector()** |
| :--- |

오른쪽 벡터 얻기 
| **RModeRemotePlayer GetRemotePlayer()** |
| :--- |

자신의 플레이어 얻기 
| **int GetInventorySize()** |
| :--- |

인벤토리 사이즈 얻기 
| **UseInventoryItem(int IventoryIndex)** |
| :--- |

인벤토리 아이템 사용 (사용할 아이템칸) 
| **EquipInventoryItem(int IventoryIndex)** |
| :--- |

인벤토리 아이템 착용 (착용할 아이템칸) 
| **UnEquipItem(string EquipSlotName)** |
| :--- |

착용 아이템 해지 (해지할 Slot이름) 
| **UnEquipItem(string EquipSlotName, string ActionName)** |
| :--- |

착용 아이템 액션 ( 액션실행 할 Slot이름, 액션 이름) 
| **WorldDropInventoryItem(int InventoryIndex)** |
| :--- |

인벤토리 아이템 월드 드랍 (월드 드랍할 아이템칸) 
