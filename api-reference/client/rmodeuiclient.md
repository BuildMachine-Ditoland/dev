# RModeUIClient

## **RModeUIClient**

**클라이언트에서 UI를 제어하는 객체, 서비스로 제공되며 스크립트에서 UI로 참조 가능하다.**

## \*\*\*\*

## **Function**

| **RModeUIScene GetUIScene\(string UISceneName\)** |
| :--- |
| **이름으로 UI 페이지 얻기** |

| **void SetVisible\(string UISceneName, bool bVisible\)** |
| :--- |
| **이름에 해당되는 UI페이지의 가시성 설정** |

| **bool IsShow\(\)** |
| :--- |
| **UI 가시성 확인** |

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>void SetText(string UISceneName, string TextName, int Value)</b>
        </p>
        <p><b>void SetText(string UISceneName, string TextName, float Value)</b>
        </p>
        <p><b>void SetText(string UISceneName, string TextName, string InText)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>&#xC774;&#xB984;&#xC5D0; &#xD574;&#xB2F9;&#xB418;&#xB294; UI&#xD398;&#xC774;&#xC9C0;&#xC758; &#xC704;&#xC82F; &#xD14D;&#xC2A4;&#xD2B8; &#xC124;&#xC815;</b>
      </td>
    </tr>
  </tbody>
</table>\| \*\*void SetChangeTextEvent\\(string UISceneName, string TextName, protected\\_function InEventFunction\\)\*\* \| \| :--- \| \| \*\*이름에 해당되는 UI페이지의 위젯의 텍스트 변경 시 호출되는 이벤트 함수 설정\*\* \| \| \*\*void SetImage\\(string UISceneName, string ImgName, string Img\\)\*\* \| \| :--- \| \| \*\*이름에 해당되는 UI페이지의 위젯 이미지 설정\*\* \| \| \*\*void SetChangeImageEvent\\(string UISceneName, string ImgName, protected\\_function InEventFunction\\)\*\* \| \| :--- \| \| \*\*이름에 해당되는 UI페이지 위젯의 이미지 변경 시 호출되는 이벤트 함수 설정\*\* \| \| \*\*void SetButtonUpEvent\\(string UISceneName, string ButtonName, protected\\_function InEventFunction\\)\*\* \| \| :--- \| \| \*\*이름에 해당되는 UI페이지 버튼 위젯이 눌렸다 띄어질 때 호출되는 이벤트 함수 설정\*\* \| \| \*\*void SetButtonPressEvent\\(string UISceneName, string ButtonName, protected\\_function InEventFunction\\)\*\* \| \| :--- \| \| \*\*이름에 해당되는 UI페이지 버튼 위젯이 눌릴 때 호출되는 이벤트 함수 설정\*\* \| \| \*\*RModeUIScene CreateModeUIScene\\(string UISceneName\\)\*\* \| \| :--- \| \| \*\*이름에 해당되는 이름을 갖는 UI 페이지 생성\\(현재 작동하지 않음\\)\*\* \|

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>void AddChildUIScene(string ParentUISceneName, string UIName, string UISceneName)</b>
        </p>
        <p><b>void AddChildUIScene(string ParentUISceneName, string ParentWidgetName, string UIName, string UISceneName)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>&#xC774;&#xB984;&#xC5D0; &#xD574;&#xB2F9;&#xB418;&#xB294; UI&#xD398;&#xC774;&#xC9C0; &#xC2A4;&#xD06C;&#xB864; &#xC704;&#xC82F;&#xC5D0; &#xC790;&#xC2DD; &#xC704;&#xC82F; &#xCD94;&#xAC00;</b>
      </td>
    </tr>
  </tbody>
</table><table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>RModeUIScene GetChildUIScene(string ParentUISceneName, string UIName)</b>
        </p>
        <p><b>RModeUIScene GetChildUIScene(string ParentUISceneName, string ParentWidgetName, string UIName)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>&#xC774;&#xB984;&#xC5D0; &#xD574;&#xB2F9;&#xB418;&#xB294; UI&#xD398;&#xC774;&#xC9C0; &#xC2A4;&#xD06C;&#xB864; &#xC704;&#xC82F;&#xC758; &#xC790;&#xC2DD; &#xC704;&#xC82F; &#xC5BB;&#xAE30;</b>
      </td>
    </tr>
  </tbody>
</table>