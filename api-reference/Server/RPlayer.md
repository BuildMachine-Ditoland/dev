# **RPlayer**


게임에 참여한 플레이어 객체에요. 
## **함수**

| **RModeServerCharacter GetCharacter()** |
| :--- |

플레이어의 캐릭터 얻기 
| **string GetPlayerName()** |
| :--- |

플레이어 이름 얻기 
| **string GetTeamName()** |
| :--- |

플레이어가 속해있는 팀 이름 얻기 
| **int GetLifeCount()** |
| :--- |

플레이어가 리스폰 할 수 있는 횟수 얻기 
| **RequestDie()** |
| :--- |

플레이어 죽음 처리. 
| **RespawnTime()** |
| :--- |

플레이어 리스폰. 설정된 시간 후 리스폰 됨 
| **SetCheckPoint(string SpawnPointName)** |
| :--- |

플레이어 체크 포인트 설정 (스폰 포인트 이름) 
| **SetFreeCamMode(bool bFreeCam)** |
| :--- |

플레이어 프리캠 모드 여부 설정 (프리캠 여부) 
| **RequestFreeCam(float WaitTime)** |
| :--- |

플레이어 프리캠 모드 요청. 설정 시간 후 프리캠 모드로 변경 (대기 시간) 
| **GiveItem(string ItemName, int Count)** |
| :--- |

플레이어에게 아이템 주기 (아이템 이름, 개수) 
| **GiveItem(string ItemName)** |
| :--- |

플레이어에게 아이템 주기 (아이템 이름) 
| **ClearItem()** |
| :--- |

플레이어 아이템 모두 제거 
| **EquipInventoryItem(int InventoryIndex)** |
| :--- |

플레이어 아이템 장착 (장착 할 인벤토리 칸) 
| **SetEnableCollisionBetweenCharacters(bool Enable)** |
| :--- |

플레이어 간 충돌 여부 설정 (충돌 여부) 
| **SetUserCollisionTypeResponse(string UserCollisionType, CollisionResponse Response)** |
| :--- |

유저 충돌 타입의 반응 설정 (충돌 타입 이름 설정, [Enum.CollisionResponse.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/collisionresponse)) 
| **bool HaveInventorySaveData()** |
| :--- |

저장소에 저장된 인벤토리 데이터가 있는지 나타낸다. 
| **RModeHitResult LineTrace(Vector Start, Vector Dir, float Distance)** |
| :--- |

바라 보는 방향으로 인자 거리 만큼 충돌 체크 (시작 지점 Vector, 목표 지점 Vector, 거리 값) 
| **ModeItemServer GetInventoryItem(int InventoryIndex)** |
| :--- |

인벤토리 아이템 얻기 (인벤토리 칸) 
| **ModeItemServer GetEquipItem(String EquipSlot)** |
| :--- |

착용 아이템 얻기 (장착 중인 아이템 슬롯) 
