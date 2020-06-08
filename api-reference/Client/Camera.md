# **Camera**


클라이언트에서 사용되는 카메라 서비스 객체에요. Camera로 얻어서 사용 할 수 있어요. 
## **함수**

| **SetSettingName(string name)** |
| :--- |

캐릭터에 적용 할 카메라 셋팅 이름 설정 (이름 값) 
| **PlayCameraShake(float time, float scale)** |
| :--- |

카메라 쉐이크 시작 (쉐이크 시간, 쉐이크 강도) 
| **StopCameraShake(bool bImmediately)** |
| :--- |

카메라 쉐이크 중지 (즉시중지 여부) 
| **PlayCameraFade(float FromAlpha, float ToAlpha, float Duration, Color Color, bool HoldFinish)** |
| :--- |

카메라 페이드 시작 (시작 강도 0~1, 종료 강도 0~1, 시작에서 종료까지 걸리는 시간, 적용할 [Color](https://ditoland-utplus.gitbook.io/ditoland/api-reference/common/color)값, 종료 시점 상태 유지 여부) 
| **StopCameraFade()** |
| :--- |

카메라 페이드 정지 
