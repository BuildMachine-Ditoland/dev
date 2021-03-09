
클라이언트에서 캐릭터의 기본 동작을 설정 할 수 있는 객체에요. 
<br>
## **이벤트**

<br>
<br>
| **ProcessInputAxisEvent(string Event, protected_function ProcessFunc)** |
| :--- |

축 인풋 이벤트에요. (설정할 이벤트 이름, 연결 함수) 

샘플 

```lua
Input:AddGroup("UIInput") --조작그룹을 추가해요.
Input:AddActionKeyEvent("UIInput", "MenuKey", Enum.Key.M) --조작 키 이벤트를 추가해요.
Input:AddAxisKeyEvent("UIInput", "AxisKey", Enum.Key.Q, 1) --조작 축 이벤트를 추가해요.
Input:ActiveGroup("UIInput") --조작그룹을 활성화해요.

LocalPlayer:ProcessInputActionEvent("MenuKey", Enum.KeyInputType.Pressed, function() --조작이 발생했을때 처리할 이벤트를 등록해요.
    print("Input!")
end)

LocalPlayer:ProcessInputAxisEvent("AxisKey", Enum.KeyInputType.Pressed, function(value) --조작이 발생했을때 처리할 이벤트를 등록해요.
    print("Axis Input!")
end)
```
<br>
<br>
| **ProcessInputActionEvent(string Event, RModeInputType InputType, protected_function ProcessFunc)** |
| :--- |

키 인풋 이벤트에요. (설정할 이벤트 이름, [Enum.KeyInputType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/keyinputtype), 연결 함수) 

샘플 

```lua
Input:AddGroup("UIInput") --조작그룹을 추가해요.
Input:AddActionKeyEvent("UIInput", "MenuKey", Enum.Key.M) --조작 키 이벤트를 추가해요.
Input:AddAxisKeyEvent("UIInput", "AxisKey", Enum.Key.Q, 1) --조작 축 이벤트를 추가해요.
Input:ActiveGroup("UIInput") --조작그룹을 활성화해요.

LocalPlayer:ProcessInputActionEvent("MenuKey", Enum.KeyInputType.Pressed, function() --조작이 발생했을때 처리할 이벤트를 등록해요.
    print("Input!")
end)

LocalPlayer:ProcessInputAxisEvent("AxisKey", Enum.KeyInputType.Pressed, function(value) --조작이 발생했을때 처리할 이벤트를 등록해요.
    print("Axis Input!")
end)
```
<br>
<br>
| **OnChangedInventoryItem** |
| :--- |

인벤토리 아이템이 변화할 때 호출되는 이벤트에요. 
<br>
## **함수**

<br>
<br>
| **MoveDir(FVector Dir, float Value)** |
| :--- |

주어진 방향으로 일정 값만큼 캐릭터를 이동시켜요. 설정된 이동 타입에 관계없이 동작해요. (원하는 이동방향 Vector 값, 이동할 크기) 
<br>
<br>
| **MoveForward(float Value)** |
| :--- |

설정된 이동 타입에 따라 앞으로 이동시켜요. (1 : 전진, -1 : 후진 이동) 
<br>
<br>
| **MoveRight(float Value)** |
| :--- |

좌, 우로 이동시켜요. (-1 : 좌측, 1 : 우측 이동) 
<br>
<br>
| **Turn(float Value)** |
| :--- |

캐릭터의 바라보는 좌우 방향을 설정해요. (-1 : 좌측, 1 : 우측 방향 값) 
<br>
<br>
| **LookUp(float Value)** |
| :--- |

캐릭터의 바라보는 상하 방향을 설정해요. (-1 : 밑,1 : 위에 방향 값) 
<br>
<br>
| **ZoomInOut(float Value)** |
| :--- |

카메라의 줌을 설정할 수 있어요. (설정할 카메라 줌 크기 값) 

샘플 

```lua
local camera = LocalPlayer:GetCurrentCamera()
camera:ZoomInOut(0.5) --카메라의 확대축소값을 조절해요.
```
<br>
<br>
| **Jump()** |
| :--- |

점프동작을 실행해요. 
<br>
<br>
| **Sit()** |
| :--- |

캐릭터의 앉기 상태 여부를 설정해요. 

샘플 

