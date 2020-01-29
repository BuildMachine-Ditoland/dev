# RModeLocalPlayer

## **RModeLocalPlayer**

**게임에서 인풋 설정 및 캐릭터의 기본 동작을 설정 할 수 있는 객체. 서비스로 제공됨 스크립트에서 LocalPlayer로 참조 가능**

 

## **Property**

| **var OnChangedInventoryItem** |
| :--- |
| **인벤토리 아이템 변화 시 호출되는 이벤트** |
 

## **Function**

| **void ProcessInputAxisEvent\(string Event, protected\_function ProcessFunc\)** |
| :--- |
| **축 인풋 이벤트 설정** |

| **void ProcessInputActionEvent\(string Event, RModeInputType InputType, protected\_function ProcessFunc\)** |
| :--- |
| **키 인풋 이벤트 설정** |

| **void Move\(FVector Dir, float Value\)** |
| :--- |
| **설정된 이동 타입에 상관없이 주어진 방향으로 일정 값만큼 캐릭터 이동** |

| **void MoveForward\(float Value\)** |
| :--- |
| **설정된 이동 타입에 따른 앞으로 이동** |

| **void Turn\(float Value\)** |
| :--- |
| **캐릭터의 바라보는 좌우 방향 설정** |

| **void LookUp\(float Value\)** |
| :--- |
| **캐릭터의 바라보는 상하 방향 설정** |

<table>
  <tbody>
    <tr>
        <td style="text-align:left"><b>void SetForwardMoveType(ForwardMoveType Type)</b></td>
    </tr>
    <tr>
      <td style="text-align:left">
        <p><b>ForwardMoveType::XYPlane - &#xC0C1;, &#xD558; &#xC774;&#xB3D9;&#xB418;&#xC9C0; &#xC54A;&#xB294; &#xD3C9;&#xBA74; &#xC774;&#xB3D9;(&#xC77C;&#xBC18; &#xC801;&#xC778; &#xCE90;&#xB9AD;&#xD130;&#xC758; &#xC774;&#xB3D9; &#xD615;&#xD0DC;)</b>
        </p>
        <p><b>ForwardMoveType::Free - &#xCE90;&#xB9AD;&#xD130;&#xAC00; &#xBC14;&#xB77C;&#xBCF4;&#xB294; &#xBC29;&#xD5A5;&#xC73C;&#xB85C; &#xC774;&#xB3D9;(&#xD504;&#xB9AC; &#xCE74;&#xBA54;&#xB77C;&#xC758; &#xC774;&#xB3D9; &#xD615;&#xD0DC;)</b>
        </p>
        <p><b>ForwardMoveType::UpDown - &#xC0C1;, &#xD558;&#xB85C;&#xB9CC; &#xC774;&#xB3D9;(&#xC5D8;&#xB9AC;&#xBCA0;&#xC774;&#xD130;, &#xC0AC;&#xB2E4;&#xB9AC;&#xC758; &#xC774;&#xB3D9; &#xD615;&#xD0DC;)</b>
        </p>
      </td>
    </tr>
     <tr>
        <td style="text-align:left"><b>MoveForward\(float Value\)의 작동 방식 설정</b>  </td>
     </tr>
  </tbody> 
</table> 

| **void FreeCamMoveUp(float Value)** |
| :--- |
| **FreeCamMoveUp(float Value) 프리캠 위, 아래로 이동** |

| **FVector GetForwardVector\(\)** |
| :--- |
| **바라보는 방향 얻기** |

| **FVector GetRightVector\(\)** |
| :--- |
| **오른쪽 방향 얻기** |

| **RModeRemotePlayer GetRemotePlayer\(\)** |
| :--- |
| **자신의 플레이어 얻기** |

| **int GetInventorySize\(\)** |
| :--- |
| **인벤토리 사이즈 얻기** |

| **void UseInventoryItem\(int IventoryIndex\)** |
| :--- |
| **인벤토리 아이템 사용** |

| **void EquipInventoryItem\(int IventoryIndex\)** |
| :--- |
| **인벤토리 아이템 착용** |

| **void UnEquipItem\(string EquipSlotName\)** |
| :--- |
| **착용 아이템 해지** |

| **void UnEquipItem\(string EquipSlotName, string ActionName\)** |
| :--- |
| **착용 아이템 액션** |

| **void WorldDropInventoryItem\(int InventoryIndex\)** |
| :--- |
| **인벤토리 아이템 월드 드랍** |

