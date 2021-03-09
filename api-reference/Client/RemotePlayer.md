
클라이언트 스크립트에서 사용되는 플레이어 객체에요. [Game:GetRemotePlayer(PlayerName)](https://ditoland-utplus.gitbook.io/ditoland/api-reference/client/game)혹은 [LocalPlayer:GetRemotePlayer()](https://ditoland-utplus.gitbook.io/ditoland/api-reference/client/localplayer) 함수를 이용하면 얻을 수 있어요. 
<br>
<br>
| **RGameClientCharacter GetCharacter()** |
| :--- |

플레이어의 캐릭터를 얻을 수 있어요. 

샘플 

```lua
local player = Game:GetAllPlayer()[1]
local character = player:GetCharacter() --플레이어의 캐릭터를 반환해요.
```
<br>
<br>
| **string GetPlayerName()** |
| :--- |

플레이어의 이름을 얻을 수 있어요. 

샘플 

```lua
local character = Game:GetAllPlayer()[1]:GetCharacter()
print(character:GetPlayerName()) --캐릭터의 플레이어 이름을 문자열로 반환해요.
```
<br>
<br>
| **ObjectFXClient CreateFX(ObjectFXClient FXObject, Bone BoneType)** |
| :--- |

캐릭터의 특정 위치에 FX를 생성할 수 있어요. (생성 할 FX 오브젝트, [Enum.Bone.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/bone)) 

샘플 

```lua
local player = LocalPlayer:GetRemotePlayer()
player:CreateFX(Workspace.Effect, Enum.Bone.Body) --캐릭터의 특정 부위에 이펙트를 생성해요.
```
<br>
<br>
| **ObjectSoundClient CreateSound(ObjectSoundClient SoundObject)** |
| :--- |

캐릭터의 위치에 Sound를 생성할 수 있어요. (생성 할 Sound 오브젝트) 

샘플 

```lua
local player = LocalPlayer:GetRemotePlayer()
player:CreateSound(Workspace.Sound)
```
<br>
<br>
| **RModeHitResult LineTrace(Vector Start, Vector Dir, float Distance)** |
| :--- |

두 지점 간의 오브젝트의 충돌을 체크할 수 있어요. (시작 지점 Vector, 원하는 지점 Vector, 지점 간의 거리) 

샘플 

```lua
local startPos = Workspace.Cube:GetTransform():GetLocation()
local dir = Vector.new(1, 0, 0)
local distance = 1000
local player = LocalPlayer:GetRemotePlayer()
local target = player:LineTrace(startPos, dir, distance) --시작 위치에서 특정 방향으로 거리만큼의 충돌 리스트가 반환돼요.

print(target.HitObject:GetName()) --충돌한 오브젝트에요.
print(target.HitLocation) --충돌한 오브젝트의 위치에요.
```
<br>
<br>
| **bool IsMyPlayer()** |
| :--- |

플레이어 자신의 플레이어인지 확인할 수 있어요. 

샘플 

```lua
local player = LocalPlayer:GetRemotePlayer()
print(player:IsMyPlayer())
```
<br>
<br>
| **Item GetEquipItem(string EquipSlot)** |
| :--- |

해당 플레이어 캐릭터가 착용중인 아이템을 얻을 수 있어요. (장착 중인 아이템 슬롯) 
# **상속받아 사용 가능한 기능들**

<br>
## **속성**

<br>
<br>
| **Parent** |
| :--- |

부모 객체를 얻을 수 있어요. 
<br>
샘플

```lua

local parent = Workspace.Floor.Parent --오브젝트의 부모를 반환해요 

print(parent:GetName())  

``` 
<br>
## **이벤트**

<br>
<br>
| **ConnectChangeEventFunction(string ValueName, function FunctionName)** |
| :--- |

추가된 값이 변경 될 때 호출되는 이벤트에요. (Value 이름, 연결 함수) 
<br>
샘플

```lua

local cube = Workspace.Cube 

 

wait(1) 

cube.SomeValue = 1 

 

local function ChangeSomeValue() 

print("ChangeSomeValue!") 

end 

cube:ConnectChangeEventFunction("SomeValue", ChangeSomeValue)  --오브젝트의 "SomeValue" 라는 Value가 변경되면 ChangeSomeValue 함수를 호출해요. 

``` 
<br>
<br>
| **AddTimeEvent(String EventName, float Time, LuaScriptFunction EventFuunction)** |
| :--- |

일정 시간뒤에 연결 함수가 호출되는 이벤트를 추가해요. (추가할 이벤트 이름, 시간, 연결 함수) 
<br>
샘플

```lua

local waitTime = 2 

local function PrintMessage() --AddTimeEvent로 등록된 함수는 일정시간을 기다린뒤, 호출돼요. 

print("Call PrintMessage!")  

end 

Game:AddTimeEvent("PrintMessage", waitTime, PrintMessage) --일정시간을 기다린뒤 호출되는 함수를 문자열로 등록해요. 

``` 
<br>
<br>
| **DeleteTimeEvent(String EventName)** |
| :--- |

등록된 시간 이벤트를 삭제해요. (삭제할 이벤트 이름) 
<br>
샘플

```lua

local waitTime = 2 

local function PrintMessage() --AddTimeEvent로 등록된 함수는 일정시간을 기다린뒤, 호출돼요. 

print("Call PrintMessage!")  

end 

Game:AddTimeEvent("PrintMessage", waitTime, PrintMessage) --일정시간을 기다린뒤 호출되는 함수를 문자열로 등록해요. 

Game:DeleteTimeEvent("PrintMessage") --AddTimeEvent로 등록한 함수를 삭제해서 호출되지 않게 해요. 

``` 
<br>
## **함수**

<br>
<br>
| **string GetName()** |
| :--- |

객체의 이름을 얻을 수 있어요. 
<br>
샘플

```lua

print(Workspace.Floor:GetName()) --오브젝트의 이름을 문자열로 반환해요. 

``` 
<br>
<br>
| **RModeObject GetParent(string ParentName)** |
| :--- |

이름으로 부모 객체를 얻을 수 있어요. (찾고싶은 부모 객체 이름) 
<br>
<br>
| **RModeObject GetChild(string ChildName)** |
| :--- |

이름으로 자식 객체를 얻을 수 있어요. (찾고싶은 자식 객체 이름) 
<br>
<br>
| **RModeObject GetGetSibling(string Name)** |
| :--- |

이름으로 형제 객체를 얻을 수 있어요. (찾고싶은 형제 객체 이름) 
<br>
<br>
| **List<RScriptObject> GetChildList()** |
| :--- |

자식 객체의 리스트를 얻을 수 있어요. 
<br>
샘플

```lua

local uiList = Workspace.HUD:GetChildList() --오브젝트의 자식 오브젝트를 리스트로 반환해요. 

for i = 1, #uiList do --리스트앞에 #을 붙여 리스트의 길이를 가져올 수 있어요. 

print(uiList[i]:GetName()) 

end 

``` 
<br>
<br>
| **bool IsCharacter()** |
| :--- |

캐릭터인지 확인할 수 있어요. 
<br>
샘플

```lua

local cube = Workspace.Cube 

if cube:IsCharacter() == true then --오브젝트가 Character면 true를 반환해요. 

print(cube:GetName() .. " Is Character") 

end 

``` 
<br>
<br>
| **bool IsStaticMesh()** |
| :--- |

스테틱 메시인지 확인할 수 있어요. 
<br>
샘플

```lua

local cube = Workspace.Cube 

if cube:IsStaticMesh() == true then --오브젝트가 StaticMesh면 true를 반환해요. 

print(cube:GetName() .. " Is StaticMesh") 

end 

``` 
<br>
<br>
| **bool IsFX()** |
| :--- |

FX인지 확인할 수 있어요. 
<br>
샘플

```lua

local cube = Workspace.Cube 

if cube:IsFX() == true then --오브젝트가 FX면 true를 반환해요. 

print(cube:GetName() .. " Is FX") 

end 

``` 
<br>
<br>
| **bool IsSound()** |
| :--- |

Sound인지 확인할 수 있어요. 
<br>
샘플

```lua

local cube = Workspace.Cube 

if cube:IsSound() == true then --오브젝트가 Sound면 true를 반환해요. 

print(cube:GetName() .. " Is Sound") 

end 

``` 
<br>
<br>
| **bool IsPointLight()** |
| :--- |

포인트 라이트인지 확인할 수 있어요. 
<br>
샘플

```lua

local cube = Workspace.Cube 

if cube:IsPointLight() == true then --오브젝트가 PointLight면 true를 반환해요. 

print(cube:GetName() .. " Is PointLight") 

end 

``` 
<br>
<br>
| **bool IsSpotLight()** |
| :--- |

스포트 라이트인지 확인할 수 있어요. 
<br>
샘플

```lua

local cube = Workspace.Cube 

if cube:IsSpotLight() == true then --오브젝트가 SpotLight면 true를 반환해요. 

print(cube:GetName() .. " Is SpotLight") 

end 

``` 
<br>
<br>
| **bool IsSurfaceUI()** |
| :--- |

서피스 UI인지 확인할 수 있어요. 
<br>
샘플

```lua

local cube = Workspace.Cube 

if cube:IsSurfaceUI() == true then --오브젝트가 SurfaceUI면 true를 반환해요. 

print(cube:GetName() .. " Is SurfaceUI") 

end 

``` 
<br>
<br>
| **bool IsScreenUI()** |
| :--- |

스크린 UI인지 확인할 수 있어요. 
<br>
샘플

```lua

local cube = Workspace.Cube 

if cube:IsScreenUI() == true then --오브젝트가 ScreenUI면 true를 반환해요. 

print(cube:GetName() .. " Is ScreenUI") 

end 

``` 
<br>
<br>
| **bool IsItem()** |
| :--- |

아이템인지 확인할 수 있어요. 
<br>
샘플

```lua

local cube = Workspace.Cube 

if cube:IsItem() == true then --오브젝트가 Item면 true를 반환해요. 

print(cube:GetName() .. " Is Item") 

end 

``` 
<br>
<br>
| **bool IsNPC()** |
| :--- |

NPC인지 확인할 수 있어요. 
<br>
샘플

```lua

local cube = Workspace.Cube 

if cube:IsNPC() == true then --오브젝트가 NPC면 true를 반환해요. 

print(cube:GetName() .. " Is NPC") 

end 

``` 
<br>
<br>
| **bool IsFolder()** |
| :--- |

폴더인지 확인할 수 있어요. 
<br>
샘플

```lua

local cube = Workspace.Cube 

if cube:IsFolder() == true then --오브젝트가 Folder면 true를 반환해요. 

print(cube:GetName() .. " Is Folder") 

end 

``` 
<br>
<br>
| **bool IsScript()** |
| :--- |

스트립트인지 확인할 수 있어요. 
<br>
샘플

```lua

local cube = Workspace.Cube 

if cube:IsScript() == true then --오브젝트가 Script면 true를 반환해요. 

print(cube:GetName() .. " Is Script") 

end 

``` 
<br>
<br>
| **bool IsCollider()** |
| :--- |

Collider인지 확인할 수 있어요. 
<br>
샘플

```lua

local cube = Workspace.Cube 

if cube:IsCollider() == true then --오브젝트가 Collider면 true를 반환해요. 

print(cube:GetName() .. " Is Collider") 

end 

``` 
<br>
<br>
| **bool IsWidget()** |
| :--- |

Widget인지 확인할 수 있어요. 
<br>
샘플

```lua

local cube = Workspace.Cube 

if cube:IsWidget() == true then --오브젝트가 Widget면 true를 반환해요. 

print(cube:GetName() .. " Is Widget") 

end 

``` 
<br>
<br>
| **bool IsCamera()** |
| :--- |

Camera인지 확인할 수 있어요. 
<br>
샘플

```lua

local cube = Workspace.Cube 

if cube:IsCamera() == true then --오브젝트가 Camera면 true를 반환해요. 

print(cube:GetName() .. " Is Camera") 

end 

``` 
<br>
<br>
| **bool IsValid()** |
| :--- |

해당 오브젝트가 유효한지 확인 할 수있어요. 
<br>
<br>
| **AddReplicateValue(string ValueName, Vector Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 벡터를 추가해요. (추가할 Value 이름, Vector 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
<br>
샘플

```lua

--서버 스크립트에서------------- 

Game:AddReplicateValue("SomeVector", Vector.new(0, 50, 0), Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요. 

print(Game.SomeVector) 

 

--클라 스크립트에서------------- 

print(Game.SomeVector) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요. 

``` 
<br>
<br>
| **AddReplicateValue(string ValueName, float Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 실수를 추가해요. (추가할 Value 이름, float 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
<br>
샘플

```lua

--서버 스크립트에서------------- 

Game:AddReplicateValue("SomeNumber", 1, Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요. 

print(Game.SomeNumber .. " in Server") 

 

--클라 스크립트에서------------- 

print(Game.SomeNumber .. " in Client") --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요. 

``` 
<br>
<br>
| **AddReplicateValue(string ValueName, bool Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 bool를 추가해요. (추가할 Value 이름, bool 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
<br>
샘플

```lua

--서버 스크립트에서------------- 

Game:AddReplicateValue("SomeBool", true, Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요. 

print(Game.SomeBool) 

 

--클라 스크립트에서------------- 

print(Game.SomeBool) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요. 

``` 
<br>
<br>
| **AddReplicateValue(string ValueName, string Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 문자열을 추가해요. (추가할 Value 이름, string 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
<br>
샘플

```lua

--서버 스크립트에서------------- 

Game:AddReplicateValue("SomeString", "Hello World!", Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요. 

print(Game.SomeString) 

 

--클라 스크립트에서------------- 

print(Game.SomeString) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요. 

``` 
<br>
<br>
| **AddReplicateValue(string ValueName, Color Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 컬러를 추가해요. (추가할 Value 이름, Color 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
<br>
샘플

```lua

--서버 스크립트에서------------- 

Game:AddReplicateValue("SomeColor", Color.new(255, 0, 0, 255), Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요. 

print(Game.SomeColor) 

 

--클라 스크립트에서------------- 

print(Game.SomeColor) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요. 

``` 
<br>
<br>
| **AddSaveValue(string ValueName, Vector Data)** |
| :--- |

해당 객체 저장소에 벡터를 추가해요. (Value 이름, Vector 데이터) 
<br>
<br>
| **AddSaveValue(string ValueName, float Data)** |
| :--- |

해당 객체 저장소에 실수를 추가해요. (Value 이름, float 데이터) 
<br>
<br>
| **AddSaveValue(string ValueName, bool Data)** |
| :--- |

해당 객체 저장소에 bool을 추가해요. (Value 이름, bool 데이터) 
<br>
<br>
| **AddSaveValue(string ValueName, string Data)** |
| :--- |

해당 객체 저장소에 문자열을 추가해요. (Value 이름, string 데이터) 
<br>
<br>
| **AddSaveValue(string ValueName, Color Data)** |
| :--- |

해당 객체 저장소에 칼라를 추가해요. (Value 이름, Color 데이터) 
