# **RVehicle**


자동차 객체에요. 
## **함수**

| **MakeVehicleChassis(RScriptWorldObject Chassis, FRVehicleCreationInfo VehicleCreationInfo)** |
| :--- |

특정 WorldObject를 Chassis로 만들어줌 (변경할 오브젝트, [Vehicle데이터](https://ditoland-utplus.gitbook.io/ditoland/api-reference/common/vehiclecreationinfo))
| **AttachWheel(RScriptWorldObject Wheel, FRWheelCreationInfo WheelCreationInfo);** |
| :--- |

Chassis에 휠을 붙임 (휠 오브젝트, [Wheel데이터](https://ditoland-utplus.gitbook.io/ditoland/api-reference/common/wheelcreationinfo))
| **SetOwner(string PlayerName);** |
| :--- |

이 Vehicle을 소유한 플레이어를 셋팅 (플레이어 이름) 
| **bool IsOccupied()** |
| :--- |

Vehicle을 이용중인지 판별 
| **void Forward(float power)** |
| :--- |

전진 (속도 값) 
| **Reverse(float power)** |
| :--- |

후진 (속도 값) 
| **SteerLeft(float power)** |
| :--- |

좌회전 (속도 값) 
| **SteerRight(float power)** |
| :--- |

우회전 (속도 값) 
| **Brake(float power);** |
| :--- |

정지 (속도 값) 
| **Reset(float height, float cooltime)** |
| :--- |

Vehicle의 자세를 바로 잡는다. (높이 값, 대기 시간) 
