# RModeRemotePlayer

## **RModeRemotePlayer**

**클라이언트 스크립트에서 사용되는 플레이어 객체. Game.GetRemotePlayer\(string PlayerName\) 함수를 이용.**



## **Function**

| **RModeClientCharacter GetCharacter\(\)** |
| :--- |
| **플레이어의 캐릭터를 얻기** |

| **string GetPlayerName\(\)** |
| :--- |
| **플레이어의 이름 얻기** |

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>ObjectFXClient CreateFX(ObjectFXClient FXObject, Bone BoneType) </b> </p>
        <p><b>ObjectFXClient CreateFX(String FXName, Bone BoneType)</b> </p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>캐릭터 특정 위치에 FX 생성</b>
      </td>
    </tr>
  </tbody>
</table>

| **ObjectSoundClient CreateSound(ObjectSoundClient SoundObject)** |
| :--- |
| **캐릭터의 위치에 Sound 생성** |

| **RModeHitResult LineTrace\(Vector Start, Vector Dir, float Distance\)** |
| :--- |
| **두지점 간의 오브젝트 충돌 체크** |

| **bool IsMyPlayer\(\)** |
| :--- |
| **플레이어 자신의 플레이어인지 확인** |

