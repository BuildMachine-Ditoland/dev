# **RCameraSetting**


캐릭터가 사용하는 카메라 설정 데이터를 가지고 있는 객체에요. 
## **함수**

| **SetDistance(float distance)** |
| :--- |

카메라와 캐릭터 사이의 직선 길이 설정 (길이 값) 
| **IsRotationFix(bool bOn)** |
| :--- |

이동시 캐릭터 회전 가능 여부 (회전 가능 여부) 
| **FieldOfView(float value)** |
| :--- |

Field Of View 각도 값 (각도 값) 
| **TargetOffset(FVector offset)** |
| :--- |

카메라 Offset Vector (Vector 값) 
| **UsePawnControlRotation(bool bUse)** |
| :--- |

폰의 회전값을 사용할것인지 여부 (사용 여부) 
| **SetCameraPitch(float value)** |
| :--- |

카메라의 Pitch(Rotation Y) 값을 설정 (Pitch 값) 
| **SetCameraLag(bool bOn, float speed, float MaxDistance)** |
| :--- |

카메라의 Lag 기능을 적용할지 여부 (적용 여부, 속도, 최대거리) 
