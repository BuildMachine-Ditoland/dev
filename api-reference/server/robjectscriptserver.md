# RObjectScriptServer



### **RObjectScriptServer**

**서버스크립트에 제공되는 RObjectScript의 자식 객체로 오브젝트의 이동, 회전, 스케일 충돌 타입 설정 등을 할 수 있다.**  


### **Function**

| **void SetCollisionType\(string usercollisiontype\)** |
| :--- |
| **해당 오브젝트의 충돌 타입을 Game에 추가한 유저충돌 타입으로 설정. 해당 타입이 없을 경우 기본 타입으로 설정** |

| **void SetCharacterCollisiontResponse\(ECollisionResponse CollisionResponse\)** |
| :--- |
| **캐릭터와 충돌 시 어떻게 처리 할지를 설정하는 함수. 해당 설정에 따라 충돌, 겹칩 이벤트 호출 됨** |

| **void SetUserCollisionTypeResponse\(string UserCollisionType, ECollisionResponse CollisionResponse\)** |
| :--- |
| **유저타입 충돌 물체와 충돌 시 처리 할지를 설정하는 함수. 해당 설정에 따라 충돌, 겹칩 이벤트 호출 됨** |

