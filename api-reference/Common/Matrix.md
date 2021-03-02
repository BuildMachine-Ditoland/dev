
Matrix 객체의 위치 회전 값을 얻거나 변경 할 수 있어요. 
## **생성자**

| **Matrix.new()** |
| :--- |

Matrix 를 생성해요. 
## **함수**

| **Vector GetLocation()** |
| :--- |

위치를 얻을 수 있어요. 
| **void SetLocation(float x, float y, float z)** |
| :--- |

주어진 값으로 위치를 설정해요. (설정할 X 값, 설정할 Y 값, 설정할 Z 값) 
| **void SetLocation(Vector LocationValue)** |
| :--- |

주어진 값으로 위치를 설정해요. (설정할 벡터 값) 
| **void AddLocation(float x, float y, float z)** |
| :--- |

주어진 값으로 기존 위치에 +로 계산해서 위치를 설정해요. (더하기 할 X 값, 더하기 할 Y 값, 더하기 할 Z 값) 
| **Vector GetRotation()** |
| :--- |

각도를 얻을 수 있어요. (Vector.X : Roll, Vector.Y : Pitch, Vector.Z : Yaw) 
| **Vector SetRotation(float Roll, float Pitch, float Yaw)** |
| :--- |

주어진 값으로 각도를 설정해요. (설정할 Roll 값, 설정할 Pitch 값, 설정할 Yaw 값) 
| **void AddRotation(float x, float y, float z)** |
| :--- |

주어진 값으로 기존 각도에 +로 계산해서 각도를 설정해요. (더하기 할 X 값, 더하기 할 Y 값, 더하기 할 Z 값) 
| **void SetScale(float scale)** |
| :--- |

주어진 값으로 스케일을 설정해요. (설정할 스케일 값) 
| **Vector SetScaleXYZ(float x, floay y, float z)** |
| :--- |

주어진 값을 이용하여 Vector 스케일을 설정해요. (설정할 X 값, 설정할 Y 값, 설정할 Z 값) 
| **Vector GetScaleXYZ()** |
| :--- |

스케일을 Vector의 형식으로 얻을 수 있어요. 
| **Vector GetForward()** |
| :--- |

객체가 바라보고 있는 방향 Vector을 얻을 수 있어요. 
| **Vector GetRight()** |
| :--- |

객체가 바라보고 있는 방향의 오른쪽 방향 Vector를 얻을 수 있어요. 
| **Vector GetTop()** |
| :--- |

객체의 위측 방향 Vector를 얻을 수 있어요. 
