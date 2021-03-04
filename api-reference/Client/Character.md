
클라이언트에서 사용되는 캐릭터에 대한 개체에요. 
## **함수**

| **Player GetPlayer()** |
| :--- |

해당 캐릭터의 플레이어를 얻을 수 있어요. 

샘플 

```lua
local character = Game:GetAllPlayer()[1]:GetCharacter()
local player = character:GetPlayer() --캐릭터의 플레이어를 반환해요.
```
| **string GetPlayerName()** |
| :--- |

플레이어의 이름을 얻을 수 있어요. 

샘플 

```lua
local character = Game:GetAllPlayer()[1]:GetCharacter()
print(character:GetPlayerName()) --캐릭터의 플레이어 이름을 문자열로 반환해요.
```
| **bool IsDriving()** |
| :--- |

캐릭터가 탈 것을 운전 중인지 아닌지 얻을 수 있어요. 
| **ObjectFXClient CreateFX(ObjectFXClient FXObject, Bone BoneType)** |
| :--- |

캐릭터 특정 위치에 FX를 생성할 수 있어요. (생성 하고싶은 FX 오브젝트, [Enum.BoneType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/bone)) 

샘플 

```lua
local character = LocalPlayer:GetRemotePlayer():GetCharacter()
character:CreateFX(Workspace.Effect, Enum.Bone.Body) --캐릭터의 특정 부위에 이펙트를 생성해요.
```
| **ObjectSoundClient CreateSound(ObjectSoundClient SoundObject)** |
| :--- |

캐릭터의 위치에 Sound를 생성할 수 있어요. (생성 하고싶은 Sound 오브젝트) 
| **AddPlayerHUD(string UIName, UISceen UI, UIDisplayType Type)** |
| :--- |

UI HUD를 붙일 수 있어요. (붙혀 질 UI 이름, 붙일 UI Sceen, UI DisplayType.) 

샘플 

```lua
local playerNameUI = HUD.PlayerNameUI
playerNameUI:SetVisible(false)

local function spawn(character)
   local ui = character:AddPlayerHUD("Name", playerNameUI, Enum.UIDisplayType.Billboard) --캐릭터에 HUD를 추가하고 이름으로 등록해요.
   ui:SetVisible(true)
end
Game.OnSpawnCharacter:Connect(spawn)
```
| **RemovePlayerHUD(string UIName)** |
| :--- |

UI HUD를 제거해요. (제거하고 싶은 UI 이름) 
| **RemovePlayerAllHUD()** |
| :--- |

현재 캐릭터의 모든 UI HUD를 제거해요. 
| **GetPlayerHUD(string UIName)** |
| :--- |

UI HUD를 얻을 수 있어요. (얻고싶은 UI 이름) 

샘플 

```lua
local character = LocalPlayer:GetRemotePlayer():GetCharacter()
local playerNameUI = character:GetPlayerHUD("Name") --캐릭터에 추가된 HUD를 이름으로 찾아서 반환해요.                      
playerNameUI.Text:SetTextColor(Color.new(255, 0, 0, 255)) 
```
| **bool IsMyCharacter()** |
| :--- |

플레이어 자신의 캐릭터인지 아닌지 확인할 수 있어요. 

샘플 

```lua
local character = LocalPlayer:GetRemotePlayer():GetCharacter() 
if character:IsMyCharacter() then --캐릭터가 자신의 캐릭터이면 true를 반환해요.
    print("My Character!") 
end
```
| **void AttachAt(RModeObject ModeObject, BoneType Bone)** |
| :--- |

캐릭터의 원하는 본을 해당 오브젝트의 중점에 부착시켜요. (부착 할 오브젝트, [Enum.Bone.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/bone)) 
| **void AttachAtTop(RModeObject ModeObject, BoneType Bone)** |
| :--- |

캐릭터의 원하는 본을 해당 오브젝트의 윗면에 부착시켜요. (부착 할 오브젝트, [Enum.Bone.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/bone)) 
# **상속받아 사용 가능한 기능들**

## **속성**

| **Parent** |
| :--- |

부모 객체를 얻을 수 있어요. 

샘플 

```lua

local parent = Workspace.Floor.Parent --오브젝트의 부모를 반환해요 

print(parent:GetName())  

``` 
## **이벤트**

| **ConnectChangeEventFunction(string ValueName, function FunctionName)** |
| :--- |

추가된 값이 변경 될 때 호출되는 이벤트에요. (Value 이름, 연결 함수) 

샘플 

```lua

local function ChangeCurBullet(value) 

Logger:Log(“Hello”) 

end 

 

-- Object의 "CurBullet" 라는 Value가 변경되면 ChangeCurBullet 함수에 연결 

Object:ConnectChangeEventFunction("CurBullet", LuaScriptFunction ChangeCurBullet)   

``` 
| **AddTimeEvent(String EventName, float Time, LuaScriptFunction EventFuunction)** |
| :--- |

일정 시간뒤에 연결 함수가 호출되는 이벤트를 추가해요. (추가할 이벤트 이름, 시간, 연결 함수) 
| **DeleteTimeEvent(String EventName)** |
| :--- |

등록된 시간 이벤트를 삭제해요. (삭제할 이벤트 이름) 
## **함수**

| **string GetName()** |
| :--- |

객체의 이름을 얻을 수 있어요. 

샘플 

```lua

print(Workspace.Floor:GetName()) --오브젝트의 이름을 문자열로 반환해요. 

``` 
| **RModeObject GetParent(string ParentName)** |
| :--- |

이름으로 부모 객체를 얻을 수 있어요. (찾고싶은 부모 객체 이름) 
| **RModeObject GetChild(string ChildName)** |
| :--- |

이름으로 자식 객체를 얻을 수 있어요. (찾고싶은 자식 객체 이름) 
| **RModeObject GetGetSibling(string Name)** |
| :--- |

이름으로 형제 객체를 얻을 수 있어요. (찾고싶은 형제 객체 이름) 
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
| **bool IsCamera()** |
| :--- |

Widget인지 확인할 수 있어요. 

샘플 

```lua

local cube = Workspace.Cube 

if cube:IsCamera() == true then --오브젝트가 Camera면 true를 반환해요. 

print(cube:GetName() .. " Is Camera") 

end 

``` 
| **bool IsValid()** |
| :--- |

해당 오브젝트가 유효한지 확인 할 수있어요. 
| **AddReplicateValue(string ValueName, Vector Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 벡터를 추가해요. (추가할 Value 이름, Vector 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, float Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 실수를 추가해요. (추가할 Value 이름, float 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, bool Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 bool를 추가해요. (추가할 Value 이름, bool 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, string Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 문자열을 추가해요. (추가할 Value 이름, string 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, Color Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화가 가능한 컬러를 추가해요. (추가할 Value 이름, Color 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddSaveValue(string ValueName, Vector Data)** |
| :--- |

해당 객체 저장소에 벡터를 추가해요. (Value 이름, Vector 데이터) 
| **AddSaveValue(string ValueName, float Data)** |
| :--- |

해당 객체 저장소에 실수를 추가해요. (Value 이름, float 데이터) 
| **AddSaveValue(string ValueName, bool Data)** |
| :--- |

해당 객체 저장소에 bool을 추가해요. (Value 이름, bool 데이터) 
| **AddSaveValue(string ValueName, string Data)** |
| :--- |

해당 객체 저장소에 문자열을 추가해요. (Value 이름, string 데이터) 
| **AddSaveValue(string ValueName, Color Data)** |
| :--- |

해당 객체 저장소에 칼라를 추가해요. (Value 이름, Color 데이터) 
