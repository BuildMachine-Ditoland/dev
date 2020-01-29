# RModeClientCharacter

## **RModeClientCharacter**

**클라이언트에서 사용되는 플레이어의 캐릭터 객체로 애니메이션 관련 기능을 설정 할 수 있다.**

## **Function**

| **GetPlayerName\(\)** |
| :--- |
| **플레이어 이름 얻기** |

| **FRModeAnimStateMachine AddAnimStateMachine\(string StateMachineName\)** |
| :--- |
| **애니메이션 상태 머신 추가. \(Game.AddAnimStateMachineSetting 함수로 추가된 상태머신 중\)** |

| **FRModeAnimStateMachine GetAnimStateMachine\(string StateMachineName\)** |
| :--- |
| **해당 애니메이션 상태 머신 얻기** |

| **RModeAnimStateBase GetCurAnimState\(\)** |
| :--- |
| **현재 애니메이션 상태 얻기** |

| **void ChangeAnimState\(string AnimState\)** |
| :--- |
| **해당 애니메이션 상태로 변경** |

| **void ChangeAnimStateMachine\(string ChangeStateMacnine\)** |
| :--- |
| **해당 애니메이션 상태 머신 변경** |

| **bool IsFly\(\)** |
| :--- |
| **캐릭터가 공중에 떠 있는가?** |

| **float GetMoveSpeed\(\)** |
| :--- |
| **현재 이동 속도 얻기** |

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>ObjectFXClient CreateFX(ObjectFXClient FXObject, Bone BoneType)</b>
        </p>
        <p><b>ObjectFXClient CreateFX(String FXName, Bone BoneType)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody><tr><td style="text-align:left">캐릭터 특정 위치에 FX 생성</td></tr></tbody>
</table>  

| **ObjectSoundClient CreateSound(ObjectSoundClient SoundObject)** |
| :--- |
| **캐릭터의 위치에 Sound 생성** |

| **void AddPlayerHUD\(string UIName\)** |
| :--- |
| **UI HUD 붙이기** |

| **void RemovePlayerHUD\(string UIName\)** |
| :--- |
| **UI HUD 제거하기** |

| **void GetPlayerHUD\(string UIName\)** |
| :--- |
| **UI HUD 얻기** |

| **bool IsMyCharacter\(\)** |
| :--- |
| **플레이어 자신의 캐릭터인지 확인** |

| **Vector GetLocation\(\)** |
| :--- |
| **현재 캐릭터 위치 얻기** |

