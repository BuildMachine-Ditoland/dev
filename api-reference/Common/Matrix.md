
Matrix 객체의 위치 회전 값을 얻거나 변경 할 수 있어요. <br>
<br>
## **생성자**

<br>
| **Matrix.new()** |
| :--- |

Matrix 를 생성해요. <br>
<br>
## **함수**

<br>
| **Vector GetLocation()** |
| :--- |

위치를 얻을 수 있어요. <br>

샘플 <br>

```lua
local character = Game:GetAllPlayer()[1]:GetCharacter()
local characterPos = character:GetTransform():GetLocation() --캐릭터의 위치값을 Vector로 반환해요.
```
<br>
| **void SetLocation(float x, float y, float z)** |
| :--- |

주어진 값으로 위치를 설정해요. (설정할 X 값, 설정할 Y 값, 설정할 Z 값) <br>

샘플 <br>

```lua
local targetTransform = Game:GetAllPlayer()[1]:GetTransform()
targetTransform:SetLocation(0, 100, 0)
targetTransform:SetRotation(Vector.new(0, 100, 0))
character:SetTransform(targetTransform) --오브젝트를 보간으로 이동시켜요. (캐릭터는 보간없이 움직여요.)
```
<br>
| **void SetLocation(Vector LocationValue)** |
| :--- |

주어진 값으로 위치를 설정해요. (설정할 벡터 값) <br>

샘플 <br>

```lua
local targetTransform = Game:GetAllPlayer()[1]:GetTransform()
targetTransform:SetLocation(Vector.new(0, 100, 0))
targetTransform:SetRotation(Vector.new(0, 100, 0))
character:SetTransform(targetTransform) --오브젝트를 보간으로 이동시켜요. (캐릭터는 보간없이 움직여요.)
```
<br>
| **void AddLocation(float x, float y, float z)** |
| :--- |

주어진 값으로 기존 위치에 +로 계산해서 위치를 설정해요. (더하기 할 X 값, 더하기 할 Y 값, 더하기 할 Z 값) <br>

샘플 <br>

```lua
local cube = Workspace.Cube
local cubeTransform = cube:GetTransform()

print(cubeTransform:GetLocation())

cubeTransform:AddLocation(50, 0, 0)
print(cubeTransform:GetLocation())
cube:SetTransform(cubeTransform)
```
<br>
| **Vector GetRotation()** |
| :--- |

각도를 얻을 수 있어요. (Vector.X : Roll, Vector.Y : Pitch, Vector.Z : Yaw) <br>

샘플 <br>

```lua
local character = Game:GetAllPlayer()[1]:GetCharacter()
local characterRot = character:GetTransform():GetRotation() --캐릭터의 회전값을 Vector로 반환해요.
```
<br>
| **Vector SetRotation(float Roll, float Pitch, float Yaw)** |
| :--- |

주어진 값으로 각도를 설정해요. (설정할 Roll 값, 설정할 Pitch 값, 설정할 Yaw 값) <br>
<br>
| **void AddRotation(float x, float y, float z)** |
| :--- |

주어진 값으로 기존 각도에 +로 계산해서 각도를 설정해요. (더하기 할 X 값, 더하기 할 Y 값, 더하기 할 Z 값) <br>

샘플 <br>

```lua
local cube = Workspace.Cube
local cubeTransform = cube:GetTransform()

print(cubeTransform:GetRotation())

cubeTransform:AddRotation(50, 0, 0)
print(cubeTransform:GetRotation())
cube:SetTransform(cubeTransform)
```
<br>
| **void SetScale(float scale)** |
| :--- |

주어진 값으로 스케일을 설정해요. (설정할 스케일 값) <br>

샘플 <br>

```lua
local cube = Workspace.Cube
local scale = cube:GetScale() --해당 오브젝트의 크기를 100으로 나눠서 Vector로 반환해요.(예를 들어 x값이 100이면 1로 반한돼요.)
scale.Y = scale.Y + 0.5
cube:SetScale(scale) --오브젝트의 크기를 설정해요.
```
<br>
| **Vector SetScaleXYZ(float x, floay y, float z)** |
| :--- |

주어진 값을 이용하여 Vector 스케일을 설정해요. (설정할 X 값, 설정할 Y 값, 설정할 Z 값) <br>

샘플 <br>

```lua
local cube = Workspace.Cube
local scale = cube:GetScale() --해당 오브젝트의 크기를 100으로 나눠서 Vector로 반환해요.(예를 들어 x값이 100이면 1로 반한돼요.)
scale.Y = scale.Y + 0.5
cube:SetScale(scale) --오브젝트의 크기를 설정해요.
```
<br>
| **Vector GetScaleXYZ()** |
| :--- |

스케일을 Vector의 형식으로 얻을 수 있어요. <br>
<br>
| **Vector GetForward()** |
| :--- |

객체가 바라보고 있는 방향 Vector을 얻을 수 있어요. <br>

샘플 <br>

```lua
local cubeTransform = Workspace.Cube:GetTransform()
print(cubeTransform:GetForward())
```
<br>
| **Vector GetRight()** |
| :--- |

객체가 바라보고 있는 방향의 오른쪽 방향 Vector를 얻을 수 있어요. <br>

샘플 <br>

```lua
local cubeTransform = Workspace.Cube:GetTransform()
print(cubeTransform:GetRight())
```
<br>
| **Vector GetTop()** |
| :--- |

객체의 위측 방향 Vector를 얻을 수 있어요. <br>

샘플 <br>

```lua
local cubeTransform = Workspace.Cube:GetTransform()
print(cubeTransform:GetTop())
```
