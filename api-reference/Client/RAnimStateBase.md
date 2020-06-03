# **RAnimStateBase**

 **애니메이션 상태(단일, 블랜드)의 부모 객체에요.** 
## **이벤트**

| **EnterEvent** |
| :--- |
 **해당 애니메이션 상태로 변경 될 때 호출되는 이벤트** 
| **UpdateEvent** |
| :--- |
 **해당 애니메이션 상태 일 때 호출되는 이벤트** 
| **ExitEvent** |
| :--- |
 **해당 애니메이션에서 다른 상태로 변경 될 때 호출되는 이벤트** 
## **함수**

| **string GetName()** |
| :--- |
 **이름 얻기** 
| **float GetPlayTime()** |
| :--- |
 **애니메이션 상태 플레이 시간 얻기** 
| **AddTransition(RModeAnimTransition InTransition)** |
| :--- |
 **다른 애니메이션 상태로의 전이 추가** 
| **RModeClientCharacter GetOwnerCharacter()** |
| :--- |
 **설정되어 있는 캐릭터 얻기** 
| **SetNeedReplicate(bool NeedReplicate)** |
| :--- |
 **동기화 필요 여부 설정** 
