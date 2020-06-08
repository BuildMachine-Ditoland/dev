# **RGameServer**


게임 전반적인 역할을 하는 객체에요. 여기 있는 기능들은 서버에서만 사용할 수 있어요. 
## **속성**

| **MaxUserCount** |
| :--- |

게임 최대 인원. 디폴트 값은 10 
## **함수**

| **AddUserCollisionType(string UserCollisionType)** |
| :--- |

유저 충돌 타입 설정 추가 (충돌 타입 이름 설정) 

특정 오브젝트의 충돌 처리를 다른 오브젝트와 다르게 할 때 사용 

예) 특정 오브젝트만 통과하고, 캐릭터는 못 통과하는 오브젝트. 
| **RSpawnPointGroup AddSpawnPointGroup(string SpawnPointGroupName)** |
| :--- |

게임에서 사용 할 스폰 포인트 그룹을 추가한다. (스폰 포인트 그룹 이름 설정) 
| **RSpawnPoint AddSpawnPoint(string SpawnPointName, RScriptWorldObject* RWorldObject)** |
| :--- |

게임에서 사용 할 스폰 포인트를 추가한다. (스폰 포인트 이름 설정, 스폰 포인트로 지정 할 오브젝트) 
| **RSpawnPoint AddSpawnPointAtGroup(string SpawnPointGroupName, string SpawnPointName, RScriptWorldObject* RWorldObject)** |
| :--- |

스폰포인트 그룹에 스폰 포인트를 추가한다. (스폰포인트를 추가할 그룹 이름, 스폰 포인트 이름, 스폰 포인트를 할 오브젝트) 
| **SetSpawnType(ModeSpawnType InSpawnType, string InSpawnObjectName)** |
| :--- |

게임의 스폰포인트 타입을 설정한다. ( [Enum.SpawnType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/spawntype), 스폰포인트 이름) 
| **SetDefaultSpawnPos(FVector Pos)** |
| :--- |

스폰 포인트 설정이 없을 경우 스폰되는 위치 셜정 (스폰 위치 Vector) 
| **RModeCharacterSetting AddCharacterSetting(string SettingName)** |
| :--- |

게임에서 사용 할 캐릭터 설정을 추가한다. (추가한 이름 설정) 
| **Team AddTeam(string TeamName)** |
| :--- |

게임에서 사용 할 팀 설정을 추가한다. (팀 이름 설정) 
| **RModeNPCSetting AddNPCSetting(string NPCSettingName)** |
| :--- |

게임에서 사용 할 NPC 설정을 추가한다. (NPC 이름 설정) 
| **Player GetPlayer(string PlayerName)** |
| :--- |

플레이어를 얻는다 (얻고 싶은 플레이어 이름) 
| **RModeServerCharacter GetPlayerCharacter(string PlayerName)** |
| :--- |

플레이어의 캐릭터를 얻는다. (얻고 싶은 플레이어 이름) 
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

모든 클라이언트에게 이벤트를 보낸다. (이벤트 이름, 전달할 변수들 ...) 
| **SendEventToClient(string PlayerName, string CustomEventName, Args ...)** |
| :--- |

해당 클라이언트에게 이벤트를 보낸다 (이벤트 보낼 플레이어 이름, 이벤트 이름, 전달할 변수들 ...) 
| **SetInventorySize(int XSize, int YSize)** |
| :--- |

인벤토리 사이즈 설정 (가로 사이즈, 세로 사이즈) 
| **SetQuickSlotCount(int Count)** |
| :--- |

퀵 슬롯 개수 설정 (개수 값) 
| **PickUpItem(RModeServerCharacter Character, ModeItem Item)** |
| :--- |

해당 케릭터가 아이템을 획득한다. (아이템을 획득할 캐릭터, 아이템 객체) 
| **CreateSyncObject(string ObjectName, Vector Location)** |
| :--- |

해당 위치에 클라이언트와 동기화 되는 오브젝트를 생성한다. (생성 할 오브젝트 이름, 생성 위치 Vector) 
| **CreateSyncObject(RScriptWorldObject WorldObject, Vector Location)** |
| :--- |

해당 위치에 클라이언트와 동기화 되는 오브젝트를 생성한다. (생성 할 오브젝트, 생성 위치 Vector) 
| **CreateNoneSyncObject(string ObjectName, Vector Location)** |
| :--- |