```lua
LocalPlayer:Sit()
```
<br>
<br>
| **UnSit()** |
| :--- |

캐릭터의 앉기 상태 여부를 풀어요. 

샘플 

```lua
LocalPlayer:UnSit()
```
<br>
<br>
| **JumpRelease()** |
| :--- |

점프를 해제 한다.(삭제 예정) 
<br>
<br>
| **SetEnableMovementeControl(bool Enable)** |
| :--- |

자신의 캐릭터 움직임 컨트롤 가능 여부를 결정해요. (활성, 비활성 여부) 

샘플 

```lua
LocalPlayer:SetEnableMovementeControl(false) --자신의 이동 조작을 비활성화해요.
```
<br>
<br>
| **SetEnableCameraControl(bool Enable)** |
| :--- |

자신의 카메라 움직임 컨트롤 가능 여부를 결정해요. (활성, 비활성 여부) 

샘플 

```lua
LocalPlayer:SetEnableCameraControl(false)
print(LocalPlayer.bEnableCameraControl)
```
<br>
<br>
| **bool bEnableCameraControl** |
| :--- |

자신의 카메라 컨트롤 가능여부를 얻거나 세팅할 수 있어요. 

샘플 

```lua
LocalPlayer:SetEnableCameraControl(false)
print(LocalPlayer.bEnableCameraControl)
```
<br>
<br>
| **SetForwardMoveType(ForwardMoveType Type)** |
| :--- |

MoveForward(float Value)의 작동 방식을 결정해요. (Enum.ForwardMoveType.타입) 

ForwardMoveType::XYPlane - 상, 하 이동이 되지않고 평면이동만 가능해요.(일반 적인 캐릭터의 이동 형태) 

ForwardMoveType::Free - 캐릭터가 바라보는 방향으로 이동해요. (프리 카메라의 이동 형태) 

ForwardMoveType::UpDown - 상, 하로만 이동해요. (엘리베이터, 사다리의 이동 형태) 
<br>
<br>
| **BeginDriving( int InVehicleModeObjectKey )** |
| :--- |

탈 것의 운전을 시작하는 함수에요. (탈 것의 키 값) 
<br>
<br>
| **EndDriving()** |
| :--- |

탈 것의 운전을 종료해요. 
<br>
<br>
| **FreeCamMoveUp(float Value)** |
| :--- |

프리캠을 위, 아래로 이동시켜요. (이동할 크기) 
<br>
<br>
| **Vector GetForwardVector()** |
| :--- |

캐릭터가 바라보는 방향을 얻을 수 있어요. 
<br>
<br>
| **Vector GetRightVector()** |
| :--- |

캐릭터의 오른쪽 벡터를 얻을 수 있어요. 
<br>
<br>
| **RModeRemotePlayer GetRemotePlayer()** |
| :--- |

자신의 플레이어를 얻을 수 있어요. 

샘플 

```lua
local player = LocalPlayer:GetRemotePlayer() --자신의 플레이어를 반환해요. 
```
<br>
<br>
| **int GetInventorySize()** |
| :--- |

인벤토리의 사이즈를 얻을 수 있어요. 

샘플 

```lua
local player = Game:GetAllPlayer()[1]
print(player:GetInventorySize()) --플레이어의 인벤토리 사이즈를 숫자로 반환해요.
```
<br>
<br>
| **UseInventoryItem(int InventoryIndex)** |
| :--- |

지정된 칸의 인벤토리 아이템을 사용해요. (사용할 아이템칸) 
<br>
<br>
| **EquipInventoryItem(int InventoryIndex)** |
| :--- |

지정된 칸의 인벤토리 아이템을 착용해요. (착용할 아이템칸) 
<br>
<br>
| **UnEquipInventoryItem(int InventoryIndex)** |
| :--- |

지정된 칸의 인벤토리 아이템의 착용을 해제해요. (해제 할 아이템칸) 
<br>
<br>
| **UnEquipItem(string EquipSlotName)** |
| :--- |

장착되어 있는 Slot이름을 통하여 착용 아이템을 해제시켜요. (해제할 Slot이름) 
<br>
<br>
| **ActionItem(string EquipSlotName, string ActionName)** |
| :--- |

