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
| 1 | RollingPart | ![RollingPart](.gitbook/assets/2-1.png) | 객체의 회전 방향을 설정할 수 있는 Toy입니다.  <br/> 반복해서 계속 회전합니다. |  **Axis X / Y / Z** <br/> - 회전할 방향 값 <br/> **Speed**  <br/>- 회전하는데 걸리는 Sec |                                                                           
| 2 | MovePart | ![MovePart](.gitbook/assets/2-2.png) | 객체의 이동을 설정할 수 있는 Toy입니다. <br/> 이동한 다음 일정 시간 대기 후 다시 원래 자리로 돌아옵니다. |  **Distance X / Y / Z**  <br/>- 이동할 방향 값 <br/>   **Speed**  <br/>- 이동하는데 걸리는 Sec WaitTime - 이동 후 대기하는 Sec |                                                                           
| 3 | Crevase | ![Crevase](.gitbook/assets/2-3.png) |  접촉하면 중력을 얻어 떨어지는 Toy입니다.  <br/> 배치할 때 다른 객체와 너무 붙여놓으면 안떨어지는 경우도 있습니다.|    **PhysicsTime**  <br/> - 밟은 뒤 몇 초 후 떨어지나  <br/>**DeleteTime** <br/> - 떨어진 뒤 삭제되는 시간 | 
| 4 | CheckPoint | ![CheckPoint](.gitbook/assets/2-4.png) |  접촉하면 플레이어의 다음 시작 위치가 변경되는 Toy입니다.  <br/>필요한 만큼 복사해서 맵에 배치하면 됩니다. |  | 
| 5 | KillBox | ![KillBox](.gitbook/assets/2-5.png) |  접촉하면 캐릭터가 사망하는 Toy입니다.  <br/>스크립트만 복사해 붙여넣으면 어떤 객체든 killBox로 만들 수 있습니다.|  | 
| 6 | TeleportPad | ![TeleportPad](.gitbook/assets/2-6.png) |   플레이어가 TeleportInPad에 접촉하면 TeleportOutPad로 순간이동하는 Toy입니다. <br/>  2개가 한 세트입니다. 취급에 주의하세요. |  **TeleportTime**  <br/>- 텔레포트 하기까지의 대기시간 |  
| 7 | Fan | ![Fan](.gitbook/assets/2-7.png) |  일정 시간마다 Fan이 동작하여 Floor와 접촉한 플레이어를 밀어내는 Toy입니다. <br/> 밀려나는 범위를 넓히고 싶다면 Floor 객체의 크기를 조정해보세요.  |  **Speed**  <br/> - 객체가 밀려나는 속도  <br/>**OnTime** <br/> - 선풍기가 정지상태에서 가동까지 걸리는 시간  <br/>**OffTime**  <br/>- 선풍기 가동 후 정지하기 까지 걸리는 시간  <br/>**FanSpeed** <br/> - 선풍기 돌아가는 속도 |                                                                                                                                                   
| 8 | Lift | ![Lift](.gitbook/assets/2-8.png) |  플레이어가 올라타면 내려가는 리프트 Toy 입니다. 협동 플레이에 적합합니다. <br/> 응용하면 점프 시 올라가는 엘리베이터 같은 걸로 개조할 수 있습니다.|  **LiftSpeed**<br/> - Lift 움직이는 속도 (1인 기준) |                                                                                                                                                      
| 9 | Lift_Button | ![Lift_Button](.gitbook/assets/2-9.png) | 버튼을 밟고 있는 동안  내려오는 리프트 Toy입니다. 협동 플레이에 적합합니다. <br/> 응용하면 자동 엘리베이터 같은 걸로 개조할 수 있습니다. |  **LiftSpeed**<br/> - Lift 움직이는 속도 (1인 기준)|                                                                                                                                                      
| 10 | BuffSpawner | ![BuffSpawner](.gitbook/assets/2-10.png) |  Spawner 내부에 있는 아이템을 랜덤으로 선택해 일정 시간마다 생성해주는 Toy입니다. <br/>옵션으로 접촉 시 일정시간 능력이 증가하는 Buff Item 4종이 포함되어 있습니다.  |  ___Spawner Property___ <br/>  **SpawnCount** <br/> - 버프가 나올 최대 개수 (예 -> 10으로 하면 버프가 10번 생성되면서 더이상 생성 X) **SpawnTime**<br/> - 버프가 스폰되는 시간 <br/><br/>   ___Item Property___ <br/>  **Duration**<br/> - 버프  지속 시간<br/> **Heal**<br/> - 힐 버프 획득 시 회복량<br/> **SpeedPlus**<br/> - 이속 버프 획득 시 증가량<br/>**JumpPlus** - 점프 버프 획득 시 증가량 |                                                                                                                                                       
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
| 25 | SlidingDoor_Button | ![SlidingDoor_Auto](.gitbook/assets/2-24.png) |   버튼을 밟으면 문이 열리는 도어 Toy입니다. |   **MoveTime**<br/>- 문 열린 뒤 닫히는 시간 <br/>**MoveSpeed**<br/>- 문이 움직이는 속도 |
  
    
  
  ###3. 맵별 추천 Toy검색 키워드
  
  Jump 1 - island , rock , tree , grass , flower , floating<br/>
  Jump 2 - island , rock , tree , grass , flower , floating<br/>
  Jump 3 - stone <br/>
  Jump 4 - 어울리는 Toy가 없음. 기본제공 모델 사용  Neon Material 활용<br/>
  Jump 5 - rock , junk , oasis<br/>

 
