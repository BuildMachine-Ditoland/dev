# **RCharacterServer**


서버에서 사용되는 캐릭터 객체에요. 
## **함수**

| **bool IsDie()** |
| :--- |

현재 죽어있는 상태를 나타낸다. 
| **string GetPlayerName()** |
| :--- |

해당 캐릭터를 소유 하고 있는 플레이어 이름 얻기. 캐릭터에서 플레이어를 얻기위해서는 Game.GetPlayer(string PlayerName) 를 이용 
| **SetMaxSpeed(float Speed)** |
| :--- |

최대 이동 속도 설정 (속도 값) 
| **SetMaxJump(float Jump)** |
| :--- |

최대 점프 속도 설정 (점프 값) 
| **SetFlyControl(float ControlRate);** |
| :--- |

공중에서 컨트롤 비율 설정 (비율 값) 
| **MoveToSpawnPoint(String SpawnPointName, bool ResetRot)** |
| :--- |

특정 스폰 위치로 이동 (이동 할 스폰포인트 이름, 방향 Rot 초기화 여부) 
| **SetTransform(Matrix)** |
| :--- |

캐릭터의 위치, 회전 설정 (Matrix 값) 
| **Vector GetLocation()** |
| :--- |

현재 캐릭터의 위치 얻기 
| **void BeginDriving( number ModeObjectKey )** |
| :--- |

탈 것의 운전을 시작한다. (탈 것의 키 값) 
| **void AttachAt( RModeObject* ModeObject )** |
| :--- |

캐릭터를 해당 오브젝트에 부착시킨다 (부착 할 오브젝트) 
| **void Detach()** |
| :--- |

캐릭터를 오브젝트에서 떨어 뜨린다 