해당 위치에 클라이언트와 동기화 되지 않는 오브젝트를 생성한다. (생성 할 오브젝트 이름, 생성 위치 Vector) 
| **CreateNoneSyncObject(RScriptWorldObject WorldObject, Vector Location)** |
| :--- |

해당 위치에 클라이언트와 동기화 되지 않는 오브젝트를 생성한다. (생성 할 오브젝트, 생성 위치 Vector) 
| **ObjectSpawner AddObjectSpawner(RObjectScript RObjectScript, EObjectSelectType SpawnType, float SpawnTime, int MaxCount)** |
| :--- |

오브젝트 스포너 생성한다. (스폰 할 오브젝트, [Enum.SpawnType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/spawntype), 스폰 시칸, 최대 스폰 개수) 
| **ObjectSelector CreateObjectSelector(EObjectSelectType SelectType)** |
| :--- |

오브젝트 셀렉터를 생성한다. ( [Enum.ObjectSelectType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/objectselecttype)) 
| **ObjectList GetObjectList(Vector Center, float Radius)** |
| :--- |

해당 영역의 오브젝트 얻기 (영역 중앙 포인트 Vector, 영역 반지름 값) 
| **UseWorldItem(RModeServerCharacter Character, ModeItem Item)** |
| :--- |

월드 아이템 사용하기 (사용할 캐릭터, 사용할 아이템) 
| **DeleteWorldItem(ModeItem Item)** |
| :--- |

월드 아이템 삭제하기 (삭제할 아이템) 
| **SaveUserGameData(String PlayerName, String KeyString, Vector SaveValue)** |
| :--- |

유저 게임 데이터 저장 (플레이어 이름, 데이터 키 값, 저장할 Vector 값) 
| **SaveUserGameData(String PlayerName, String KeyString, float SaveValue)** |
| :--- |

유저 게임 데이터 저장 (플레이어 이름, 데이터 키 값, 저장할 float 값) 
| **SaveUserGameData(String PlayerName, String KeyString, bool SaveValue)** |
| :--- |

유저 게임 데이터 저장 (플레이어 이름, 데이터 키 값, 저장할 Bool 값 
| **SaveUserGameData(String PlayerName, String KeyString, int SaveValue)** |
| :--- |

유저 게임 데이터 저장 (플레이어 이름, 데이터 키 값, 저장할 Int 값) 
| **SaveUserGameData(String PlayerName, String KeyString, String SaveValue)** |
| :--- |

유저 게임 데이터 저장 (플레이어 이름, 데이터 키 값, 저장할 String 값) 
| **SaveUserGameData(String PlayerName, String KeyString, Color SaveValue)** |
| :--- |

유저 게임 데이터 저장 (플레이어 이름, 데이터 키 값, 저장할 Color 값) 
| **Object GetSavedUserGameData(String PlayerName, String KeyString)** |
| :--- |

유저 게임 데이터 얻기 (플레이어 이름, 데이터 키 값) 
| **SaveGameStatisticsData(String PlayerName, String KeyString, int SaveValue, bool Overwrite, bool Ascending)** |
| :--- |

게임 통계 데이터 저장 (플레이어 이름, 데이터 키 값, 저장 값, 덮어씌우기 여부, 오름차순 정렬 여부) 
| **GetGameStatisticsData(String KeyString, bool Ascending, int Offset, int Count, LuaScriptFunction CallBack)** |
| :--- |
| **SendToClient_GameStatisticsData(String PlayerName, String KeyString, bool Ascending, int Offset, int Count)** |
| :--- |

게임 통계 데이터 클라이언트로 보내주기 (플레이어 이름, 데이터 키 값, 오름차순 정렬 여부, Offset 값, Count 값) 
| **vector<Player> GetAllPlayer()** |
| :--- |

모든 플레이어 얻기 
| **NPC CreateNPC(String NPCName, String NPCSetting, Vector Location)** |
| :--- |

NPC 생성 (NPC 이름 설정, NPC 세팅 지정, 생성 위치 Vector) 
| **DeleteNPC(String NPCName)** |
| :--- |

NPC 삭제 (삭제할 NPC 이름) 
