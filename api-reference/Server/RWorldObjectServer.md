# **RWorldObjectServer**

서버 모드 오브젝트들(ObjectFXServer, ObjectSoundServer, ObjectPointLightServer 등)의 부모 객체. 
## **함수**

| **SetCollisionType(string usercollisiontype)** |
| :--- |
해당 오브젝트의 충돌 타입을 Game에 추가한 유저충돌 타입으로 설정. 해당 타입이 없을 경우 기본 타입으로 설정 
| **SetCharacterCollisionResponse(ECollisionResponse CollisionResponse)** |
| :--- |
캐릭터와 충돌 시 어떻게 처리 할지를 설정하는 함수. 해당 설정에 따라 충돌, 겹칩 이벤트 호출 됨 
| **SetUserCollisionTypeResponse(string UserCollisionType, ECollisionResponse CollisionResponse)** |
| :--- |
유저타입 충돌 물체와 충돌 시 처리 할지를 설정하는 함수. 해당 설정에 따라 충돌, 겹칩 이벤트 호출 됨 
| **SetReplicatePriority(int priority)** |
| :--- |
서버에서 클라로 얼마나 많이 동기화 할것인지에 대한 값 설정. 
