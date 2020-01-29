# RModeServer

## **RModeServer**

**RModeGame의 자식 객체로, 서버 스크립트에 Game 으로 제공되는 객체**

## **Property**

| **var MaxUserCount** |
| :--- |
| **게임 최대 인원. 디폴트 값은 10** |

## **Function**
  
<table>
  <thead>
  <tr><td style="text-align:left">void AddUserCollisionType\(string UserCollisionType\)</td></tr>
    <tr>
      <th style="text-align:left">
        <p><b>&#xC720;&#xC800; &#xCDA9;&#xB3CC; &#xD0C0;&#xC785; &#xC124;&#xC815; &#xCD94;&#xAC00;.</b>
        </p>
        <p><b>&#xD2B9;&#xC815; &#xC624;&#xBE0C;&#xC81D;&#xD2B8;&#xC758; &#xCDA9;&#xB3CC; &#xCC98;&#xB9AC;&#xB97C; &#xB2E4;&#xB978; &#xC624;&#xBE0C;&#xC81D;&#xD2B8;&#xC640; &#xB2E4;&#xB974;&#xAC8C; &#xD560; &#xB54C; &#xC0AC;&#xC6A9;</b>
        </p>
        <p><b>&#xC608;) &#xD2B9;&#xC815; &#xC624;&#xBE0C;&#xC81D;&#xD2B8;&#xB9CC; &#xD1B5;&#xACFC;&#xD558;&#xACE0;, &#xCE90;&#xB9AD;&#xD130;&#xB294; &#xBABB; &#xD1B5;&#xACFC;&#xD558;&#xB294; &#xC624;&#xBE0C;&#xC81D;&#xD2B8;.</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>

| **RModeSpawnPointGroup AddSpawnPointGroup(string SpawnPointGroupName)** |
| :--- |
| **게임에서 사용 할 스폰 포인트 그룹을 추가한다.** |

| **RModeSpawnPoint AddSpawnPoint\(string SpawnPointName, FRObjectScript\* RObjectScript\)** |
| :--- |
| **게임에서 사용 할 스폰 포인트를 추가한다.** |

| **void SetSpawnType\(ModeSpawnType InSpawnType, string InSpawnObjectName\)** |
| :--- |
| **게임의 스폰포인트 타입을 설정한다.** |

| **void SetDefaultSpawnPos\(FVector Pos\)** |
| :--- |
| **스폰 포인트 설정이 없을 경우 스폰되는 위치 셜정** |

| **RModeCharacterSetting AddCharacterSetting\(string SettingName\)** |
| :--- |
| **게임에서 사용 할 캐릭터 설정을 추가한다.** |

| **Team AddTeam\(string TeamName\)** |
| :--- |
| **게임에서 사용 할 팀 설정을 추가한다.** |

| **Player GetPlayer\(string PlayerName\)** |
| :--- |
| **플레이어를 얻는다** |

| **RModeServerCharacter GetPlayerCharacter\(string PlayerName\)** |
| :--- |
| **플레이어의 캐릭터를 얻는다.** |

| **void SetTeamSetting\(EModeTeamType TeamType, EDivideTeamType DivideTeamType\)** |
| :--- |
| **게임의 팀전 여부, 팀 나누기 방식을 설정 한다.** |

| **number GetPlayerCount\(\)** |
| :--- |
| **현재 게임에 참여하고 있는 플레이어 수를 얻는다.** |

| **void ResetTeamSetting\(\)** |
| :--- |
| **게임의 팀 설정을 모두 없앤다.** |

| **void ApplyTeamSetting\(\)** |
| :--- |
| **게임의 팀 설정을 적용한다.** |

| **void ReqResetGame\(\)** |
| :--- |
| **게임 리셋을 요청한다.** |

| **void SetCanEnterUser\(\)** |
| :--- |
| **게임에 유저의 진입 가능 여부를 설정한다 \(false로 설정 할 경우 해당 게임으로 더 이상 유저가 진입하지 않는다\)** |

| **void BroadcastEvent\(string CustomEventName, Args ...\)** |
| :--- |
| **모든 클라이언트에게 이벤트를 보낸다.** |

| **void SendEventToClient\(string PlayerName, string CustomEventName, Args ...\)** |
| :--- |
| **해당 클라이언트에게 이벤트를 보낸다** |

| **void SetInventorySize\(int XSize, int YSize\)** |
| :--- |
| **인벤토리 사이즈 설정** |

| **void SetQuickSlotCount\(int Count\)** |
| :--- |
| **퀵 슬롯 개수 설정** |

| **void PickUpItem\(RModeServerCharacter Character, ModeItem Item\)** |
| :--- |
| **해당 케릭터가 아이템을 획득한다.** |

| **void CreateSyncObject\(string ObjectName, Vector Location\)** |
| :--- |
| **해당 위치에 클라이언트와 동기화 되는 오브젝트를 생성한다.** |

| **void CreateNoneSyncObject\(string ObjectName, Vector Location\)** |
| :--- |
| **해당 위치에 클라이언트와 동기화 되지 않는 오브젝트를 생성한다.** |

| **ObjectSpawner AddObjectSpawner\(RObjectScript RObjectScript, EObjectSelectType SpawnType, float SpawnTime, int MaxCount\)** |
| :--- |
| **오브젝트 스포너 생성한다.** |

| **ObjectSelector CreateObjectSelector\(EObjectSelectType SelectType\)** |
| :--- |
| **오브젝트 셀렉터를 생성한다.** |

| **ObjectList GetObjectList\(Vector Center, float Radius\)** |
| :--- |
| **해당 영역의 오브젝트 얻기** |

| **void UseWorldItem\(RModeServerCharacter Character, ModeItem Item\)** |
| :--- |
| **월드 아이템 사용하기** |

| **void DeleteWorldItem\(ModeItem Item\)** |
| :--- |
| **월드 아이템 삭제하기** |

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>void SaveUserGameData(String PlayerName, String KeyString, Vector SaveValue)</b>
        </p>
        <p><b>void SaveUserGameData(String PlayerName, String KeyString, float SaveValue)</b>
        </p>
        <p><b>void SaveUserGameData(String PlayerName, String KeyString, bool SaveValue)</b>
        </p>
        <p><b>void SaveUserGameData(String PlayerName, String KeyString, int SaveValue)</b>
        </p>
        <p><b>void SaveUserGameData(String PlayerName, String KeyString, String SaveValue)</b>
        </p>
        <p><b>void SaveUserGameData(String PlayerName, String KeyString, Color SaveValue)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody><tr><td style="text-align:left"><b>유저 게임 데이터 저장</b></td></tr></tbody>
</table> 

| **Object GetSavedUserGameData(String PlayerName, String KeyString)** |
| :--- |
| **유저 게임 데이터 얻기** |

| **void SaveGameStatisticsData\(String PlayerName, String KeyString, int SaveValue, bool Overwrite, bool Ascending\)** |
| :--- |
| **게임 통계 데이터 저장** |

| **void GetGameStatisticsData\(String KeyString, bool Ascending, int Offset, int Count, LuaScriptFunction CallBack\)** |
| :--- |
| **게임 통계 데이터 얻기** |

| **void SendToClient\_GameStatisticsData\(String PlayerName, String KeyString, bool Ascending, int Offset, int Count\)** |
| :--- |
| **게임 통계 데이터 클라이언트로 보내주기** |

| **vector&lt;Player&gt; GetAllPlayer\(\)** |
| :--- |
| **모든 플레이어 얻기** |

