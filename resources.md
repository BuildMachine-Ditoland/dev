# Resources

### 1. GameJam Toy 검색 방법


1-1. 스튜디오의 오른쪽 하단에 위치한 툴박스를 찾아 검색필터 기능을 사용합니다.


![](.gitbook/assets/resources1-1.png)

1-2. 검색필터의 Tag 항목에서 Sci_Fi를 선택하고 APPLY 버튼을 누르면 GameJam Toy가 표시됩니다.

![](.gitbook/assets/resources1-2.png)

1-3. 툴박스에서 토이를 마우스로 클릭하면, 현재 보고있는 화면에 토이가 생성됩니다.

### 2. GameJam Toy 목록

| 번호 | 이름 | 이미지 | 설명 | 설정값 |
| :---: | :--- | :---: | :--- |:--- |
| 1 | RollingPart | ![RollingPart](.gitbook/assets/2-1.png) | 일정 패턴으로 반복해서 회전하는 Toy 입니다.  <br/> 회전 방향과 속도를 설정할 수 있습니다. |  **Axis X / Y / Z** <br/> - 회전할 방향 값 <br/> **Speed**  <br/>- 회전하는데 걸리는 Sec |                                                                           
| 2 | MovePart | ![MovePart](.gitbook/assets/2-2.png) | 일정 패턴으로 반복해서 움직이는 Toy 입니다. <br/> 방향과 거리, 속도를 설정할 수 있습니다. |  **Distance X / Y / Z**  <br/>- 이동할 방향 값 <br/>   **Speed**  <br/>- 이동하는데 걸리는 Sec <br/>  **WaitTime** - 이동 후 대기하는 Sec |                                                                           
| 3 | Crevase | ![Crevase](.gitbook/assets/2-3.png) |  플레이어가 접촉하면 떨어져서 사라지는 Toy 입니다.  <br/> 배치할 때 다른 객체와 너무 붙여놓으면 안떨어지는 경우도 있습니다.|    **PhysicsTime**  <br/> - 밟은 뒤 몇 초 후 떨어지나  <br/>**DeleteTime** <br/> - 떨어진 뒤 삭제되는 시간 | 
| 4 | CheckPoint | ![CheckPoint](.gitbook/assets/2-4.png) |  접촉하면 플레이어의 다음 시작 위치가 변경되는 Toy입니다.  <br/>필요한 만큼 복사해서 맵에 배치하면 됩니다. |  | 
| 5 | KillBox | ![KillBox](.gitbook/assets/2-5.png) |  접촉하면 캐릭터가 사망하는 Toy입니다.  <br/>스크립트만 복사해 붙여넣으면 어떤 객체든 killBox로 만들 수 있습니다.|  | 
| 6 | TeleportPad | ![TeleportPad](.gitbook/assets/2-6.png) |   플레이어가 TeleportInPad에 접촉하면 TeleportOutPad로 순간이동하는 Toy입니다. <br/>  2개가 한 세트입니다. 취급에 주의하세요. |  **TeleportTime**  <br/>- 텔레포트 하기까지의 대기시간 |  
| 7 | Fan | ![Fan](.gitbook/assets/2-7.png) | 일정 시간마다 Fan이 동작하면서 Floor에 접촉되어 있는 플레이어를 밀어내는 Toy입니다. <br/> 밀려나는 범위를 넓히고 싶다면 Floor 객체의 크기를 조정해보세요.  |  **Speed**  <br/> - 객체가 밀려나는 속도  <br/>**OnTime** <br/> - 선풍기가 정지상태에서 가동까지 걸리는 시간  <br/>**OffTime**  <br/>- 선풍기 가동 후 정지하기 까지 걸리는 시간  <br/>**FanSpeed** <br/> - 선풍기 돌아가는 속도 |                                                                                                                                                   
| 8 | Lift | ![Lift](.gitbook/assets/2-8.png) |  플레이어가 올라타면 내려가는 리프트 Toy 입니다. 협동 플레이에 적합합니다. <br/> 응용하면 점프 시 올라가는 엘리베이터 같은 걸로 개조할 수 있습니다.|  **LiftSpeed**<br/> - Lift 움직이는 속도 (1인 기준) |                                                                                                                                                      
| 9 | Lift_Button | ![Lift_Button](.gitbook/assets/2-9.png) | 버튼을 밟고 있는 동안  내려오는 리프트 Toy입니다. 협동 플레이에 적합합니다. <br/> 응용하면 자동 엘리베이터 같은 걸로 개조할 수 있습니다. |  **LiftSpeed**<br/> - Lift 움직이는 속도 (1인 기준)|                                                                                                                                                      
| 10 | BuffSpawner | ![BuffSpawner](.gitbook/assets/2-10.png) |  일정 시간마다 Buff를 생성해주는 Toy입니다. <br/> 옵션으로 일정시간 능력을 변화시키는 4종의 Buff Item을 포함하고 있습니다.  |  ___Spawner Property___ <br/>  **SpawnCount** <br/> - 버프가 나올 최대 개수 (예 -> 10으로 하면 버프가 10번 생성되면서 더이상 생성 X) **SpawnTime**<br/> - 버프가 스폰되는 시간 <br/><br/>   ___Item Property___ <br/>  **Duration**<br/> - 버프  지속 시간<br/> **Heal**<br/> - 힐 버프 획득 시 회복량<br/> **SpeedPlus**<br/> - 이속 버프 획득 시 증가량<br/>**JumpPlus** - 점프 버프 획득 시 증가량 |                                                                                                                                                       
| 11 | StopWatch | ![StopWatch](.gitbook/assets/2-11.png) |  스타트 라인에 접촉하면 타이머가 실행되며, 엔드 라인에 접촉하면 타이머가 멈추는 Toy입니다. |   |       
| 12 | Turret_1 | ![Turret_1](.gitbook/assets/2-12.png) | 플레이어가 접근하면 추적해 공격하는 터렛 Toy입니다. 친숙한 기본 외형입니다. <br/> 총알에 다양한 효과를 넣어 보세요. |   **ScanTime**<br/> - 스캔 대기시간<br/>**FireTime**<br/>- 발사 대기시간<br/>**FireDistance**<br/>- 포착 거리<br/>**LightColorR**<br/>- LightColor 변경할 Color R 값<br/>**LightColorG**<br/>- LightColor 변경할 Color G 값<br/>**LightColorB**<br/>- LightColor 변경할 Color B 값<br/>**BulletSpeed**<br/>- Bullet이 목적지까지의 도착시간 (초단위)<br/>**BulletDamage**<br/>- 캐릭터가 Bullet에 맞았을 때 줄 대미지<br/>  |      
| 13 | Turret_2 | ![Turret_2](.gitbook/assets/2-13.png) | 플레이어가 접근하면 추적해 공격하는 터렛 Toy입니다. 개선된 외형입니다. <br/> 총알에 다양한 효과를 넣어 보세요.|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"|
| 14 | Turret_3 | ![Turret_3](.gitbook/assets/2-14.png) | 플레이어가 접근하면 추적해 공격하는 터렛 Toy입니다. 많이 개선된 외형입니다.<br/>  총알에 다양한 효과를 넣어 보세요.|&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"|
| 15 | Turret_4 | ![Turret_4](.gitbook/assets/2-15.png) | 플레이어가 접근하면 추적해 공격하는 터렛 Toy입니다. 너무 개선된 외형입니다.<br/>  총알에 다양한 효과를 넣어 보세요. |&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"|
| 16 | CrashBlock_HP | ![CrashBlock_HP](.gitbook/assets/2-16.png) | HP가 있는 벽 오브젝트 Toy입니다.<br/> 벽과 충돌하면 벽의 HP가 감소되며, 벽의 HP가 0이되면 파괴됩니다. |    **HP** <br/> - 벽에 설정할 HP<br/> **MaxHP** <br/>- 벽의 최대 HP 설정<br/> **IsDelete** <br/>- 벽이 파괴 된 후 삭제할지 말지 여부<br/>**DeleteTime** <br/>- 벽이 파괴돈 후 삭제될때 까지의 시간<br/>**ObjectDamage** <br/>- 캐릭터가 아닌 오브젝트가 충돌 시 입을 대미지<br/> | 
| 17 | JumpPad_Auto | ![JumpPad_Auto](.gitbook/assets/2-17.png) | 접촉한 플레이어를 높이 점프시켜주는 Toy입니다.  |     | 
| 18 | JumpPad_Auto_PowerUP | ![JumpPad_Auto_PowerUP](.gitbook/assets/2-18.png) |   접촉한 플레이어를 매우 높이 점프시켜주는 Toy입니다.  |   **JumpPower**<br/>- 패드를 밞았을 때 적용되는 점프력  | 
| 19 | ConveryorBelt | ![ConveryorBelt](.gitbook/assets/2-19.png) | 플레이어가 벨트 위에 올라타면 벨트를 따라 천천히 이동되는 Toy입니다.  <br/> 벨트를 잘 사용하면 미끄러지는 바닥 효과를 낼 수 있습니다.  |**BeltSpeed8**<br/> - 벨트 위에 올라간 객체가 얻는 추가 속도입니다. | 
| 20 | WeaponBox | ![WeaponBox](.gitbook/assets/2-20.png) | 접촉하면 지정된 아이템을 장착해주는 Toy입니다. 현재 Rifle로 지정되어 있습니다.| Rifle Toy와 함께 사용해야 합니다.<br/>Rifle을 Toybox 폴더에 넣어야 동작합니다.  |
| 21 | BulletSupplyBox | ![BulletSupplyBox](.gitbook/assets/2-21.png) |  접촉하면 Rifle 무기의 탄환이 충전됩니다.| Rifle Toy와 함께 사용해야 합니다. | 
| 22 | Rifle_FPS | ![Rifle_FPS](.gitbook/assets/2-22.png) |  플레이어와 접촉하면 장착되고 마우스 클릭으로 공격할 수 있는 라이플 Toy입니다.<br/> FPS (1인칭) 용으로 설정되어 있습니다. |  ___Rifle.Script Parameters___<br/> **Normal_Damage**<br/>- 공격력<br/>**MaxBullet**<br/> - 보유 최대 탄환<br/>**BulletDistance**<br/> - 총알의 사거리<br/> **BulletSpeed**<br/>- 총알의 속도<br/>**ShakeTime**<br/>- 발사 시 흔들리는 시간**ShakeScale**<br/> - 발사 시 흔들리는 범위**CurBullet**<br/>- 현재 탄창 내 총알량**ReloadBullet**<br/>- 재장전 시 탄창 총알량<br/>**ReloadTime**<br/>- 재장전 시간<br/>**IsReload**<br/>- 재장전 상태임을  체크<br/>**WeaponName**<br/>- HUD에 표시될 총 이름 | 
| 23 | Rifle_TPS | ![Rifle_TPS](.gitbook/assets/2-23.png) | 플레이어와 접촉하면 장착되고 마우스 클릭으로 공격할 수 있는 라이플 Toy입니다.<br/>   TPS (3인칭) 용으로 설정되어 있습니다. |&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"|
| 24 | SlidingDoor_Auto | ![SlidingDoor_Auto](.gitbook/assets/2-24.png) | 접근하면 자동으로 열리는 문 Toy입니다. |   **MoveTime**<br/>- 문 열린 뒤 닫히는 시간<br/>**MoveSpeed**<br/>- 문이 움직이는 속도 |
| 25 | SlidingDoor_Button | ![SlidingDoor_Auto](.gitbook/assets/2-25.png) |   버튼을 밟으면 문이 열리는 도어 Toy입니다. |   **MoveTime**<br/>- 문 열린 뒤 닫히는 시간 <br/>**MoveSpeed**<br/>- 문이 움직이는 속도 |
| 26 | FanToy | ![SlidingDoor_Auto](.gitbook/assets/2-26.png) |  캐릭터를 밀어내는 선풍기 Toy입니다. |  **Speed**<br/>- 객체가 밀려나는 속도 <br/>**OnTime**<br/>- 선풍기가 정지상태에서 가동까지 걸리는 시간<br/>**OffTime**<br/>- 선퐁기 가동후 정지하기 까지 걸리는 시간<br/>**FanSpeed**<br/>- 선풍기 돌아가는 속도 |
| 27 | LadderToy | ![SlidingDoor_Auto](.gitbook/assets/2-27.png) | 구조물을 오를 수 있게 도와주는 사다리 Toy입니다. |  |   
| 28 | Pushable_Object | ![SlidingDoor_Auto](.gitbook/assets/2-28.png) | 벽에 몇초 이상 접근하면 미는 방향으로 움직이는 벽 Toy입니다. |  **CheckTime**<br/>- 캐릭터가 몇초이상 밀어야 움직일지 결정할 시간 <br/>**MoveSpeed**<br/>- 벽이 움직일 속도<br/>**IsPush**<br/>- 벽을 밀 수 있는지 가능여부|
| 29 | SeatToy | ![SlidingDoor_Auto](.gitbook/assets/2-29.png) | 캐릭터가 앉을 수 있는 의자 Toy입니다. |  |
| 30 | SuperJump | ![SlidingDoor_Auto](.gitbook/assets/2-30.png) | Space키를 오래 누를수록 더 높게 점프할 수 있는 슈퍼 점프 모듈 Toy입니다. <br/>배율값이 높을수록 점프 거리가 높아집니다. | **DefaultJump**<br/>- 기본 점프력 <br/>**JumpMultiple**<br/>-  입력 시간에 따른 점프 배율 값 |
| 31 | [Guys]<br/> FallBlock | ![SlidingDoor_Auto](.gitbook/assets/2-31.png) | 밟으면 일정 시간 후 추락하는 Toy입니다. | **WavePower**<br/>- 흔들림 연출의 강도 <br/>**DeleteTime**<br/>-  발판을 밟고 삭제되기까지의 걸리는 시간 |
| 32 | [Guys]<br/> SpeedBlock | ![SlidingDoor_Auto](.gitbook/assets/2-32.png) | 올라타면 진행 방향으로 자동 이동되는 가속 발판 Toy입니다. <br/>이동속도가 높을 수록 가속도가 빨라집니다. | **MoveSpeed**<br/>- 캐릭터를 해당 방향으로 움직일 스피드 |
| 33 | [Guys]<br/> RotBlock | ![SlidingDoor_Auto](.gitbook/assets/2-33.png) | 지정 방향으로 계속해서 회전하는 원판 Toy입니다. | **RotRandom**<br/>- 왼쪽, 오른쪽으로 회전하는 걸 랜덤으로 할건지에 대한 여부 <br/>**RotTime**<br/>- 총 회전하는데 걸리는 시간 <br/>**RotRight**<br/>- 시계 방향으로 돌건지 선택 (Random 선택하면 이건 적용 안됨) |
| 34 | [Guys]<br/> AutoWallRightLeft | ![SlidingDoor_Auto](.gitbook/assets/2-34.png) | 캐릭터를 밀어내는 벽 Toy입니다. | **RightMoveTime**<br/>- 오른쪽으로 가기까지의 걸리는 시간<br/>**RightWaitTime**<br/>- 오른쪽 도착 후에 대기 <br/>**LeftMoveTime**<br/>- 왼쪽으로 가기까지의 걸리는 시간 <br/>**LeftWaitTime**<br/>- 왼쪽 도착 후에 대기 시간 <br/>**MoveVector**<br/>- 위로 얼마나 올라갈지 결정 |
| 35 | [Guys]<br/> AutoWallUpDown | ![SlidingDoor_Auto](.gitbook/assets/2-35.png) | 위아래로 이동하는 차단 벽 Toy입니다. | **UpMoveTime**<br/>- 위로 올라가기 까지 걸리는 시간<br/>**UpWaitTime**<br/>- 위로 올라간 후에 대기 시간 <br/>**DownMoveTime**<br/>- 아래로 내려가기까지 걸리는 시간 <br/>**DownWaitTime**<br/>- 아래로 내려간 후에 대기 시간 <br/>**MoveVector**<br/>- 위로 얼마나 올라갈지 결정 |
| 36 | [Guys]<br/> CrashDoorSet | ![SlidingDoor_Auto](.gitbook/assets/2-36.png) | 일정 시간 부딪히면 파괴되는 문 Toy 세트입니다.  | **CrashCount**<br/>- 몇번 부딪히면 파괴될지 횟수<br/>**CollisionWait**<br/>- 충돌 후에 다음 충돌까지 걸리는 대기시간<br/>**Force**<br/>- 파괴될 때 얼마만큼의 힘을 줄지 결정 <br/>**WavePower**<br/>- 흔들림 연출의 강도를 설정 <br/>**IsDelete**<br/>- 파괴된 후에 문을 제거할지 선택<br/>**DeleteTime**<br/>- 문을 제거까지 걸리는 시간<br/>**RandomSet**<br/>- 랜덤으로 몇개가 파괴가능하게 할 지 선택 |
| 37 | [Guys]<br/> CrashDoor | ![SlidingDoor_Auto](.gitbook/assets/2-37.png) | 일정 시간 부딪히면 파괴되는 문 Toy입니다.  | **CrashCount**<br/>- 몇번 부딪히면 파괴될지 횟수<br/>**CollisionWait**<br/>- 충돌 후에 다음 충돌까지 걸리는 대기시간<br/>**Force**<br/>- 파괴될 때 얼마만큼의 힘을 줄지 결정 <br/>**WavePower**<br/>- 흔들림 연출의 강도를 설정 <br/>**IsDelete**<br/>- 파괴된 후에 문을 제거할지 선택<br/>**DeleteTime**<br/>- 문을 제거까지 걸리는 시간 |
| 38 | [Guys]<br/> LaunchBall | ![SlidingDoor_Auto](.gitbook/assets/2-38.png) | 일정 시간마다 구체를 발사하는 Toy입니다.  | **SpawnTime**<br/>- 공이 생성되기까지 걸리는 시간<br/>**IsRandom**<br/>- 체크할 시 Base안에 있는 Ball중에 랜덤으로 생성 ( 체크풀 시 순차적으로 생성)<br/>**ForwardForce**<br/>- 공이 생설될 때 앞으로 치고나갈 힘 <br/>**MaxCount**<br/>- 총 생성될 개수 (설정한 값 이상은 더이상 생성안됨) <br/>**BallKG**<br/>- 생성된 Ball의 무게를 설정<br/>**DeleteTime**<br/>- 공이 생성 후 삭제까지의 시간<br/>**Force**<br/>- 물체에 부딪힐 때 캐릭터가 날아가는 힘 |
| 39 | [Guys]<br/> HitRoad | ![SlidingDoor_Auto](.gitbook/assets/2-39.png) | 좌우로 움직이며 진로를 방해하는 Toy입니다.  | **RotRandom**<br/>- 왼쪽, 오른쪽으로 회전하는 걸 랜덤으로 할건지에 대한 여부<br/>**RotTime**<br/>- 총 회전하는데 걸리는 시간<br/>**MoveTime**<br/>- 이동 하는데 까지 걸리는 시간 <br/>**Force**<br/>- 물체에 부딪힐 때 캐릭터가 날아가는 힘 <br/>**UpForce**<br/>-캐릭터가 떠오르는 힘 |
| 40 | [Guys]<br/> RotWindmill | ![SlidingDoor_Auto](.gitbook/assets/2-40.png) | 지정 방향으로 계속해서 회전하며, 부딪히면 캐릭터를 반대로 밀어내는 Toy입니다.  | **RotRandom**<br/>- 왼쪽, 오른쪽으로 회전하는 걸 랜덤으로 할건지에 대한 여부<br/>**RotTime**<br/>- 총 회전하는데 걸리는 시간 |
| 41 | [Guys]<br/> RotHammer | ![SlidingDoor_Auto](.gitbook/assets/2-41.png) | 지정 방향으로 계속해서 회전하며, 부딪히면 캐릭터를 반대로 밀어내는 Toy입니다. | **RotRandom**<br/>- 왼쪽, 오른쪽으로 회전하는 걸 랜덤으로 할건지에 대한 여부<br/>**RotTime**<br/>- 총 회전하는데 걸리는 시간<br/> **Force**<br/>- 물체에 부딪힐 때 캐릭터가 날아가는 힘<br/>**UpForce**<br/>- 캐릭터가 떠오르는 힘 |
| 42 | [Guys]<br/> RotClock | ![SlidingDoor_Auto](.gitbook/assets/2-42.png) | 지정 방향으로 계속해서 회전하며, 부딪히면 캐릭터를 반대로 밀어내는 Toy입니다. | **RotRandom**<br/>- 왼쪽, 오른쪽으로 회전하는 걸 랜덤으로 할건지에 대한 여부<br/>**RotTime**<br/>- 총 회전하는데 걸리는 시간<br/> **Force**<br/>- 물체에 부딪힐 때 캐릭터가 날아가는 힘<br/>**UpForce**<br/>- 캐릭터가 떠오르는 힘 |
| 43 | [Guys]<br/> ClockWeight | ![SlidingDoor_Auto](.gitbook/assets/2-43.png) | 지정 방향으로 계속해서 회전하며, 부딪히면 캐릭터를 반대로 밀어내는 Toy입니다. | **Angle**<br/>- 추가 회전하는 각도 (해당 값만큼 왔다갔다함)<br/>**MoveTime**<br/>- 이동하는데 걸리는 시간<br/> **Force**<br/>- 물체에 부딪힐 때 캐릭터가 날아가는 힘<br/>**UpForce**<br/>- 캐릭터가 떠오르는 힘 |
 
  
    
  
  ###3. 맵별 추천 Toy검색 키워드
  
  Jump 1 - island , rock , tree , grass , flower , floating<br/>
  Jump 2 - island , rock , tree , grass , flower , floating<br/>
  Jump 3 - stone <br/>
  Jump 4 - 어울리는 Toy가 없음. 기본제공 모델 사용  Neon Material 활용<br/>
  Jump 5 - rock , junk , oasis<br/>

 
