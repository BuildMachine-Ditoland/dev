# RModeAnimStateMachineSetting

### **RModeAnimStateMachineSetting**

**게임에 사용되는 애니매이션 상태머신을 설정하는 객체. Game.AddAnimStateMachineSetting 로 생성**  


### **Function**

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
  <tbody>
    <tr>
      <td style="text-align:left"><b>&#xB2E8;&#xC77C; &#xC560;&#xB2C8;&#xBA54;&#xC774;&#xC158; &#xC0C1;&#xD0DC; &#xC124;&#xC815; &#xCD94;&#xAC00;</b>
      </td>
    </tr>
  </tbody>
</table><table>
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
  <tbody>
    <tr>
      <td style="text-align:left"><b>&#xBE14;&#xB79C;&#xB4DC; &#xC560;&#xB2C8;&#xBA54;&#xC774;&#xC158; &#xC0C1;&#xD0DC; &#xC124;&#xC815; &#xCD94;&#xAC00;</b>
      </td>
    </tr>
  </tbody>
</table><table>
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
  <tbody>
    <tr>
      <td style="text-align:left"><b>&#xC560;&#xB2C8;&#xBA54;&#xC774;&#xC158; &#xC0C1;&#xD0DC; &#xC804;&#xC774; &#xC124;&#xC815; &#xCD94;&#xAC00;</b>
      </td>
    </tr>
  </tbody>
</table>| **void SetStartState\(string StateName** |
| :--- |
| **애니메이션 상태머신이 활성화 될 때 시작 애니메이션 상태 설정** |