착용하고 있는 아이템의 액션을 설정하는 함수에요. (설정할 장착 Slot이름, 액션 이름) 
<br>
<br>
| **WorldDropInventoryItem(int InventoryIndex)** |
| :--- |

지정된 칸의 아이템을 월드에 드랍시켜요. (월드 드랍할 아이템칸) 
<br>
<br>
| **class FRScriptWorldObject* GetCurrentCamera()** |
| :--- |

현재 camera(FRScriptObjectCameraClient)를 얻는다. 

샘플 

```lua
local camera = LocalPlayer:GetCurrentCamera() --캐릭터의 카메라를 반환해요.
```
<br>
<br>
| **class FRScriptWorldObject* SetCurrentCamera(RScriptWorldObject SourceCamera)** |
| :--- |

SourceCamera를 복사하고, 복사된 Camera로 전환 합니다. 이전 camera는 삭제됩니다.(생성 할 SourceObject) 

샘플 

```lua
local targetCharacter = LocalPlayer:GetRemotePlayer():GetCharacter()
local sourceCamera = Workspace.MainCamera
local characterCamera = LocalPlayer:SetCurrentCamera(sourceCamera) --플레이어에게 카메라를 할당해요.

LocalPlayer:ResetIgnoreLookInput() --카메라 조작을 초기화해요.

characterCamera.Parent = targetCharacter --카메라의 부모 오브젝트를 설정해요.
characterCamera:SetLookAtTarget(nil) --카메라가 대상 오브젝트를 바라보게 해요. (nil이면 바라보지 않아요.)
```
<br>
<br>
| **bool ApplyCurrentCamera(class FRScriptWorldObject* ScriptWorldObject)** |
| :--- |

ScriptWorldObject or ScriptWorldObject의 child에 camera가 있다면 현재 camera로 전환 
<br>
<br>
| **Vector GetControlRotation()** |
| :--- |

Control 각도를 얻을 수 있어요 (Vector.X : Pitch, Vector.Y : Yaw, Vector.Z : Roll) 
<br>
<br>
| **SetControlRotation(Vector)** |
| :--- |

Control 각도를 설정해요 (Vector.X : Pitch, Vector.Y : Yaw, Vector.Z : Roll) 

샘플 

```lua
local sourceCamera = Workspace.MainCamera
local targetCharacter = LocalPlayer:GetRemotePlayer():GetCharacter()
local cameraRotation = sourceCamera:GetTransform():GetRotation()
local characterRotation = targetCharacter:GetTransform():GetRotation()
LocalPlayer:SetControlRotation(Vector.new(0, cameraRotation.Z + characterRotation.Z, 0)) --카메라의 회전값을 설정해요.
```
<br>
<br>
| **ResetIgnoreLookInput()** |
| :--- |

Stops ignoring look input by resetting the ignore look input state 

샘플 

```lua
local targetCharacter = LocalPlayer:GetRemotePlayer():GetCharacter()
local sourceCamera = Workspace.MainCamera
local characterCamera = LocalPlayer:SetCurrentCamera(sourceCamera) --플레이어에게 카메라를 할당해요.

LocalPlayer:ResetIgnoreLookInput() --카메라 조작을 초기화해요.

characterCamera.Parent = targetCharacter --카메라의 부모 오브젝트를 설정해요.
characterCamera:SetLookAtTarget(nil) --카메라가 대상 오브젝트를 바라보게 해요. (nil이면 바라보지 않아요.)
```
<br>
<br>
| **SetIgnoreLookInput(RScriptValueBool InValue)** |
| :--- |

Locks or unlocks look input, consecutive calls stack up and require the same amount of calls to undo, or can all be undone using ResetIgnoreLookInput. 

샘플 

```lua
LocalPlayer:SetIgnoreLookInput(false) --자신의 카메라 조작을 비활성화해요.  
```
<br>
<br>
| **bool bShowMouseCursor** |
| :--- |

마우스 커서를 보이거나 숨길 수 있어요, 

샘플 

```lua
LocalPlayer.bShowMouseCursor = false --자신의 마우스 커서를 비활성화해요.
```
<br>
<br>
| **bool bCaptureMousePermanently** |
| :--- |

마우스를 캡쳐한 상태를 유지합니다. 
# **상속받아 사용 가능한 기능들**

