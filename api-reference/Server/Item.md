
서버에서 사용되는 Item 객체에요. 
# **상속받아 사용 가능한 기능들**

## **속성**

| **Parent** |
| :--- |

부모 객체를 얻을 수 있어요. 
## **이벤트**

| **UseEvent** |
| :--- |

아이템 사용 시 호출되는 이벤트에요. 
| **EquipEvent** |
| :--- |

아이템 장착 시 호출되는 이벤트에요. 
| **UnEquipEvent** |
| :--- |

아이템 탈착 시 호출되는 이벤트에요. 
| **OnCreateEvent** |
| :--- |

생성 시 호출되는 이벤트에요. 
| **OnUpdateEvent** |
| :--- |

생성 후 매 프레임마다 호출되는 이벤트에요. 
| **OnDestroyEvent** |
| :--- |

삭제될 때 호출되는 이벤트에요. 
| **OnCollisionEvent** |
| :--- |

다른 객체와 충돌할 때 호출되는 이벤트에요. 
| **OnBeginOverlapEvent** |
| :--- |

다른 객체와 겹쳐질 때 호출되는 이벤트에요. 
| **OnEndOverlapEvent** |
| :--- |

다른 객체와 겹쳐짐이 끝날 때 호출되는 이벤트에요. 
| **OnOverlapUpdateEvent** |
| :--- |

다른 객체와 겹쳐있는 동안 매 프레임마다 호출되는 이벤트에요. 
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
## **함수**

| **float GetItemCount()** |
| :--- |

아이템의 개수를 얻을 수 있어요. 
| **float GetActionCoolTime()** |
| :--- |

아이템의 액션 시간을 얻을 수 있어요. 
| **void SetActionCoolTime(float Time)** |
| :--- |

아이템의 액션 시간을 설정할 수 있어요. (설정하고 싶은 시간) 
| **string GetEquipSlot()** |
| :--- |

해당 아이템의 장착 슬롯을 가져올 수 있어요. 
| **RResourceID GetIconImg()** |
| :--- |

아이템의 아이콘 이미지를 얻을 수 있어요. 
| **AddAction(string ActionName, LuaScriptFunction Function)** |
| :--- |

아이템 착용 후 액션을 추가해요. (액션 이름, 연결 함수) 
| **AddToggleAction(string ActionName, LuaScriptFunction StartFunction, LuaScriptFunction EndFunction)** |
| :--- |

아이템 착용 후 토글 액션을 추가해요. (액션 이름, 액션 시작 시 연결 함수, 액션 종료 시 연결 함수) 
| **SetCollisionType(string usercollisiontype)** |
| :--- |

해당 오브젝트의 충돌 타입을 지정해줘요. 

