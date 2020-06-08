# **Team**


게임에서 사용될 팀을 설정 할 때 사용되는 객체에요. [RGameServer](https://ditoland-utplus.gitbook.io/ditoland/api-reference/server/rgameserver#undefined-1)의 Game:AddTeam 함수를 이용해요. 
## **속성**

| **int MaxPlayerCount** |
| :--- |

팀 최대 인원 
## **함수**

| **AddUsingCharacter(string CharacterSetting)** |
| :--- |

팀에서 사용될 캐릭터 설정을 추가 (캐릭터세팅 이름) 

Game:AddCharacterSetting으로 추가한 캐릭터설정 중에서만 가능해요 
| **SetUsingSpawnPointGroup(string InSpawnPointGroup)** |
| :--- |

팀에서 사용될 스폰 포인트 그룹을 추가 (스폰 그룹 이름) 

Game:AddSpawnPointGroup으로 추가한 스폰 그룹 중에서만 가능해요 
| **AddFixedCharacter(string CharacterSetting)** |
| :--- |

팀 고정 캐릭터설정 추가 (캐릭터 세팅 이름) 

Game:AddCharacterSetting으로 추가한 캐릭터설정 중에서만 가능해요 
| **AddFixedSpawnPoint(string SpawnPoint)** |
| :--- |

팀 고정 스폰 포인트 추가(Game에 AddSpawnPoint 함수로 추가한 스폰 포인트중) 
| **ReviveTeamPlayerCharacter()** |
| :--- |

팀원중 죽어있는 캐릭터 리스폰 시킨다. 

Life가 남아있어야 해요 
