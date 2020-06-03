# **RGameClient**

 **게임 전반적인 역할을 하는 객체에요. 여기 있는 기능들은 클라이언트에서만 사용할 수 있어요.** 
## **이벤트**

| **ReceiveGameStatisticsDataEvent** |
| :--- |
 **서버로 부터 게임 통계 데이터 받았을 때 이벤트** 
## **함수**

| **RModeRemotePlayer GetRemotePlayer(string PlayerName);** |
| :--- |
 **이름으로 플레이어 얻기** 
| **RModeClientCharacter GetRemotePlayerCharacter(string PlayerName)** |
| :--- |
 **해당 플레이어의 캐릭터 얻기** 
| **int GetPlayerCount** |
| :--- |
 **현재 게임에 참여한 플레이어 수 얻기** 
| **SendEventToServer(string EventName, Args ... )** |
| :--- |
 **서버에 커스텀 이벤트 보내기** 
| **RModeSequenceAnimStateSetting AddAnimStateMachineSetting(string StateMachineName)** |
| :--- |
 **캐릭터에 사용될 애니메이션 상태머신 설정 추가** 
| **RModeSequenceAnimStateSetting GetAnimStateMachineSetting(string StateMachineName)** |
| :--- |
 **설정된 애니메이션 상태머신 얻기** 
| **SetCharacterAnimStateMachine(string CharacterSettingName, string AnimStateMachineSettingName)** |
| :--- |
 **해당 캐릭터 설정, 해당 애니메이션 상태 머신 사용하게 설정** 
| **SetNPCAnimStateMachine(string NPCSettingName, string AnimStateMachineSettingName)** |
| :--- |
 **해당 NPC 설정, 해당 애니메이션 상태 머신 사용하게 설정** 
| **RModeCameraSetting AddCameraSetting(string CameraSettingName)** |
| :--- |
 **카메라 설정을 추가한다** 
| **ChangeCameraOffset(Vector Offset, float Time)** |
| :--- |
 **카메라를 주어진 Offset 값 만큼 Time(초단위) 시간안에 이동 시킨다.** 
| **ChangeCameraOffset(Vector Offset, float Time)** |
| :--- |
 **카메라를 주어진 Offset으로 Time(초단위) 시간안에 이동 시킨다.** 
| **RestoreCameraOffset(float Time)** |
| :--- |
 **원래 Offset으로 Time(초단위) 시간안에 이동 시킨다.** 
| **ObjectFXClient CreateFX(ObjectFXClient FXObject, Vetor Location)** |
| :--- |
 **FX 생성** 
| **ObjectFXClient CreateFX(String FXName, Vetor Location)** |
| :--- |
 **FX 생성** 
| **DeleteFX(ObjectFXClient Object)** |
| :--- |
 **FX 제거** 
| **ObjectSoundClient PlaySound(ObjectSoundClient SoundObject, Vetor Location)** |
| :--- |
 **사운드 플레이** 
| **ObjectSoundClient PlaySound(String SoundObjectName)** |
| :--- |
 **사운드 플레이** 
| **ObjectSoundClient PlaySound(String SoundObjectName, Vector Location)** |
| :--- |
 **사운드 플레이** 
| **StopSound(String SoundName)** |
| :--- |
 **플레이 중인 사운드 정지** 
| **CreateObject(string ObjectName, Vector Location)** |
| :--- |
 **해당 위치에 해당 월드 트리 오브젝트를 생성한다.** 
| **CreateObject(RScriptWorldObject Object, Vector Location)** |
| :--- |
 **해당 위치에 해당 월드 트리 오브젝트를 생성한다.** 
