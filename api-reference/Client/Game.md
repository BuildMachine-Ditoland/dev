
게임 전반적인 역할을 하는 객체에요. 여기 있는 기능들은 클라이언트에서만 사용할 수 있어요. 
## **이벤트**

| **ReceiveGameStatisticsDataEvent** |
| :--- |

서버로 부터 게임 통계 데이터 받았을 때 발생하는 이벤트에요. 
## **함수**





| **RModeRemotePlayer GetRemotePlayer(string PlayerName);** |
| :--- |

이름으로 플레이어를 얻을 수 있어요. (찾고싶은 플레이어 이름) 

샘플 

```lua
local player = LocalPlayer:GetRemotePlayer() --자신의 플레이어를 반환해요. 
```




| **RGameClientCharacter GetRemotePlayerCharacter(string PlayerName)** |
| :--- |

플레이어 이름으로 해당 플레이어의 캐릭터를 얻을 수 있어요. (캐릭터를 찾고싶은 플레이어 이름) 

샘플 

```lua
local character = Game:GetRemotePlayerCharacter(PlayerName) --플레이어 이름에 해당하는 캐릭터를 반환해요.
```




| **int GetPlayerCount** |
| :--- |

현재 게임에 참여하고 있는 플레이어의 수를 얻을 수 있어요. 

샘플 

```lua
print(Game:GetPlayerCount())
```




| **vector<Player> GetAllPlayer()** |
| :--- |

모든 플레이어 얻을 수 있어요. 

샘플 

```lua
local allPlayerList = Game:GetAllPlayer() --모든 플레이어를 리스트로 반환해요.
for i = 1, #allPlayerList do
    print(allPlayerList[i]:GetName())
end
```




| **SendEventToServer(string EventName, Args ... )** |
| :--- |

서버에 커스텀 이벤트를 보내는 함수에요. (이벤트 이름, 전달하고 싶은 변수들 ...) 

샘플 

```lua
--클라 스크립트에서
local cube = Workspace.Cube
wait(1)
cube:SendEventToServer("SomeFunc", 1) --자신 플레이어에게 SomeFunc() 함수를 호출해요. 
--서버 스크립트에서

local cube = Workspace.cube
local function SomeFunc(player, id) --첫 인자로 player가 들어가요.
                                    --필요하다면 함수의 인자도 넣을 수 있어요. 단, 숫자나 문자열 인자만 넣을 수 있어요.
    print("Call SomeFunc from " .. player:GetName() .. " (" .. id .. ")")
end
cube:ConnectEventFunction("SomeFunc", SomeFunc) --오브젝트에 "SomeFunc"라는 이벤트 이름으로 SomeFunc 함수를 연결해요.
                                                --오브젝트가 아닌 Game에도 연결할 수 있어요. 그러나 그룹과 폴더에는 연결할 수 없어요.
                                                --같은 대상에 등록된 이벤트만 호출할 수 있어요.
```




| **RModeSequenceAnimStateSetting AddAnimStateMachineSetting(string StateMachineName)** |
| :--- |

캐릭터에 사용될 애니메이션 상태머신 설정을 추가할 수 있어요. (설정할 상태머신 이름) 




| **RModeSequenceAnimStateSetting GetAnimStateMachineSetting(string StateMachineName)** |
| :--- |

설정된 애니메이션 상태머신을 얻을 수 있어요. (얻고 싶은 상태머신 이름) 




| **SetCharacterAnimStateMachine(RCharacterSetting CharacterSetting, RAnimStateMachineSetting AnimSetting)** |
| :--- |

해당 캐릭터 설정으로 생성되는 캐릭터의 애니메이션 상태 머신을 설정 할 수 있어요. (대상 캐릭터 설정, 사용 할 애니메이션 상태 설정) 




| **SetNPCAnimStateMachine(string NPCSettingName, string AnimStateMachineSettingName)** |
| :--- |

해당 NPC의 애니메이션 상태 머신 사용하게 할 수 있어요. (설정한 NPC 이름, 애니메이션 상태 머신 이름) 




