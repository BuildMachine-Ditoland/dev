# **RSequenceAnimStateSetting**


[RAnimStateSettingBase](https://ditoland-utplus.gitbook.io/ditoland/api-reference/client/ranimstatesettingbase)의 자식 객체로, 단일 애니메이션을 플레이하는 애니메이션 상태를 설정하는 객체에요. 

[RAnimStateSettingBase](https://ditoland-utplus.gitbook.io/ditoland/api-reference/client/ranimstatesettingbase)의 AddAnimState 함수로 생성해요. 
## **이벤트**

| **void AddAnimationEvent(String EventName, float Time, protected_function function EventFunction)** |
| :--- |

애니메이션 이벤트 추가 (이벤트 이름, 플레이 시간, 연결 함수) 
| **void DeleteAnimationEvent(String EventName)** |
| :--- |

애니메이션 이벤트 제거 (이벤트 이름) 
