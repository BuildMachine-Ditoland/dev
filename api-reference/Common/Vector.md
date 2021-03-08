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
샘플 

```lua
local pos1 = Vector.new(50, 0, 0) --x 50, y 0, z 0로 할당돼요.
local pos2 = Vector.new(100) --x 100, y 100, z 100로 할당돼요.
local pos3 = Vector.new() --x 0, y 0, z 0로 할당돼요.

print(pos1)
print(pos2)
print(pos3)
```
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
local pos1 = Vector.new(1, 2, 3)
local pos2 = Vector.new(3) --pos2.X = 3, pos2.Y = 3, pos2.Z = 3로 할당돼요.
local pos3 = pos1 + pos2   --pos3.X = 4, pos3.Y = 5, pos3.Z = 6로 할당돼요.

local pos4 = Vector.new()  --pos4.X = 0,  pos4.Y = 0, pos4.Z = 0로 할당돼요.
pos4.X = 10                --pos4.X = 10, pos4.Y = 0, pos4.Z = 0로 할당돼요.
pos4.Normalize()           --pos4.X = 1,  pos4.Y = 0, pos4.Z = 0로 할당돼요.
```
