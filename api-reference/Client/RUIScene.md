# **RUIScene**

 **클라이언트에서 보여지는 UI페이지이며, 설정되어 있는 위젯 객체를 제어하는 객체에요.** 
# **이벤트**

| ### **OnInitEvent** |
| :--- |
 **UI가 초기화 되었을 때 호출되는 이벤트** 
| ### **OnVisibleEvent** |
| :--- |
 **UI가 보여질 때 호출되는 이벤트** 
| ### **OnUpdateEvent** |
| :--- |
 **UI가 보여지는 동안 호출되는 이벤트** 
| ### **OnInVisibleEvent** |
| :--- |
 **UI가 안 보여질 때 호출되는 이벤트 객체** 
## **함수**

| **SetVisible(bool bVisible)** |
| :--- |
 **UI의 표시 여부를 설정** 
| **SetWidgetVisible(string WidgetName, bool bVisible)** |
| :--- |
 **UI 위젯의 표시 여부를 설정** 
| **SetWidgetAnchor(string WidgetName, ERObjectUIAnchorType type)** |
| :--- |
 **UI 위젯의 표시 여부를 설정** 
| **SetWidgetOpacity(string WidgetName, float Opacity)** |
| :--- |
 **UI 위젯의 표시 여부를 설정** 
| **SetText(string WidgetName, int Value)** |
| :--- |
 **위젯의 정수 값으로 텍스트 설정** 
| **SetText(string WidgetName, float Value)** |
| :--- |
 **위젯의 실수 값으로 텍스트 설정** 
| **SetText(string WidgetName, string InText)** |
| :--- |
 **위젯의 문자열로 텍스트 설정** 
| **SetTextColor(string WidgetName, Color color)** |
| :--- |
 **텍스트 색 설정** 
| **SetChangeTextEvent(string TextName, protected_function InEventFunction)** |
| :--- |
 **위젯의 텍스트 변경 시 호출되는 이벤트 함수 설정** 
| **SetImage(string ImgName, ResoureID TextureID)** |
| :--- |
 **위젯의 이미지 설정** 
| **SetChangeImageEvent(string ImgName, protected_function InEventFunction)** |
| :--- |
 **위젯의 이미지 변경 시 호출되는 이벤트 함수 설정** 
| **SetButtonUpEvent(string ButtonName, protected_function InEventFunction)** |
| :--- |
 **버튼 위젯이 눌렸다 띄어질 때 호출되는 이벤트 함수 설정** 
| **SetButtonPressEvent(string ButtonName, protected_function InEventFunction)** |
| :--- |
 **버튼 위젯이 눌릴 때 호출되는 이벤트 함수 설정** 
| **SetWidgetLocation(string WidgetName, float X, float Y)** |
| :--- |
 **위젯의 위치 변경** 
| **AddChildUIScene(string ChildUISceneName, FRUIScene* Element)** |
| :--- |
 **UI씬에 자식 UI씬 추가** 
| **AddChildUIScene(string ParentWidgetName, string ChildUISceneName, FRUIScene* Element)** |
| :--- |
 **UI씬에 자식 UI씬 추가** 
| **RModeUIScene GetChildUIScene(string ChildUISceneName)** |
| :--- |
 **스크롤 위젯의 자식 위젯 얻기** 
| **RModeUIScene GetChildUIScene(string ParentWidgetName, string ChildUISceneName)** |
| :--- |
 **스크롤 위젯의 자식 위젯 얻기** 
| **string GetText(string WidgetName)** |
| :--- |
 **텍스트 내용 얻기** 
| **bool IsWidgetVisible(string WidgetName)** |
| :--- |
 **위젯이 보이는지를 나타낸다.** 
| **AddUIMove(string WidgetName, string TrackName, Vector Pos, float Time)** |
| :--- |
 **해당 Scene에 WidgetName을 이름으로 가진 위젯의 이동 변화를 추가한다.** 
| **AddWorldRot(string WidgetName, string TrackName, FVector Rot, float Time)** |
| :--- |
 **해당 Scene에 WidgetName을 이름으로 가진 위젯의 회전 변화를 추가한다.** 
| **AddUIScale(string WidgetName, string TrackName, FVector Size, float Time)** |
| :--- |
 **해당 Scene에 WidgetName을 이름으로 가진 위젯의 크기 변화를 추가한다.** 
| **AddUIOpacity(string WidgetName, string TrackName, float opacity, float Time)** |
| :--- |
 **해당 Scene에 WidgetName을 이름으로 가진 위젯의 투명도 변화를 추가한다.** 
| **AddUIEmpty(string TrackName, string TrackName, float Time)** |
| :--- |
 **해당 Scene에 WidgetName을 이름으로 가진 위젯의 변환에 대기 시간을 추가한다.** 
| **PlayUIActionTrack(string TrackName, TransformPlayType Type, int PlayCount)** |
| :--- |
 **설정된 변환 컨트롤러 실행** 
| **StopUIActionTrack(string TrackName)** |
| :--- |
 **변환 컨트롤러 정지** 
| **PauseUIActionTrack(string TrackName)** |
| :--- |
 **변환 컨트롤러 일시 정지** 
| **ResumeUIActionTrack(string TrackName)** |
| :--- |
 **변환 컨트롤러 다시 플레이** 
| **IsPlayingUIActionTrack(string TrackName)** |
| :--- |
 **해당 TransformTrack이 플레이 중인지 확인** 
| **ResetUIActionTrack(string TrackName)** |
| :--- |
 **해당 TransformTrack 리셋(적용되기 전의 Transform 으로 설정)** 
| **RemoveUIActionTrack(String TrackName)** |
| :--- |
 **해당 Track 제거** 
| **ResetUIActionTrack()** |
| :--- |
 **TransformTrack 이 적용되기 전의 최초 Transform으로 설정** 
