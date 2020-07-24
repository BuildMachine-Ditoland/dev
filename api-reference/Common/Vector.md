
Vector에 대한 정보를 다루는 객체에요. 
## **생성자**

| **Vector.new(number X, number Y, number Z)** |
| :--- |

Vector를 X, Y, Z 좌표값을 이용해서 생성해줘요. (생성할 X좌표 값, 생성할 Y좌표 값, 생성할 Z좌표 값) 
| **Vector.new(number Value)** |
| :--- |

Vector를 Value값을 이용해서 생성해줘요. (생성할 Value 값) 
| **Vector.new()** |
| :--- |

Vector의 X, Y, Z 좌표를 0으로해서 생성해줘요. 
## **연산자**


Vector = Vector + Vector 

두 벡터 값을 더해서 그 값을 리턴해줘요. 

Vector = Vector - Vector 

앞에 벡터에서 뒤의 벡터를 뺀 값을 리턴해줘요. 

Vector = Vector * Vector 

두 벡터 값을 곱해서 그 값을 리턴해줘요. 

Vector = Vector * float 

두 벡터 값을 곱해서 그 값을 리턴해줘요. 
## **함수**

| **void Normalize()** |
| :--- |

단위를 1로 정규화 시켜주는 함수에요. 
| **float CosineAngle2D(Vector Other)** |
| :--- |

두 벡터의 XY 평면의 사잇각의 cos 값을 리턴해줘요. (사잇각을 구할 벡터) 
## **속성**

| **X** |
| :--- |

X 좌표에요. 
| **Y** |
| :--- |

Y 좌표에요. 
| **Z** |
| :--- |

Z 좌표에요. 

샘플 

```lua
a = Vector.new(1, 2, 3)
b = Vector.new(3)

c = a + b		--> c.X = 4, c.Y = 5, c.Z = 6

d = Vector.new()
d.X = 10

d.Normalize()   --> d.X = 1, d.Y = 0, d.Z = 0
```
