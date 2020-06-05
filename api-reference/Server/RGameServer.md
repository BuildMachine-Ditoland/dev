# **RGameServer**


게임 전반적인 역할을 하는 객체에요. 여기 있는 기능들은 서버에서만 사용할 수 있어요. 
## **속성**

| **MaxUserCount** |
| :--- |

게임 최대 인원. 디폴트 값은 10 
## **함수**

| **AddUserCollisionType(string UserCollisionType)** |
| :--- |

유저 충돌 타입 설정 추가.  

특정 오브젝트의 충돌 처리를 다른 오브젝트와 다르게 할 때 사용 

예) 특정 오브젝트만 통과하고, 캐릭터는 못 통과하는 오브젝트. 
| **RSpawnPointGroup AddSpawnPointGroup(string SpawnPointGroupName)** |
| :--- |

게임에서 사용 할 스폰 포인트 그룹을 추가한다. 
| **RSpawnPoint AddSpawnPoint(string SpawnPointName, RScriptWorldObject* RWorldObject)** |
| :--- |

게임에서 사용 할 스폰 포인트를 추가한다. 
| **RSpawnPoint AddSpawnPointAtGroup(string SpawnPointGroupName, string SpawnPointName, RScriptWorldObject* RWorldObject)** |
| :--- |

스폰포인트 그룹에 스폰 포인트를 추가한다. 
| **SetSpawnType(ModeSpawnType InSpawnType, string InSpawnObjectName)** |
| :--- |

게임의 스폰포인트 타입을 설정한다. 
| **SetDefaultSpawnPos(FVector Pos)** |
| :--- |

스폰 포인트 설정이 없을 경우 스폰되는 위치 셜정 
| **RModeCharacterSetting AddCharacterSetting(string SettingName)** |
| :--- |

게임에서 사용 할 캐릭터 설정을 추가한다. 
| **Team AddTeam(string TeamName)** |
| :--- |

게임에서 사용 할 팀 설정을 추가한다. 
| **RModeNPCSetting AddNPCSetting(string NPCSettingName)** |
| :--- |

게임에서 사용 할 NPC 설정을 추가한다. 
| **Player GetPlayer(string PlayerName)** |
| :--- |

플레이어를 얻는다 
| **RModeServerCharacter GetPlayerCharacter(string PlayerName)** |
| :--- |

플레이어의 캐릭터를 얻는다. 
| **SetTeamSetting(EModeTeamType TeamType, EDivideTeamType DivideTeamType)** |
| :--- |

게임의 팀전 여부, 팀 나누기 방식을 설정 한다. 
| **int GetPlayerCount()** |
| :--- |

현재 게임에 참여하고 있는 플레이어 수를 얻는다. 
| **ResetTeamSetting()** |
| :--- |

게임의 팀 설정을 모두 없앤다. 
| **ApplyTeamSetting()** |
| :--- |

게임의 팀 설정을 적용한다. 
| **ReqResetGame()** |
| :--- |

게임 리셋을 요청한다. 
| **SetCanEnterUser()** |
| :--- |

게임에 유저의 진입 가능 여부를 설정한다 (false로 설정 할 경우 해당 게임으로 더 이상 유저가 진입하지 않는다) 
| **BroadcastEvent(string CustomEventName, Args ...)** |
| :--- |

모든 클라이언트에게 이벤트를 보낸다. 
| **SendEventToClient(string PlayerName, string CustomEventName, Args ...)** |
| :--- |

해당 클라이언트에게 이벤트를 보낸다 
| **SetInventorySize(int XSize, int YSize)** |
| :--- |

인벤토리 사이즈 설정 
| **SetQuickSlotCount(int Count)** |
| :--- |

퀵 슬롯 개수 설정 
| **PickUpItem(RModeServerCharacter Character, ModeItem Item)** |
| :--- |

해당 케릭터가 아이템을 획득한다. 
| **CreateSyncObject(string ObjectName, Vector Location)** |
| :--- |

해당 위치에 클라이언트와 동기화 되는 오브젝트를 생성한다. 
| **CreateSyncObject(RScriptWorldObject WorldObject, Vector Location)** |
| :--- |

해당 위치에 클라이언트와 동기화 되는 오브젝트를 생성한다. 
| **CreateNoneSyncObject(string ObjectName, Vector Location)** |
| :--- |

해당 위치에 클라이언트와 동기화 되지 않는 오브젝트를 생성한다. 
| **CreateNoneSyncObject(RScriptWorldObject WorldObject, Vector Location)** |
| :--- |

해당 위치에 클라이언트와 동기화 되지 않는 오브젝트를 생성한다. 
| **ObjectSpawner AddObjectSpawner(RObjectScript RObjectScript, EObjectSelectType SpawnType, float SpawnTime, int MaxCount)** |
| :--- |

오브젝트 스포너 생성한다. 
| **ObjectSelector CreateObjectSelector(EObjectSelectType SelectType)** |
| :--- |

오브젝트 셀렉터를 생성한다. 
| **ObjectList GetObjectList(Vector Center, float Radius)** |
| :--- |

해당 영역의 오브젝트 얻기 
| **UseWorldItem(RModeServerCharacter Character, ModeItem Item)** |
| :--- |

월드 아이템 사용하기 
| **DeleteWorldItem(ModeItem Item)** |
| :--- |

월드 아이템 삭제하기 
| **SaveUserGameData(String PlayerName, String KeyString, Vector SaveValue)** |
| :--- |

유저 게임 데이터 저장 
| **SaveUserGameData(String PlayerName, String KeyString, float SaveValue)** |
| :--- |

유저 게임 데이터 저장 
| **SaveUserGameData(String PlayerName, String KeyString, bool SaveValue)** |
| :--- |

유저 게임 데이터 저장 
| **SaveUserGameData(String PlayerName, String KeyString, int SaveValue)** |
| :--- |

유저 게임 데이터 저장 
| **SaveUserGameData(String PlayerName, String KeyString, String SaveValue)** |
| :--- |

유저 게임 데이터 저장 
| **SaveUserGameData(String PlayerName, String KeyString, Color SaveValue)** |
| :--- |

유저 게임 데이터 저장 
| **Object GetSavedUserGameData(String PlayerName, String KeyString)** |
| :--- |

유저 게임 데이터 얻기 
| **SaveGameStatisticsData(String PlayerName, String KeyString, int SaveValue, bool Overwrite, bool Ascending)** |
| :--- |

게임 통계 데이터 저장 
| **GetGameStatisticsData(String KeyString, bool Ascending, int Offset, int Count, LuaScriptFunction CallBack)** |
| :--- |
| **SendToClient_GameStatisticsData(String PlayerName, String KeyString, bool Ascending, int Offset, int Count)** |
| :--- |

게임 통계 데이터 클라이언트로 보내주기 
| **vector<Player> GetAllPlayer()** |
| :--- |

모든 플레이어 얻기 
| **NPC CreateNPC(String NPCName, String NPCSetting, Vector Location)** |
| :--- |

NPC 생성 
| **DeleteNPC(String NPCName)** |
| :--- |

NPC 삭제 