<br>
## **속성**

<br>
<br>
| **Parent** |
| :--- |

부모 객체를 얻을 수 있어요. 
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
## **함수**

<br>
<br>
<br>
| **string GetName()** |
| :--- |

객체의 이름을 얻을 수 있어요. 
샘플

```lua

print(Workspace.Floor:GetName()) --오브젝트의 이름을 문자열로 반환해요. 

``` 
<br>
<br>
<br>
| **RModeObject GetParent(string ParentName)** |
| :--- |

이름으로 부모 객체를 얻을 수 있어요. (찾고싶은 부모 객체 이름) 
<br>
<br>
<br>
| **RModeObject GetChild(string ChildName)** |
| :--- |

이름으로 자식 객체를 얻을 수 있어요. (찾고싶은 자식 객체 이름) 
<br>
<br>
<br>
| **RModeObject GetGetSibling(string Name)** |
| :--- |

이름으로 형제 객체를 얻을 수 있어요. (찾고싶은 형제 객체 이름) 
<br>
<br>
<br>
| **List<RScriptObject> GetChildList()** |
| :--- |

자식 객체의 리스트를 얻을 수 있어요. 
샘플

```lua

local uiList = Workspace.HUD:GetChildList() --오브젝트의 자식 오브젝트를 리스트로 반환해요. 

for i = 1, #uiList do --리스트앞에 #을 붙여 리스트의 길이를 가져올 수 있어요. 

print(uiList[i]:GetName()) 

end 

``` 
<br>
<br>
<br>
| **bool IsCharacter()** |
| :--- |

캐릭터인지 확인할 수 있어요. 
샘플

```lua

local cube = Workspace.Cube 

if cube:IsCharacter() == true then --오브젝트가 Character면 true를 반환해요. 

print(cube:GetName() .. " Is Character") 

end 

``` 
<br>
<br>
<br>
| **bool IsStaticMesh()** |
| :--- |

스테틱 메시인지 확인할 수 있어요. 
샘플

```lua

local cube = Workspace.Cube 

if cube:IsStaticMesh() == true then --오브젝트가 StaticMesh면 true를 반환해요. 

print(cube:GetName() .. " Is StaticMesh") 

end 

``` 
<br>
<br>
<br>
| **bool IsFX()** |
| :--- |

FX인지 확인할 수 있어요. 
샘플

```lua

local cube = Workspace.Cube 

if cube:IsFX() == true then --오브젝트가 FX면 true를 반환해요. 

print(cube:GetName() .. " Is FX") 

end 

``` 
<br>
<br>
<br>
| **bool IsSound()** |
| :--- |

Sound인지 확인할 수 있어요. 
샘플

```lua

local cube = Workspace.Cube 

if cube:IsSound() == true then --오브젝트가 Sound면 true를 반환해요. 

print(cube:GetName() .. " Is Sound") 

end 

``` 
<br>
<br>
<br>
| **bool IsPointLight()** |
| :--- |

포인트 라이트인지 확인할 수 있어요. 
샘플

```lua

local cube = Workspace.Cube 

if cube:IsPointLight() == true then --오브젝트가 PointLight면 true를 반환해요. 

print(cube:GetName() .. " Is PointLight") 

end 

``` 
<br>
<br>
<br>
| **bool IsSpotLight()** |
| :--- |

스포트 라이트인지 확인할 수 있어요. 
샘플

```lua

local cube = Workspace.Cube 

if cube:IsSpotLight() == true then --오브젝트가 SpotLight면 true를 반환해요. 

print(cube:GetName() .. " Is SpotLight") 

end 

``` 
<br>
<br>
<br>
| **bool IsSurfaceUI()** |
| :--- |

서피스 UI인지 확인할 수 있어요. 
샘플

```lua

local cube = Workspace.Cube 

if cube:IsSurfaceUI() == true then --오브젝트가 SurfaceUI면 true를 반환해요. 

print(cube:GetName() .. " Is SurfaceUI") 

end 

``` 
<br>
<br>
<br>
| **bool IsScreenUI()** |
| :--- |

스크린 UI인지 확인할 수 있어요. 
샘플

