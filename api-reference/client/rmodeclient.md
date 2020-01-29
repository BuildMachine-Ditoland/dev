# RModeClient

## **RModeClient**

**RModeGame의 자식 객체로, 클라이언트 스크립트에서 Game 로 제공되는 객체**


## **Property**

| **var ReceiveGameStatisticsDataEvent** |
| :--- |
| **서버로 부터 게임 통계 데이터 받았을 때 이벤트** |


## **Function**

| **RModeRemotePlayer GetRemotePlayer\(string PlayerName\);** |
| :--- |
| **이름으로 플레이어 얻기** |

| **RModeClientCharacter GetRemotePlayerCharacter\(string PlayerName\)** |
| :--- |
| **해당 플레이어의 캐릭터 얻기** |

| **number GetPlayerCount\(\)** |
| :--- |
| **현재 게임에 참여한 플레이어 수 얻기** |

| **void SendEventToServer\(string EventName, Args ... \)** |
| :--- |
| **서버에 커스텀 이벤트 보내기** |

| **RModeSequenceAnimStateSetting AddAnimStateMachineSetting\(string StateMachineName\)** |
| :--- |
| **캐릭터에 사용 될 애니메이션 상태머신 설정 추가** |

| **RModeSequenceAnimStateSetting GetAnimStateMachineSetting\(string StateMachineName\)** |
| :--- |
| **설정된 애니메이션 상태머신 얻기** |

| **void SetCharacterAnimStateMachine\(string CharacterSettingName, string AnimStateMachineSettingName\)** |
| :--- |
| **해당 캐릭터 설정, 해당 애니메이션 상태 머신 사용하게 설정** |

| **void AddCameraSetting\(String CameraSettingName\)** |
| :--- |
| **캐릭터에 설정 할 수 있는 카메라 설정을 추가한다** |

| **void ChangeCameraOffset\(Vector Offset, float Time\)** |
| :--- |
| **카메라를 주어진 Offset 값 만큼 Time\(초단위\) 시간안에 이동 시킨다.** |

| **void RestoreCameraOffset\(float Time\)** |
| :--- |
| **원래 Offset으로 Time\(초단위\) 시간안에 이동 시킨다.** |

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>ObjectFXClient CreateFX(ObjectFXClient FXObject, Vetor Location)</b>
        </p>
        <p><b>ObjectFXClient CreateFX(String FXName, Vetor Location)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody><tr><td style="text-align:left">FX 생성</td></tr></tbody>
</table> 

| **void DeleteFX(ObjectFXClient Object)** |
| :--- |
| **FX 제거** | 

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>ObjectSoundClient PlaySound(ObjectSoundClient SoundObject, Vetor Location)</b>
        </p>
        <p><b>ObjectSoundClient PlaySound(String SoundObjectName)</b>
        </p>
        <p><b>ObjectSoundClient PlaySound(String SoundObjectName, Vector Location)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody><tr><td style="text-align:left">사운드 플레이</td></tr></tbody>
</table>  

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>void StopSound(String SoundName)</b>
        </p>
        <p><b>void StopSound(ObjectSoundClient Object)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody><tr><td style="text-align:left">플레이 중인 사운드 정지</td></tr></tbody>
</table>  

| **void CreateObject(string ObjectName, Vector Location)** |
| :--- |
| **해당 위치에 해당 월드 트리 오브젝트를 생성한다** | 

