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