```lua

local cube = Workspace.Cube 

if cube:IsScreenUI() == true then --오브젝트가 ScreenUI면 true를 반환해요. 

print(cube:GetName() .. " Is ScreenUI") 

end 

``` 
<br>
<br>
<br>
| **bool IsItem()** |
| :--- |

아이템인지 확인할 수 있어요. 
샘플

```lua

local cube = Workspace.Cube 

if cube:IsItem() == true then --오브젝트가 Item면 true를 반환해요. 

print(cube:GetName() .. " Is Item") 

end 

``` 
<br>
<br>
<br>
| **bool IsNPC()** |
| :--- |

NPC인지 확인할 수 있어요. 
샘플

```lua

local cube = Workspace.Cube 

if cube:IsNPC() == true then --오브젝트가 NPC면 true를 반환해요. 

print(cube:GetName() .. " Is NPC") 

end 

``` 
<br>
<br>
<br>
| **bool IsFolder()** |
| :--- |

폴더인지 확인할 수 있어요. 
샘플

```lua

local cube = Workspace.Cube 

if cube:IsFolder() == true then --오브젝트가 Folder면 true를 반환해요. 

print(cube:GetName() .. " Is Folder") 

end 

``` 
<br>
<br>
<br>
| **bool IsScript()** |
| :--- |

스트립트인지 확인할 수 있어요. 
샘플

```lua

local cube = Workspace.Cube 

if cube:IsScript() == true then --오브젝트가 Script면 true를 반환해요. 

print(cube:GetName() .. " Is Script") 

end 

``` 
<br>
<br>
<br>
| **bool IsCollider()** |
| :--- |

Collider인지 확인할 수 있어요. 
샘플

```lua

local cube = Workspace.Cube 

if cube:IsCollider() == true then --오브젝트가 Collider면 true를 반환해요. 

print(cube:GetName() .. " Is Collider") 

end 

``` 
<br>
<br>
<br>
| **bool IsWidget()** |
| :--- |

Widget인지 확인할 수 있어요. 
샘플

```lua

local cube = Workspace.Cube 

if cube:IsWidget() == true then --오브젝트가 Widget면 true를 반환해요. 

print(cube:GetName() .. " Is Widget") 

end 

``` 
<br>
<br>
<br>
| **bool IsCamera()** |
| :--- |

Camera인지 확인할 수 있어요. 
샘플

```lua

local cube = Workspace.Cube 

if cube:IsCamera() == true then --오브젝트가 Camera면 true를 반환해요. 

print(cube:GetName() .. " Is Camera") 

end 

``` 
<br>
<br>
<br>
| **bool IsValid()** |
| :--- |

해당 오브젝트가 유효한지 확인 할 수있어요. 
<br>
<br>
<br>
| **AddReplicateValue(string ValueName, Vector Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 벡터를 추가해요. (추가할 Value 이름, Vector 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
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
<br>
| **AddReplicateValue(string ValueName, float Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 실수를 추가해요. (추가할 Value 이름, float 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
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
<br>
| **AddReplicateValue(string ValueName, bool Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 bool를 추가해요. (추가할 Value 이름, bool 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
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
<br>
| **AddReplicateValue(string ValueName, string Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 문자열을 추가해요. (추가할 Value 이름, string 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
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
<br>
| **AddReplicateValue(string ValueName, Color Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 컬러를 추가해요. (추가할 Value 이름, Color 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
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
<br>
| **AddSaveValue(string ValueName, Vector Data)** |
| :--- |

해당 객체 저장소에 벡터를 추가해요. (Value 이름, Vector 데이터) 
<br>
<br>
<br>
| **AddSaveValue(string ValueName, float Data)** |
| :--- |

해당 객체 저장소에 실수를 추가해요. (Value 이름, float 데이터) 
<br>
<br>
<br>
| **AddSaveValue(string ValueName, bool Data)** |
| :--- |

해당 객체 저장소에 bool을 추가해요. (Value 이름, bool 데이터) 
<br>
<br>
<br>
| **AddSaveValue(string ValueName, string Data)** |
| :--- |

해당 객체 저장소에 문자열을 추가해요. (Value 이름, string 데이터) 
<br>
<br>
<br>
| **AddSaveValue(string ValueName, Color Data)** |
| :--- |

해당 객체 저장소에 칼라를 추가해요. (Value 이름, Color 데이터) 
