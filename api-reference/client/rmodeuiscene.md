# RModeUIScene

### **RModeUIScene**

**클라이언트에서 보여지는 UI페이지이며, 설정되어 있는 위젯 객체를 제어하는 객체**  


### **Property**

| **var InitEvent** |
| :--- |
|  **UI가 초기화 되었을 때 호출되는 이벤트 객체** |

| **var VisibleEvent** |
| :--- |
| **UI가 보여질 때 호출되는 이벤트 객체** |

| **var UpdateEvent** |
| :--- |
| **UI가 보여지는 동안 호출되는 이벤트 객체** |

| **var InVisibleEvent** |
| :--- |
| **UI가 안 보여질 때 호출되는 이벤트 객체** |

### \*\*\*\*

### **Function**

| **void SetVisible\(bool bVisible\)** |
| :--- |
| **UI 가시성 설정** |

| **void SetWidgetVisible\(const std::string&WidgetName, bool bVisible\)** |
| :--- |
| **UI 위젯 가시성 설정** |

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>void SetText(string WidgetName, int Value)</b>
        </p>
        <p><b>void SetText(string WidgetName, float Value)</b>
        </p>
        <p><b>void SetText(string WidgetName, string InText)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>&#xC704;&#xC82F;&#xC758; &#xD14D;&#xC2A4;&#xD2B8; &#xC124;&#xC815;</b>
      </td>
    </tr>
  </tbody>
</table>| **void SetTextColor\(string WidgetName, Color color\)** |
| :--- |
| **텍스트 색 설정** |

| **void SetChangeTextEvent\(string TextName, protected\_function InEventFunction\)** |
| :--- |
| **위젯의 텍스트 변경 시 호출되는 이벤트 함수 설정** |

| **void SetImage\(string ImgName, ResoureID TextureID\)** |
| :--- |
| **위젯의 이미지 변경** |

| **void SetChangeImageEvent\(string ImgName, protected\_function InEventFunction\)** |
| :--- |
| **위젯의 이미지 변경 시 호출되는 이벤트 함수 설정** |

| **void SetButtonUpEvent\(string ButtonName, protected\_function InEventFunction\)** |
| :--- |
| **버튼 위젯이 눌렸다 띄어질 때 호출되는 이벤트 함수 설정** |

| **void SetButtonPressEvent\(string ButtonName, protected\_function InEventFunction\)** |
| :--- |
| **버튼 위젯이 눌릴 때 호출되는 이벤트 함수 설정** |

| **void SetWidgetLocation\(string WidgetName, float X, float Y\)** |
| :--- |
| **위젯의 위치 변경** |

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>void AddChildUIScene(string ChildUISceneName, FRModeUIScene* Element)</b>
        </p>
        <p><b>void AddChildUIScene(string ParentWidgetName, string ChildUISceneName, FRModeUIScene* Element)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>&#xC2A4;&#xD06C;&#xB864; &#xC704;&#xC82F;&#xC5D0; &#xC790;&#xC2DD; &#xC704;&#xC82F; &#xCD94;&#xAC00;</b>
      </td>
    </tr>
  </tbody>
</table><table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p><b>RModeUIScene GetChildUIScene(string ChildUISceneName)</b>
        </p>
        <p><b>RModeUIScene GetChildUIScene(string ParentWidgetName, string ChildUISceneName)</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>&#xC2A4;&#xD06C;&#xB864; &#xC704;&#xC82F;&#xC758; &#xC790;&#xC2DD; &#xC704;&#xC82F; &#xC5BB;&#xAE30;</b>
      </td>
    </tr>
  </tbody>
</table>| **String GetText\(string WidgetName\)** |
| :--- |
| **텍스트 내용 얻기** |

| **String IsFrameVisible** |
| :--- |
| **위젯 가시성 확인** |

