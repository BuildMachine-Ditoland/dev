# **RScriptWorldObject**


스크립트로 제공되는 월드 객체(월드 트리 오브젝트)에요. 
## **이벤트**

| **OnCreateEvent** |
| :--- |

생성 시 호출되는 이벤트 
| **OnUpdateEvent** |
| :--- |

생성 후 매 프레임에 호출되는 이벤트 
| **OnDestoryEvent** |
| :--- |

삭제될 때 호출되는 이벤트 
| **OnCollisionEvent** |
| :--- |

다른 객체와 충돌할 때 호출되는 이벤트 
| **OnBeginOverlapEvent** |
| :--- |

다른 객체와 겹쳐질 때 호출되는 이벤트 
| **OnEndOverlapEvent** |
| :--- |

다른 객체와 겹쳐짐이 끝날 때 호출되는 이벤트 
| **OnOverlapUpdateEvent** |
| :--- |

다른 객체와 겹쳐있는 동안 매 프레임 호출되는 이벤트 
## **함수**

| **int GetModeObjectKey()** |
| :--- |

객체 키 값 얻기 
| **Matrix GetTransform()** |
| :--- |

매트릭스 얻기 
| **SetTransform(Matrix)** |
| :--- |

매트릭스 설정 (Matrix 값) 
| **Vector GetLocation()** |
| :--- |

위치 얻기 
| **SetLocation(Vector position, bool collisionCheck)** |
| :--- |

위치 설정 (위치 Vector 값, 충돌 처리 여부) 
| **SetForward(Vector Forward)** |
| :--- |

바라보는 방향 설정 (방향 Vector 값) 
| **AddForce(Vector Force)** |
| :--- |

물리 힘 추가 (힘을 가할 Vector 값) 
| **SetVisibility(bool bNewVisibility)** |
| :--- |

가시성 설정 (가시성 여부) 
| **AddLocalMove(string TrackName, Vector Pos, float Time, bool CheckCollision)** |
| :--- |

로컬 좌표 기준으로 이동 변화를 추가한다. (Track 이름, 이동 변화를 줄 값, 완료까지 걸리는 시간, 충돌 처리 여부) 
| **AddLocalRot(string TrackName, Vector Rot, float Time)** |
| :--- |

로컬 좌표 기준으로 회전 변화를 추가한다. (Track 이름, 회전 변화를 줄 값, 완료까지 걸리는 시간) 
| **AddLocalScale(string TrackName, Vector Scale, float Time)** |
| :--- |

로컬 좌표 기준으로 스케일 변화를 추가한다. (Track 이름, 스케일 변화를 줄 값, 완료까지 걸리는 시간) 
| **AddWorldMove(string TrackName, Vector Pos, float Time, bool CheckCollision)** |
| :--- |

월드 좌표 기준으로 이동 변화를 추가한다. (Track 이름, 이동 변화를 줄 값, 완료까지 걸리는 시간, 충돌 처리 여부) 
| **AddWorldRot(string TrackName, Vector Rot, float Time)** |
| :--- |

월드 좌표 기준으로 회전 변화를 추가한다. (Track 이름, 회전 변화를 줄 값, 완료까지 걸리는 시간) 
| **AddEmpty(string TrackName, float Time)** |
| :--- |

객체 변환의 대기 시간을 추가한다. (Track 이름, 대기 시간) 
| **PlayTransformTrack(string TrackName, TransformPlayType Type, int PlayCount)** |
| :--- |

설정된 변환 컨트롤러 실행 (Track 이름, [Enum.TransformPlayType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/transformplaytype), 실행 횟수) 
| **StopTransformTrack(string TrackName)** |
| :--- |

변환 컨트롤러 정지 (Track 이름) 
| **PauseTransformTrack(string TrackName)** |
| :--- |

변환 컨트롤러 일시 정지 (Track 이름) 
| **ResumeTransformTrack(string TrackName)** |
| :--- |

변환 컨트롤러 다시 플레이 (Track 이름) 
| **bool IsPlayingTransformTrack(string TrackName)** |
| :--- |

해당 TransformTrack이 플레이 중인지 확인 (Track 이름) 
| **ResetTransformTrack(string TrackName)** |
| :--- |

해당 TransformTrack 이 적용되기 전의 Transform으로 리셋 (Track 이름) 
| **RemoveTransformTrack(String TrackName)** |
| :--- |

해당 Track 제거 (Track 이름) 
| **ResetTransform()** |
| :--- |

