# **RScriptGame**

스크립트 게임 객체에요. 
## **이벤트**

| **OnUpdateEvent** |
| :--- |
매 프레임 호출되는 이벤트 
| **OnEnterPlayer** |
| :--- |
플레이어 진입 시 호출되는 이벤트 
| **OnLeavePlayer** |
| :--- |
플레이어 나갈 때 호출되는 이벤트 
| **OnDeathCharacter** |
| :--- |
케릭터 죽을 때 호출되는 이벤트 
| **OnSpawnCharacter** |
| :--- |
케릭터 스폰 될 때 호출되는 이벤트 
## **함수**

| **RModePhase AddPhase(string phasename)** |
| :--- |
게임에 단계를 추가한다. (단계 이름) 
| **RModePhase GetPhaseByName(string phasename)** |
| :--- |
단계 이름으로 단계 가져오기 (단계 이름) 
| **RModePhase GetCurPhase()** |
| :--- |
현재 단계 가져오기 
| **RModePhase ChangePhaseByName(string changephasename)** |
| :--- |
이름으로 단계 변경하기 (변경할 단계 이름) 
| **RModePhase ChangeToNextPhase()** |
| :--- |
다음 단계로 변경하기. 
| **ConnectEventFunction(string customevent, LuaScriptFunction function) ** |
| :--- |
유저가 추가하는 이벤트(이벤트 이름, 연결 함수) 
| **float GetPassTime()** |
| :--- |
진행된 시간 얻기 
| **DeleteObject(RScriptWorldObject)** |
| :--- |
오브젝트 삭제하기 (오브젝트) 
