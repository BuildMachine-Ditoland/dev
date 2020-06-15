
Matrix 객체의 위치 회전 값을 얻거나 변경 할 수 있어요. 
## **생성자**

| **Matrix.new()** |
| :--- |

Matrix 를 생성해요. 
## **함수**

| **Vector GetLocation()** |
| :--- |

위치를 얻을 수 있어요. 
| **SetLocation(Vector)** |
| :--- |

주어진 값으로 위치를 설정해요. (설정할 Vector 값) 
| **Vector GetRotation()** |
| :--- |

각도를 얻을 수 있어요. (Vector.X : Pitch, Vector.Y : Yaw, Vector.Z : Roll) 
| **Vector SetRotation(float Pitch, float Yaw, float Roll)** |
| :--- |

주어진 값으로 각도를 설정해요. (설정할 Vector.X 값, 설정할 Vector.Y 값, 설정할 Vector.Z 값) 
| **SetScale(float scale)** |
| :--- |

주어진 값으로 스케일을 설정해요. (설정할 스케일 값) 
| **Vector SetScaleXYZ(float x, float y, float z)** |
| :--- |

주어진 값을 이용하여 Vector 스케일을 설정해요. (설정할 X 값, 설정할 Y 값, 설정할 Z 값) 
| **float GetScale()** |
| :--- |

스케일을 얻을 수 있어요 
| **Vector GetScaleXYZ(float x, float y, float z)** |
| :--- |

XYZ 값을 이용해 Vector 스케일을 얻을 수 있어요. (X 값, Y 값, Z 값) 
