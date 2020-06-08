# **RAnimStateMachineSetting**


게임에 사용되는 애니매이션 상태머신을 설정하는 객체에요. Game:AddAnimStateMachineSetting로 생성해요. 
## **함수**

| **RModeSequenceAnimStateSetting AddAnimState(string StateName, string ResourceID)** |
| :--- |

단일 애니메이션 상태 설정 추가 (상태 이름, 리소스 ID) 
| **RModeSequenceAnimStateSetting AddAnimState(string StateName, string ResourceID, int PlayCount)** |
| :--- |

단일 애니메이션 상태 설정 추가 (상태 이름, 리소스 ID, 플레이 횟수) 
| **RModeSequenceAnimStateSetting AddAnimState(string StateName, string ResourceID, int PlayCount, float PlaySpeed)** |
| :--- |

단일 애니메이션 상태 설정 추가 (상태 이름, 리소스 ID, 플레이 횟수, 플레이 속도) 
| **RModeBlendAnimStateSetting AddBlendAnimState(string StateName, protected_function BlendFunction)** |
| :--- |

블랜드 애니메이션 상태 설정 추가 (상태 이름, 연결 함수) 
| **RModeBlendAnimStateSetting AddBlendAnimState(string StateName, protected_function BlendFunction, int PlayCount)** |
| :--- |

블랜드 애니메이션 상태 설정 추가 (상태 이름, 연결 함수, 플레이 횟수) 
| **AddAnimTransition(string FromState, string ToState)** |
| :--- |

애니메이션 상태 전이 설정 추가 (시작 상태 이름, 전이할 상태 이름) 
| **AddAnimTransition(string FromState, string ToState, float BlendTime)** |
| :--- |

애니메이션 상태 전이 설정 추가 (시작 상태 이름, 전이할 상태 이름, 블렌딩 시간) 
| **AddAnimTransition(string FromState, string ToState, protected_function Condition)** |
| :--- |

애니메이션 상태 전이 설정 추가 (시작 상태 이름, 전이할 상태 이름, 연결 함수) 
| **AddAnimTransition(string FromState, string ToState, protected_function Condition, float BlendTime)** |
| :--- |

애니메이션 상태 전이 설정 추가 (시작 상태 이름, 전이할 상태 이름, 연결 함수, 블렌딩 시간) 
| **SetStartState(string StateName)** |
| :--- |

애니메이션 상태머신이 활성화 될 때 시작 애니메이션 상태 설정 (상태 이름) 