TransformTrack 이 적용되기 전의 최초 Transform으로 설정 
| **SetFriction( float value, float restitution, float density )** |
| :--- |

이 오브젝트의 표면 물리 마찰력을 설정 (마찰 값, 탄성 값, 밀도 값) 
| **MakeVehicleChassis( VehicleCreationInfo Info )** |
| :--- |

이 오브젝트를 VehicleChassis로 변경 ( [VehicleCreationInfo데이터](https://ditoland-utplus.gitbook.io/ditoland/api-reference/common/vehiclecreationinfo)) 
| **FRModeVehicle GetVehicle()** |
| :--- |

Vehicle 객체 반환 
# **상속받아 사용 가능한 기능들**

## **속성**

| **Parent** |
| :--- |

부모 오브젝트 
## **이벤트**

| **ConnectChangeEventFunction(string ValueName, function FunctionName)** |
| :--- |

추가된 값이 변경 될 때 호출되는 이벤트 (Value 이름, 연결 함수) 
## **샘플**


```lua

local function ChangeCurBullet(value) 

Logger:Log(“Hello”) 

end 

 

-- Object의 "CurBullet" 라는 Value가 변경되면 ChangeCurBullet 함수에 연결 

Object:ConnectChangeEventFunction("CurBullet", ChangeCurBullet)   

``` 
## **함수**

| **string GetName()** |
| :--- |

이름 얻기 
| **RModeObject GetParent(string ParentName)** |
| :--- |

이름으로 부모 객체 얻기 (찾고싶은 부모 객체 이름) 
| **RModeObject GetChild(string ChildName)** |
| :--- |

이름으로 자식 객체 얻기 (찾고싶은 자식 객체 이름) 
| **RModeObject GetGetSibling(string Name)** |
| :--- |

이름으로 형제 객체 얻기 (찾고싶은 형제 객체 이름) 
| **bool IsCharacter()** |
| :--- |

캐릭터인지 확인 
| **bool IsStaticMesh()** |
| :--- |

스테틱 메시인지 확인 
| **bool IsFX()** |
| :--- |

FX인지 확인 
| **bool IsSound()** |
| :--- |

Sound인지 확인 
| **bool IsPointLight()** |
| :--- |

포인트 라이트인지 확인 
| **bool IsSurfaceUI()** |
| :--- |

서피스 UI인지 확인 
| **bool IsScreenUI()** |
| :--- |

스크린 UI인지 확인 
| **bool IsItem()** |
| :--- |

아이템인지 확인 
| **bool IsNPC()** |
| :--- |

NPC인지 확인 
| **bool IsFolder()** |
| :--- |

폴더인지 확인 
| **bool IsScript()** |
| :--- |

스트립트인지 확인 
| **bool IsCollider()** |
| :--- |

Collider인지 확인 
| **bool IsWidget()** |
| :--- |

Widget인지 확인 
| **AddReplicateValue(string ValueName, Vector Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화 기능이 있는 벡터를 추가 (추가할 Value 이름, Vector 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, float Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화 기능이 있는 실수를 추가 (추가할 Value 이름, float 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, bool Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화 기능이 있는 bool를 추가 (추가할 Value 이름, bool 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, string Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화 기능이 있는 문자열을 추가 (추가할 Value 이름, string 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddReplicateValue(string ValueName, Color Data, ReplicateType Type, float Time, bool bSaveToStorage)** |
| :--- |

해당 객체에 서버, 클라이언트 간 동기화 기능이 있는 칼라를 추가 (추가할 Value 이름, Color 데이터, [Enum.ReplicateType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/replicatetype), 동기화 시간, 스토리지 저장 여부) 
| **AddSaveValue(string ValueName, Vector Data)** |
| :--- |

해당 객체 저장소에 벡터를 추가 (Value 이름, Vector 데이터) 
| **AddSaveValue(string ValueName, float Data)** |
| :--- |

해당 객체 저장소에 실수를 추가 (Value 이름, float 데이터) 
| **AddSaveValue(string ValueName, bool Data)** |
| :--- |

해당 객체 저장소에 bool을 추가 (Value 이름, bool 데이터) 
| **AddSaveValue(string ValueName, string Data)** |
| :--- |

해당 객체 저장소에 문자열을 추가 (Value 이름, string 데이터) 
| **AddSaveValue(string ValueName, Color Data)** |
| :--- |

해당 객체 저장소에 칼라를 추가 (Value 이름, Color 데이터) 