| **ObjectFXClient CreateFX(ObjectFXClient FXObject, Vetor Location)** |
| :--- |

FX를 생성할 수 있어요. (생성 할 FX 오브젝트, 생성할 위치) 

샘플 

```lua
local spawnPos = Workspace.Cube:GetTransform():GetLocation()
Game:CreateFX(Workspace.Effect, spawnPos) --이펙트를 지정 위치에 생성해요.
```




| **DeleteFX(ObjectFXClient Object)** |
| :--- |

FX를 제거시켜요. (제거할 FX 오브젝트) 

샘플 

```lua
Game:DeleteFX(Workspace.Effect)   
```




| **ObjectSoundClient PlaySound(ObjectSoundClient SoundObject, Vetor Location)** |
| :--- |

사운드를 플레이해요. (플레이 할 Sound 오브젝트, 플레이 할 위치 Vector) 

샘플 

```lua
Game:PlaySound(Workspace.Sound, Vector.new(0, 0, 0))
```

플레이 중인 사운드를 정지시켜요. (정지할 Sound) 




| **CreateObject(RScriptWorldObject Object, Vector Location)** |
| :--- |

지정된 위치에 오브젝트를 생성 시켜요. (생성 할 Object, 생성 할 위치 Vector) 

샘플 

```lua
local cube = Workspace.Cube
local createPos = Vector.new(0, 0, 0)
local temp = Game:CreateObject(cube, createPos) --오브젝트를 지정된 위치에 생성해요. (생성한 클라이언트에서만 보여요.)
print(temp:GetName()) --CreateObject로 생성한 오브젝트를 변수에 담은 뒤 후처리할 수 있어요.
```




| **CreateUIScene(RScriptUISceneClient Source)** |
| :--- |

Source와 같은 UIScene을 생성한다. 

샘플 

```lua
local uiScene = Game:CreateUIScene(Workspace.ScreenUI) --대상 UI를 복제해요.
print(uiScene:GetName())
```




| **CreateUIScene(string UISceneName, RScriptUISceneClient Source)** |
| :--- |

Source와 같은 UIScene을 생성 후, UISceneName을 생성된 오브젝트 이름으로 설정한다. (생성할 오브젝트의 이름 UISceneName, 생성 할 오브젝트 Source) 

샘플 

```lua
local uiScene = Game:CreateUIScene("NewScreenUI", Workspace.ScreenUI) --새로운 이름으로 대상 UI를 복제해요.
print(uiScene:GetName())
```




| **Vector GetMouseHitLocation()** |
| :--- |

자신의 마우스 2D 위치에서 월드에 충돌된 3D위치 좌표를 얻을 수 있어요. 

샘플 

```lua
Input:AddGroup("MouseInput")
Input:AddActionKeyEvent("MouseInput", "ClickKey", Enum.Key.LeftMouseButton)
Input:ActiveGroup("MouseInput")

LocalPlayer:ProcessInputActionEvent("ClickKey", Enum.KeyInputType.Released, function()
    local pos = Game:GetMouseHitLocation() --마우스를 클릭한 위치를 Vector로 반환해요.
    print("Click Position : " .. pos)
end
```




| **Object GetMouseHitObject()** |
| :--- |

자신의 마우스 2D 위치에서 월드에 충돌된 Object를 얻어 올 수 있어요. 

샘플 

```lua
while true do
    local hitObj = Game:GetMouseHitObject() --마우스 커서 위치에 해당하는 오브젝트를 반환해요.
    if hitObj ~= nil then
        print(hitObj:GetName())
    else
        print("nil")
    end
    wait(0.5)
end
```
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

| **OnUpdateEvent** |
| :--- |
매 프레임마다 호출되는 이벤트에요.
샘플

