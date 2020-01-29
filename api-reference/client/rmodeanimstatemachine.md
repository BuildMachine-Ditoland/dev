# RModeAnimStateMachine

## **RModeAnimStateMachine**

**애니메이션 상태 머신. RModeClientCharacter 의 AddAnimStateMachine 함수로 생성 가능.**

**Game.AddAnimStateMachineSetting 로 상태머신 설정한 후 Game.SetCharacterAnimStateMachine 로 해당 애니메이션 상태머신을**

**사용 할 캐릭터 셋팅을 설정하면, 해당 캐릭터 셋팅으로 캐릭터 생성 될 때 해당 애니메이션 상태머신이 설정 됨.**

## **Function**

| **string GetName\(\)** |
| :--- |
| **애니메이션 상태 머신 이름 얻기** |

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>RModeSequenceAnimState* AddAnimState(string StateName, string ResourceID)</b>
        </p>
        <p><b>RModeSequenceAnimState* AddAnimState(string StateName, string ResourceID, int PlayCount)</b>
        </p>
        <p><b>RModeSequenceAnimState* AddAnimState(string StateName, string ResourceID, int Playcount, float PlaySpeed)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>| **단일 애니메이션을 플레이하는 애니메이션 상태 추가** |
| :--- |


<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>RModeBlendAnimState AddBlendAnimState(string StateName, protected_function BlendFunction)</b>
        </p>
        <p><b>RModeBlendAnimState AddBlendAnimState(string StateName, protected_function BlendFunction, int PlayCount)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>| **블랜드 애니메이션 상태 추가** |
| :--- |


<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>void AddTransition(string FromState, string ToState)</b>
        </p>
        <p><b>void AddTransition(string FromState, string ToState, float BlendTime)</b>
        </p>
        <p><b>void AddTransition(string FromState, string ToState, protected_function Condition)</b>
        </p>
        <p><b>void AddTransition(string FromState, string ToState, protected_function Condition, float BlendTime)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>| **애니메이션 상태 전이 추가** |
| :--- |


<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>void AddTransition(string FromState, string ToState)</b>
        </p>
        <p><b>void AddTransition(string FromState, string ToState, float BlendTime)</b>
        </p>
        <p><b>void AddTransition(string FromState, string ToState, protected_function Condition)</b>
        </p>
        <p><b>void AddTransition(string FromState, string ToState, protected_function Condition, float BlendTime)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody></tbody>
</table>| **애니메이션 상태 전이 추가** |
| :--- |


| **void ChangeAnimStateDirect\_ForScript\(string ChangeStateName\)** |
| :--- |
| **해당 애니메이션 상태로 전이** |

