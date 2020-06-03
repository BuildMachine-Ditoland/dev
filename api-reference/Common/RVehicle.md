# **RVehicle**

 **자동차 객체에요.** 
## **함수**

| **MakeVehicleChassis(RScriptWorldObject Chassis, FRVehicleCreationInfo VehicleCreationInfo)** |
| :--- |
 **특정 WorldObject를 Chassis로 만들어줌.** 
| **AttachWheel(RScriptWorldObject Wheel, FRWheelCreationInfo WheelCreationInfo);** |
| :--- |
 **Chassis에 휠을 붙임.** 
| **SetOwner(string PlayerName);** |
| :--- |
 **이 Vehicle을 소유한 플레이어를 셋팅** 
| **bool IsOccupied()** |
| :--- |
 **이 Vehicle이 이용중인지?** 
| **void Forward(float power)** |
| :--- |
 **전진** 
| **Reverse(float power)** |
| :--- |
 **후진** 
| **SteerLeft(float power)** |
| :--- |
 **좌회전** 
| **SteerRight(float power)** |
| :--- |
 **우회전** 
| **Brake(float power);** |
| :--- |
 **정지** 
| **Reset(float height, float cooltime)** |
| :--- |
 **Vehicle의 자세를 바로 잡는다.** 