```lua
local cube = Workspace.Cube
local playTime = 0
local function UpdateEvent(updateTime) --OnUpdateEvent로 연결된 함수는 updateTime 인자가 고정적으로 들어가요.
    playTime = playTime + updateTime --시간을 기록해요.
end
cube.OnUpdateEvent:Connect(UpdateEvent) --Game이나 오브젝트에 매프레임마다 호출되는 함수를 연결해요.
```
| **OnEnterPlayer** |
| :--- |
플레이어가 게임에 입장 시 호출되는 이벤트에요.
샘플

```lua
local function EnterPlayer(player) --OnEnterPlayer로 연결된 함수는 player 인자가 고정적으로 들어가요.
    print("Enter " .. player:GetName()) 
end
Game.OnEnterPlayer:Connect(EnterPlayer) --Game에 플레이어가 게임에 입장하면 호출되는 함수를 연결해요.
```
| **OnLeavePlayer** |
| :--- |
플레이어가 게임에서 나갈 때 호출되는 이벤트에요.
샘플

```lua
local function LeavePlayer(player) --OnLeavePlayer로 연결된 함수는 player 인자가 고정적으로 들어가요.
    print("Leave " .. player:GetName()) 
end
Game.OnLeavePlayer:Connect(LeavePlayer) --Game에 플레이어가 게임을 종료하면 호출되는 함수를 연결해요.
```
| **OnDeathCharacter** |
| :--- |
케릭터가 죽을 때 호출되는 이벤트에요.
샘플

```lua
local function DeathCharacter(character) --OnDeathCharacter로 연결된 함수는 character 인자가 고정적으로 들어가요.
    print("Death " .. character:GetName()) 
end
Game.OnDeathCharacter:Connect(DeathCharacter) --Game에 캐릭터가 죽으면 연결된 호출되는 함수를 연결해요.
```
| **OnSpawnCharacter** |
| :--- |
케릭터가 스폰 될 때 호출되는 이벤트에요.
샘플

```lua
local function SpawnCharacter(character) --OnSpawnCharacter로 연결된 함수는 character 인자가 고정적으로 들어가요.
    print("Spawn " .. character:GetName()) 
end
Game.OnSpawnCharacter:Connect(SpawnCharacter) --Game에 캐릭터가 생성되면 연결된 호출되는 함수를 연결해요.
```
샘플

```lua
local function EnterPlayer(Player)
	local Character = Player:GetCharacter()
	local PlayerName = Character:GetPlayerName()
	print(PlayerName.." Join Game !")
end
--게임에 플레이어가 들어올 시 EnterPlayer함수에 연결
Game.OnEnterPlayer:Connect(EnterPlayer)
```
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
| **AddTimeEvent(String EventName, float Time, LuaScriptFunction EventFuunction)** |
| :--- |
일정 시간뒤에 연결 함수가 호출되는 이벤트를 추가해요. (추가할 이벤트 이름, 시간, 연결 함수)
샘플

```lua
local waitTime = 2
local function PrintMessage() --AddTimeEvent로 등록된 함수는 일정시간을 기다린뒤, 호출돼요.
    print("Call PrintMessage!") 
end
Game:AddTimeEvent("PrintMessage", waitTime, PrintMessage) --일정시간을 기다린뒤 호출되는 함수를 문자열로 등록해요.
```
| **DeleteTimeEvent(String EventName)** |
| :--- |
등록된 시간 이벤트를 삭제해요. (삭제할 이벤트 이름)
샘플

```lua
local waitTime = 2
local function PrintMessage() --AddTimeEvent로 등록된 함수는 일정시간을 기다린뒤, 호출돼요.
    print("Call PrintMessage!") 
end
Game:AddTimeEvent("PrintMessage", waitTime, PrintMessage) --일정시간을 기다린뒤 호출되는 함수를 문자열로 등록해요.
Game:DeleteTimeEvent("PrintMessage") --AddTimeEvent로 등록한 함수를 삭제해서 호출되지 않게 해요.
```
## **함수**

| **RModePhase AddPhase(string phasename)** |
| :--- |
게임에 단계를 추가할 수 있어요. (추가할 단계 이름)
샘플

