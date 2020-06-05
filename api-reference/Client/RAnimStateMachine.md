# **RAnimStateMachine**


애니메이션 상태 머신이에요. [RGameClient](https://ditoland-utplus.gitbook.io/ditoland/api-reference/client/rgameclient#undefined-1)의 AddAnimStateMachineSetting 함수로 생성 가능해요. 

Game:AddAnimStateMachineSetting 로 상태머신 설정한 후 Game:SetCharacterAnimStateMachine 로 해당 애니메이션 상태머신을 사용 할 캐릭터로 설정하면, 

해당 캐릭터 셋팅으로 캐릭터 생성 될 때 해당 애니메이션 상태머신이 설정 돼요. 
# **함수**

| **RModeSequenceAnimState AddAnimState(string StateName, string ResourceID)** |
| :--- |

단일 애니메이션을 플레이하는 애니메이션 상태 추가 (상태 이름, 리소스 ID) 
| **RModeSequenceAnimState AddAnimState(string StateName, string ResourceID, int PlayCount)** |
| :--- |

단일 애니메이션을 플레이하는 애니메이션 상태 추가 (상태 이름, 리소스 ID, 플레이 횟수) 
| **RModeSequenceAnimState AddAnimState(string StateName, string ResourceID, int Playcount, float PlaySpeed)** |
| :--- |

단일 애니메이션을 플레이하는 애니메이션 상태 추가 (상태 이름, 리소스 ID, 플레이 횟수, 플레이 속도) 
| **RModeBlendAnimState AddBlendAnimState(string StateName, protected_function BlendFunction)** |
| :--- |

블렌드 애니메이션 상태 추가 (상태 이름, 연결 함수) 
| **RModeBlendAnimState AddBlendAnimState(string StateName, protected_function BlendFunction, int PlayCount)** |
| :--- |

블렌드 애니메이션 상태 추가 (상태 이름, 연결 함수, 플레이 횟수) 
| **AddTransition(string FromState, string ToState)** |
| :--- |

애니메이션 상태 전이 추가 (시작 상태 이름, 전이할 상태 이름) 
| **AddTransition(string FromState, string ToState, float BlendTime)** |
| :--- |

애니메이션 상태 전이 추가 (시작 상태 이름, 전이할 상태 이름, 블렌딩 시간) 
| **AddTransition(string FromState, string ToState, protected_function Condition)** |
| :--- |

애니메이션 상태 전이 추가 (시작 상태 이름, 전이할 상태 이름, 연결 함수) 
| **AddTransition(string FromState, string ToState, protected_function Condition, float BlendTime)** |
| :--- |

애니메이션 상태 전이 추가 (시작 상태 이름, 전이할 상태 이름, 연결 함수, 블렌딩 시간) 
| **SetStartStateName(string StateName)** |
| :--- |

애니메이션 상태 머신이 활성화 될 때 시작 애니메이션 상태 설정 (상태 이름) 
| **ChangeAnimStateDirect_ForScript(string ChangeStateName)** |
| :--- |

해당 애니메이션 상태로 전이 (변경할 상태 이름) 
