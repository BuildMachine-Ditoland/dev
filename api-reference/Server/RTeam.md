# **Team**

게임에서 사용될 팀을 설정 할 때 사용되는 객체에요. Game.AddTeam 함수를 이용해요. 
## **속성**

| **int MaxPlayerCount** |
| :--- |
팀 최대 인원 
## **함수**

| **AddUsingCharacter(string CharacterSetting)** |
| :--- |
팀에서 사용될 캐릭터 설정을 추가(Game에 AddCharacterSetting 함수로 추가한 캐릭터설정 중) 
| **SetUsingSpawnPointGroup(string InSpawnPointGroup)** |
| :--- |
팀에서 사용될 스폰 포인트 그룹을 추가(Game에 AddSpawnPointGroup 함수로 추가한 스폰 그룹중) 
| **AddFixedCharacter(string CharacterSetting)** |
| :--- |
팀 고정 캐릭터설정 추가(Game에 AddCharacterSetting 함수로 추가한 캐릭터설정 중) 
| **AddFixedSpawnPoint(string SpawnPoint)** |
| :--- |
팀 고정 스폰 포인트 추가(Game에 AddSpawnPoint 함수로 추가한 스폰 포인트중) 
| **ReviveTeamPlayerCharacter()** |
| :--- |
팀원중 죽어있는 캐릭터 리스폰(생명이 남아 있어야 한다) 
