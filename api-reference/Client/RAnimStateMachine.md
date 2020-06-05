# **RAnimStateMachine**

애니메이션 상태 머신이에요. RGameClientCharacter 의 AddAnimStateMachine 함수로 생성 가능해요. 
Game.AddAnimStateMachineSetting 로 상태머신 설정한 후 Game.SetCharacterAnimStateMachine 로 해당 애니메이션 상태머신을 
사용 할 캐릭터 셋팅을 설정하면, 해당 캐릭터 셋팅으로 캐릭터 생성 될 때 해당 애니메이션 상태머신이 설정 돼요. 
# **함수**

| **RModeSequenceAnimState* AddAnimState(string StateName, string ResourceID)** |
| :--- |
단일 애니메이션을 플레이하는 애니메이션 상태 추가 
| **RModeSequenceAnimState* AddAnimState(string StateName, string ResourceID, int PlayCount)** |
| :--- |
단일 애니메이션을 플레이하는 애니메이션 상태 추가 
| **RModeSequenceAnimState* AddAnimState(string StateName, string ResourceID, int Playcount, float PlaySpeed)** |
| :--- |
단일 애니메이션을 플레이하는 애니메이션 상태 추가 
| **RModeBlendAnimState AddBlendAnimState(string StateName, protected_function BlendFunction)** |
| :--- |
블렌드 애니메이션 상태 추가 
| **RModeBlendAnimState AddBlendAnimState(string StateName, protected_function BlendFunction, int PlayCount)** |
| :--- |
블렌드 애니메이션 상태 추가 
| **AddTransition(string FromState, string ToState)** |
| :--- |
애니메이션 상태 전이 추가 
| **void AddTransition(string FromState, string ToState, float BlendTime)** |
| :--- |
애니메이션 상태 전이 추가 
| **AddTransition(string FromState, string ToState, protected_function Condition)** |
| :--- |
애니메이션 상태 전이 추가 
| **AddTransition(string FromState, string ToState, protected_function Condition, float BlendTime)** |
| :--- |
애니메이션 상태 전이 추가 
| **SetStartStateName(string StateName)** |
| :--- |
애니메이션 상태 머신이 활성화 될 때 시작 애니메이션 상태 설정 
| **ChangeAnimStateDirect_ForScript(string ChangeStateName)** |
| :--- |
해당 애니메이션 상태로 전이 
