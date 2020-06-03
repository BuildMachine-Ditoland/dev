# **RScriptObject**

| **스크립트로 제공되는 기본 객체** |
## **속성**

| **Parent** |
| :--- |
| **부모 오브젝트** |
## **이벤트**

| **ConnectChangeEventFunction(string ValueName, function FunctionName)** |
| :--- |
| **추가된 값이 변경 될 때 호출되는 이벤트** |
## **샘플**

```lua
local function EnterPlayer (Player)
	Logger:Log(“Hello”)
end

-- Game.OnEnterPlayer가 RModeEventFunction을 리턴
Game.OnEnterPlayer:Connect(EnterPlayer)	 
```
## **함수**

| **string GetName()** |
| :--- |
| **이름 얻기** |
| **RModeObject GetParent(string ParentName)** |
| :--- |
| **부모 객체 얻기** |
| **RModeObject GetChild(string ChildName)** |
| :--- |
| **이름으로 자식 객체 얻기** |
| **RModeObject GetGetSibling(string Name)** |
| :--- |
| **이름으로 형제 객체 얻기** |
| **AddReplicateValue(string ValueName, Vector Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |
| **해당 객체에 서버, 클라이언트 간 동기화 기능이 있는 벡터를 추가** |
| **AddReplicateValue(string ValueName, float Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |
| **해당 객체에 서버, 클라이언트 간 동기화 기능이 있는 실수를 추가** |
| **AddReplicateValue(string ValueName, bool Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |
| **해당 객체에 서버, 클라이언트 간 동기화 기능이 있는 bool를 추가** |
| **AddReplicateValue(string ValueName, string Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |
| **해당 객체에 서버, 클라이언트 간 동기화 기능이 있는 문자열을 추가** |
| **AddReplicateValue(string ValueName, Color Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |
| **해당 객체에 서버, 클라이언트 간 동기화 기능이 있는 칼라를 추가** |
| **AddSaveValue(string ValueName, Vector Data)** |
| :--- |
| **해당 객체 저장소에 벡터를 추가** |
| **AddSaveValue(string ValueName, float Data)** |
| :--- |
| **해당 객체 저장소에 실수를 추가** |
| **AddSaveValue(string ValueName, bool Data)** |
| :--- |
| **해당 객체 저장소에 bool을 추가** |
| **AddSaveValue(string ValueName, string Data)** |
| :--- |
| **해당 객체 저장소에 문자열을 추가** |
| **AddSaveValue(string ValueName, Color Data)** |
| :--- |
| **해당 객체 저장소에 칼라를 추가** |