```lua
--서버 스크립트에서-------------
local LobbyState = Game:AddPhase("Lobby") --사용할 Phase를 등록해요.
local PlayState = Game:AddPhase("Play") --Phase는 여러개도 등록할 수 있어요.
local ResultState = Game:AddPhase("Result")
Game:AddReplicateValue("GameState", "Lobby", Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.

--각 Phase로 전환되었을때 처리할 이벤트 함수를 추가해요.
local function EnterLobbyState()
    Game.GameState = "Lobby" 
    print("Enter Lobby State")
end
LobbyState.EnterEvent:Connect(EnterLobbyState) --해당 Phase로 변경됐을때 호출되는 이벤트를 연결해요.

local function UpdateLobbyState(UpdateTime)                    
    print("Update Lobby State")
end
LobbyState.UpdateEvent:Connect(UpdateLobbyState)  --해당 Phase일때 매프레임마다 호출되는 이벤트를 연결해요.

local function ExitLobbyState()
    print("End Lobby State")
end
LobbyState.ExitEvent:Connect(ExitLobbyState) --해당 Phase가 끝날때 호출되는 이벤트를 연결해요.

local function EnterPlayState()
    Game.GameState = "Play" 
    print("Enter Play State")
end
PlayState.EnterEvent:Connect(EnterPlayState)

local function EnterResultState()
    Game.GameState = "Result" 
    print("Enter Result State")
end
ResultState.EnterEvent:Connect(EnterResultState)

wait(1)
Game:ChangePhaseByName("Game") --이름으로 Phase를 전환해요.
wait(1)
Game:ChangeToNextPhase() --다음 Phase로 전환해요. (만약 마지막 Phase면 처리되지 않아요.)
     
--클라 스크립트에서-------------
local LobbyState = Game:AddPhase("Lobby") --서버 스크립트에서 추가한 Phase를 똑같이 등록해요.
local PlayState = Game:AddPhase("Play") 
local ResultState = Game:AddPhase("Result")

--각 Phase로 전환되었을때 처리할 이벤트 함수를 추가해요.
--서버 스크립트와 동일하게 작성하되, Game.GameState = "Lobby" 같은 Phase 변경은 제외해요. (서버에서만 처리해야 해요.)
local function EnterLobbyState()     
    print("Enter Lobby State")
end
LobbyState.EnterEvent:Connect(EnterLobbyState)

local function EnterPlayState()
    print("Enter Play State")
end
PlayState.EnterEvent:Connect(EnterPlayState)

local function EnterResultState()
    print("Enter Result State")
end
ResultState.EnterEvent:Connect(EnterResultState)

--스크립트 제일 아래에 상태가 바뀔때마다 관련된 Phase 함수가 호출될 수 있도록 연결해요.
Game:ConnectChangeEventFunction("GameState", function() 
    Game:ChangePhaseByName(Game.GameState) 
end)
```
| **RModePhase GetPhaseByName(string phasename)** |
| :--- |
단계 이름으로 단계를 불러올 수 있어요. (불러올 단계 이름)
| **RModePhase GetCurPhase()** |
| :--- |
현재 단계를 얻을 수 있어요.
| **RModePhase ChangePhaseByName(string changephasename)** |
| :--- |
단계 이름을 통해 해당 단계로 변경할 수 있어요. (변경할 단계 이름)
| **RModePhase ChangeToNextPhase()** |
| :--- |
다음 단계로 변경할 수 있어요.
| **ConnectEventFunction(string customevent, LuaScriptFunction function) ** |
| :--- |
유저가 추가한 이벤트에 함수를 연결할 수 있어요. (이벤트 이름, 연결 함수)
샘플

