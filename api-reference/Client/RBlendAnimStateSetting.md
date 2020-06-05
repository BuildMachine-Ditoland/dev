# **RBlendAnimStateSetting**


[RAnimStateSettingBase](https://ditoland-utplus.gitbook.io/ditoland/api-reference/client/ranimstatesettingbase)의 자식 객체로, 여러 애니메이션을 특정 값에 따라 블랜딩하는 애니메이션 상태를 설정하는 객체에요. 

예) 이동 속도에 따른 평상시, 걷기, 달리기 애니메이션 블랜딩 

[RAnimStateSettingBase](https://ditoland-utplus.gitbook.io/ditoland/api-reference/client/ranimstatesettingbase)의 AddBlendAnimState 함수로 생성해요. 
## **함수**

| **ModeBlendAnimationDataSetting AddBlendAnimation(float BlendValue, string AnimResourceID)** |
| :--- |

블랜딩 애니메이션 추가 (블렌드 값, 리소스 ID) 
| **ModeBlendAnimationDataSetting AddBlendAnimation(float BlendValue, string AnimResourceID, float PlaySpeed)** |
| :--- |

블랜딩 애니메이션 추가 (블렌드 값, 리소스 ID, 플레이 속도) 
