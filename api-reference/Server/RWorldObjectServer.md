# **RWorldObjectServer**


서버 모드 오브젝트들(ObjectFXServer, ObjectSoundServer, ObjectPointLightServer 등)의 부모 객체. 
## **함수**

| **SetCollisionType(string usercollisiontype)** |
| :--- |

해당 오브젝트의 충돌 타입을 설정 

[Game:AddUserCollisionType](https://ditoland-utplus.gitbook.io/ditoland/api-reference/server/rgameserver#undefined-1)으로 추가한 타입만 가능해요 없을 시에는 기본 타입으로 지정되요 
| **SetCharacterCollisionResponse(ECollisionResponse CollisionResponse)** |
| :--- |

캐릭터와 충돌 시 어떻게 처리 할지를 설정하는 함수 ( [Enum.CollisionResponse.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/collisionresponse)) 
| **SetUserCollisionTypeResponse(string UserCollisionType, ECollisionResponse CollisionResponse)** |
| :--- |

유저타입 충돌 물체의 충돌 시 처리를 변경하는 함수 (변경 할 유저타입 충돌 이름, [Enum.CollisionResponse.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/collisionresponse)) 
| **SetReplicatePriority(int priority)** |
| :--- |

서버에서 클라로 얼마나 많이 동기화 할것인지에 대한 값 설정 (우선 순위 값) 