```lua
local cube = Workspace.cube
local function SomeFunc(playerName) --필요하다면 함수의 인자도 넣을 수 있어요. 단, 숫자나 문자열 인자만 넣을 수 있어요.
    print("Call SomeFunc from " .. playerName)
end
cube:ConnectEventFunction("SomeFunc", SomeFunc) --오브젝트에 "SomeFunc"라는 이벤트 이름으로 SomeFunc 함수를 연결해요.
                                                --오브젝트가 아닌 Game에도 연결할 수 있어요. 그러나 그룹과 폴더에는 연결할 수 없어요.
                                                --같은 대상에 등록된 이벤트만 호출할 수 있어요.
```
| **float GetPassTime()** |
| :--- |
단계가 진행된 시간을 얻을 수 있어요.
| **DeleteObject(RScriptWorldObject)** |
| :--- |
오브젝트를 삭제할 수 있어요. (삭제할 오브젝트)
서버에서 사용하면 서버와 클라 오브젝트 모두 삭제되고 클라에서 사용하면 클라 오브젝트만 삭제해요
샘플

```lua
local cube = Workspace.Cube
Game:DeleteObject(cube) --오브젝트를 파괴해요.
```
| **List<HitResult> LineTraceList(Vector Start, Vector Dir, float Distance)** |
| :--- |
설정된 시작 지점에서 원하는 방향으로 지정된 거리 만큼의 충돌 리스트들을 가져올 수 있어요. (시작 지점 Vector, 목표 지점 Vector, 거리 값)
샘플

```lua
local startPos = Workspace.Cube
local dir = Vector.new(0, 1, 0)
local distance = 100
local targetList = Game:LineTraceList(startPos, dir, distance) --시작 위치에서 특정 방향으로 거리만큼의 충돌 리스트가 반환돼요.
for i = 1, #targetList do 
    print("Left " .. targetList[i].HitObject:GetName()) 
end
```
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
Camera인지 확인할 수 있어요.
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
해당 객체에 서버, 클라이언트 간 동기화가 가능한 벡터를 추가해요. (추가할 Value 이름, Vector 데이터, //@[] Enum.ReplicateType.타입 https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype , 동기화 시간, 스토리지 저장 여부)
샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeVector", Vector.new(0, 50, 0), Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeVector)

--클라 스크립트에서-------------
print(Game.SomeVector) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
| **AddReplicateValue(string ValueName, float Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |
해당 객체에 서버, 클라이언트 간 동기화가 가능한 실수를 추가해요. (추가할 Value 이름, float 데이터, //@[] Enum.ReplicateType.타입 https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype , 동기화 시간, 스토리지 저장 여부)
샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeNumber", 1, Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeNumber .. " in Server")

--클라 스크립트에서-------------
print(Game.SomeNumber .. " in Client") --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
| **AddReplicateValue(string ValueName, bool Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |
해당 객체에 서버, 클라이언트 간 동기화가 가능한 bool를 추가해요. (추가할 Value 이름, bool 데이터, //@[] Enum.ReplicateType.타입 https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype , 동기화 시간, 스토리지 저장 여부)
샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeBool", true, Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeBool)

--클라 스크립트에서-------------
print(Game.SomeBool) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
| **AddReplicateValue(string ValueName, string Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |
해당 객체에 서버, 클라이언트 간 동기화가 가능한 문자열을 추가해요. (추가할 Value 이름, string 데이터, //@[] Enum.ReplicateType.타입 https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype , 동기화 시간, 스토리지 저장 여부)
샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeString", "Hello World!", Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeString)

--클라 스크립트에서-------------
print(Game.SomeString) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
| **AddReplicateValue(string ValueName, Color Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |
해당 객체에 서버, 클라이언트 간 동기화가 가능한 컬러를 추가해요. (추가할 Value 이름, Color 데이터, //@[] Enum.ReplicateType.타입 https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype , 동기화 시간, 스토리지 저장 여부)
샘플

```lua
--서버 스크립트에서-------------
Game:AddReplicateValue("SomeColor", Color.new(255, 0, 0, 255), Enum.ReplicateType.Changed, 0, false) --서버와 클라이언트간 동기화되는 값을 등록하고 초기값을 설정한뒤, 값이 변경될때마다 호출되게 해요.
print(Game.SomeColor)

--클라 스크립트에서-------------
print(Game.SomeColor) --서버에서 값이 바뀌었지만 클라에서도 동일하게 출력돼요.
```
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
