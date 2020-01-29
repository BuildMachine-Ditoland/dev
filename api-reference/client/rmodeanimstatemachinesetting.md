# RModeAnimStateMachineSetting

## **RModeAnimStateMachineSetting**

**게임에 사용되는 애니매이션 상태머신을 설정하는 객체.**
**Game.AddAnimStateMachineSetting 로 생성**

## **Function**

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>RModeSequenceAnimStateSetting AddAnimState(string StateName, string ResourceID)</b>
        </p>
        <p><b>RModeSequenceAnimStateSetting AddAnimState(string StateName, string ResourceID, int PlayCount)</b>
        </p>
        <p><b>RModeSequenceAnimStateSetting AddAnimState(string StateName, string ResourceID, int PlayCount, float PlaySpeed)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody><tr><td style="text-align:left"><b>단일 애니메이션 상태 설정 추가</b></td></tr></tbody>
</table> 

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>RModeBlendAnimStateSetting AddBlendAnimState(string StateName, protected_function BlendFunction)</b>
        </p>
        <p><b>RModeBlendAnimStateSetting AddBlendAnimState(string StateName, protected_function BlendFunction, int PlayCount)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody><tr><td style="text-align:left"><b>블랜드 애니메이션 상태 설정 추가</b></td></tr></tbody>
</table> 

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>void AddAnimTransition(string FromState, string ToState)</b>
        </p>
        <p><b>void AddAnimTransition(string FromState, string ToState, float BlendTime)</b>
        </p>
        <p><b>void AddAnimTransition(string FromState, string ToState, protected_function Condition)</b>
        </p>
        <p><b>void AddAnimTransition(string FromState, string ToState, protected_function Condition, float BlendTime)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody><tr><td style="text-align:left"><b>애니메이션 상태 전이 설정 추가</b></td></tr></tbody>
</table>

| **void SetStartState(string StateName** |
| :--- |
| **애니메이션 상태머신이 활성화 될 때 시작 애니메이션 상태 설정** |

