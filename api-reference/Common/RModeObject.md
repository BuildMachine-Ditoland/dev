# **RModeObject**

| **월드트리의 오브젝트에 해당하는 스크립트 객체** |
| :--- |
## **함수**

| **string GetName()** |
| :--- |
| **객체 이름 얻기** |

| **RModeObject GetParent(string ParentName)** |
| :--- |
| **부모 객체 얻기** |

| **RModeObject GetChild(string ChildName)** |
| :--- |
| **이름으로 자식 객체 얻기** |

| **Vector GetLocation()** |
| :--- |
| **위치 얻기** |

| **OnCreateEvent** |
| :--- |
| **생성 시 호출되는 이벤트** |

| **OnUpdateEvent** |
| :--- |
| **생성 후 매 프레임에 호출되는 이벤트** |

| **OnDestoryEvent** |
| :--- |
| **삭제될 때 호출되는 이벤트** |

| **OnCollisionEvent** |
| :--- |
| **다른 객체와 충돌할 때 호출되는 이벤트** |

| **OnBeginOverlapEvent** |
| :--- |
| **다른 객체와 겹쳐질 때 호출되는 이벤트** |

| **OnEndOverlapEvent** |
| :--- |
| **다른 객체와 겹쳐짐이 끝날 때 호출되는 이벤트** |

| **OnOverlapUpdateEvent** |
| :--- |
| **다른 객체와 겹쳐있는 동안 매 프레임 호출되는 이벤트** |

| **RModeObject GetChild(string childName)** |
| :--- |
| **자식 객체 얻기** |

| **RModeObject GetChild(string childName)** |
| :--- |
| **부모 객체 얻기** |

| **AddLocalMove(string TrackName, FVector Pos, float Time, bool CheckCollision)** |
| :--- |
| **로컬 좌표 기준으로 이동 변화를 추가한다.** |

| **AddLocalRot(string TrackName, FVector Rot, float Time)** |
| :--- |
| **로컬 좌표 기준으로 회전 변화를 추가한다.** |

| **AddScale(string TrackName, FVector Scale, float Time)** |
| :--- |
| **로컬 좌표 기준으로 스케일 변화를 추가한다.** |

| **AddWorldMove(string TrackName, FVector Pos, float Time, bool CheckCollision)** |
| :--- |
| **월드 좌표 기준으로 이동 변화를 추가한다.** |

| **월드 좌표 기준으로 회전 변화를 추가한다.** |
| :--- |
| **AddWorldRot(string TrackName, FVector Rot, float Time)** |

| **AddEmpty(string TrackName, float Time)** |
| :--- |
| **객체 변환의 대기 시간을 추가한다.** |

| **PlayTransformTrack(string TrackName, ERObjectTransformPlayType Type, int PlayCount)** |
| :--- |
| **설정된 변환 컨트롤러 실행** |

| **StopTransformTrack(string TrackName)** |
| :--- |
| **변환 컨트롤러 정지** |

| **PauseTransformTrack(string TrackName)** |
| :--- |
| **변환 컨트롤러 일시 정지** |

| **ResumeTransformTrack(string TrackName)** |
| :--- |
| **변환 컨트롤러 다시 플레이** |

| **IsPlayingTransformTrack(string TrackName)** |
| :--- |
| **해당 TransformTrack이 플레이 중인지 확인** |

| **ResetTransformTrack(string TrackName)** |
| :--- |
| **해당 TransformTrack 리셋(적용되기 전의 Transform 으로 설정)** |

| **RemoveTransformTrack(String TrackName)** |
| :--- |
| **해당 Track 제거** |

| **ResetTransform()** |
| :--- |
| **TransformTrack 이 적용되기 전의 최초 Transform으로 설정** |

| **SetFriction( float value, float restitution, float density )** |
| :--- |
| **이 오브젝트의 표면 물리 마찰력을 설정** |

| **MakeVehicleChassis( const sol::table luaVehicleCreationInfo )** |
| :--- |
| **이 오브젝트를 VehicleChassis 로 변경.** |