[Game:AddUserCollisionType](https://ditoland-utplus.gitbook.io/ditoland/api-reference/server/game)으로 추가한 타입만 가능해요 없을 시에는 기본 타입으로 지정되요 
| **SetCharacterCollisionResponse(ECollisionResponse CollisionResponse)** |
| :--- |

캐릭터와 충돌 시 어떻게 처리 할지를 설정하는 함수에요. ( [Enum.CollisionResponse.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/collisionresponse)) 
| **SetUserCollisionTypeResponse(string UserCollisionType, ECollisionResponse CollisionResponse)** |
| :--- |

유저타입 충돌 물체의 충돌 시 처리를 변경하는 함수에요. (변경 할 유저타입 충돌 이름, [Enum.CollisionResponse.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/collisionresponse)) 
| **SetReplicatePriority(int priority)** |
| :--- |

서버에서 클라로 얼마나 많이 동기화 할것인지에 대한 값을 설정할 수 있어요. (우선 순위 값) 
| **int GetModeObjectKey()** |
| :--- |

객체의 키 값을 얻을 수 있어요. 
| **Matrix GetTransform()** |
| :--- |

매트릭스를 얻을 수 있어요. 
| **SetTransform(Matrix)** |
| :--- |

매트릭스를 설정할 수 있어요. (Matrix 값, bool 충돌 처리 여부) 
| **Teleport(Matrix)** |
| :--- |

매트릭스를 설정할 수 있어요. (Matrix 값) 
| **Vector GetLocation()** |
| :--- |

(Deprecated)객체의 현재 위치를 얻을 수 있어요. 
| **SetLocation(Vector position, bool collisionCheck)** |
| :--- |

(Deprecated)객체의 위치를 설정할 수 있어요. (설정할 위치 Vector 값, 충돌 처리 여부) 
| **Vector GetRotation()** |
| :--- |

(Deprecated)각도를 얻을 수 있어요. (Vector.X : Pitch, Vector.Y : Yaw, Vector.Z : Roll) 
| **SetRotation(Vector InValue)** |
| :--- |

(Deprecated)주어진 값으로 각도를 설정해요. (InValue.X : Roll, InValue.Y : Pitch, InValue.Z : Yaw) 
| **Vector GetScale()** |
| :--- |

(Deprecated)스케일을 얻을 수 있어요 
| **SetScale(Vector scale)** |
| :--- |

(Deprecated)주어진 값으로 스케일을 설정해요. (설정할 스케일 값) 
| **SetTag(String Tag)** |
| :--- |

객체의 tag를 설정해요. (설정할 tag) 
| **String GetTag()** |
| :--- |

객체에 설정된 tag를 얻을 수 있어요. 
| **SetForward(Vector Forward)** |
| :--- |

(Deprecated)객체의 바라보는 방향을 설정할 수 있어요. (설정할 방향 Vector 값) 
| **Vector GetForward()** |
| :--- |

(Deprecated)객체의 바라보는 방향을 얻을 수 있어요. 
| **Vector GetRight()** |
| :--- |

(Deprecated)객체의 오른쪽 방향을 얻을 수 있어요. 
| **AddForce(Vector Force)** |
| :--- |

객체에 물리 힘을 추가할 수 있어요. (힘을 가할 Vector 값) 
| **SetVisibility(bool bNewVisibility)** |
| :--- |

객체의 가시성 여부를 설정할 수 있어요. (가시성 여부) 
| **AddLocalMove(string TrackName, Vector Pos, float Time, bool CheckCollision)** |
| :--- |

로컬 좌표를 기준으로 이동 변화를 추가할 수 있어요. (설정할 Track 이름, 이동 변화를 줄 값, 완료까지 걸리는 시간, 충돌 처리 여부) 
| **AddLocalRot(string TrackName, Vector Rot, float Time)** |
| :--- |

로컬 좌표를 기준으로 회전 변화를 추가할 수 있어요. (설정할 Track 이름, 회전 변화를 줄 값, 완료까지 걸리는 시간) 
| **AddLocalScale(string TrackName, Vector Scale, float Time)** |
| :--- |

로컬 좌표를 기준으로 스케일 변화를 추가할 수 있어요. (설정할 Track 이름, 스케일 변화를 줄 값, 완료까지 걸리는 시간) 
| **AddWorldMove(string TrackName, Vector Pos, float Time, bool CheckCollision)** |
| :--- |

월드 좌표를 기준으로 이동 변화를 추가할 수 있어요. (설정할 Track 이름, 이동 변화를 줄 값, 완료까지 걸리는 시간, 충돌 처리 여부) 
| **AddWorldRot(string TrackName, Vector Rot, float Time)** |
| :--- |

월드 좌표를 기준으로 회전 변화를 추가할 수 있어요. (설정할 Track 이름, 회전 변화를 줄 값, 완료까지 걸리는 시간) 
| **AddEmpty(string TrackName, float Time)** |
| :--- |

객체 변환에 대기 시간을 추가할 수 있어요. (추가할 Track 이름, 대기 시간) 
| **PlayTransformTrack(string TrackName, TransformPlayType Type, int PlayCount)** |
| :--- |

설정된 변환 컨트롤러를 실행시켜요. (실행할 Track 이름, [Enum.TransformPlayType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/transformplaytype), 실행 횟수) 
| **StopTransformTrack(string TrackName)** |
| :--- |

변환 컨트롤러를 정지시켜요. (정지할 Track 이름) 
| **PauseTransformTrack(string TrackName)** |
| :--- |

변환 컨트롤러를 일시 정지시켜요 (일시 정지할 Track 이름) 
| **ResumeTransformTrack(string TrackName)** |
| :--- |

변환 컨트롤러를 다시 플레이시켜요. (플레이할 Track 이름) 
| **bool IsPlayingTransformTrack(string TrackName)** |
| :--- |

해당 TransformTrack이 플레이 중인지 확인할 수 있어요. (확인할 Track 이름) 
| **ResetTransformTrack(string TrackName)** |
| :--- |

해당 TransformTrack 이 적용되기 전의 Transform으로 리셋시켜요. (리셋할 Track 이름) 
| **RemoveTransformTrack(String TrackName)** |
| :--- |

해당 Track을 제거해요. (제거할 Track 이름) 
| **ResetTransform()** |
| :--- |

TransformTrack 이 적용되기 전의 최초 Transform으로 리셋시켜요. 
| **SetFriction( float value, float restitution, float density )** |
| :--- |

오브젝트의 표면 물리 마찰력을 설정할 수 있어요. (마찰 값, 탄성 값, 밀도 값) 
| **MakeVehicleChassis( VehicleCreationInfo Info )** |
| :--- |

오브젝트를 VehicleChassis로 변경시켜요. (변경할 [VehicleCreationInfo데이터](https://ditoland-utplus.gitbook.io/ditoland/api-reference/common/vehiclecreationinfo)) 
| **SetName(string NewName)** |
| :--- |

오브젝트의 이름을 변경 할 수 있어요. (새로운 이름) 
| **FRModeVehicle GetVehicle()** |
| :--- |

Vehicle 객체를 얻을 수 있어요. 
| **string GetName()** |
| :--- |

객체의 이름을 얻을 수 있어요. 
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
| **bool IsCharacter()** |
| :--- |

캐릭터인지 확인할 수 있어요. 
| **bool IsStaticMesh()** |
| :--- |

스테틱 메시인지 확인할 수 있어요. 
| **bool IsFX()** |
| :--- |

FX인지 확인할 수 있어요. 
| **bool IsSound()** |
| :--- |

Sound인지 확인할 수 있어요. 
| **bool IsPointLight()** |
| :--- |

포인트 라이트인지 확인할 수 있어요. 
| **bool IsSpotLight()** |
| :--- |

스포트 라이트인지 확인할 수 있어요. 
| **bool IsSurfaceUI()** |
| :--- |

서피스 UI인지 확인할 수 있어요. 
| **bool IsScreenUI()** |
| :--- |

스크린 UI인지 확인할 수 있어요. 
| **bool IsItem()** |
| :--- |

아이템인지 확인할 수 있어요. 
| **bool IsNPC()** |
| :--- |

NPC인지 확인할 수 있어요. 
| **bool IsFolder()** |
| :--- |

폴더인지 확인할 수 있어요. 
| **bool IsScript()** |
| :--- |

스트립트인지 확인할 수 있어요. 
| **bool IsCollider()** |
| :--- |

Collider인지 확인할 수 있어요. 
| **bool IsWidget()** |
| :--- |

Widget인지 확인할 수 있어요. 
| **bool IsCamera()** |
| :--- |

Widget인지 확인할 수 있어요. 
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
