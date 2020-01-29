# RModePhase

## **RModeGame**

**게임을 단계별로 구성 할 때 사용하는 객체. Game.AddPhase\(string phasename\) 를 사용하여 이용가능**

 

## **Property**

| **var EnterEvent** |
| :--- |
| **단계에 진입 시 호출되는 이벤트 객체** |

| **var UpdateEvent** |
| :--- |
| **단계가 활성화 되어 있는 때 매 프레임 호출되는 이벤트 객체** |

| **var ExitEvent** |
| :--- |
| **단계에서 다른 단계로 변경 될 때 호출되는 이벤트 객체** |

 

## **Functions**

| **number GetPhaseTime\(\)** |
| :--- |
| **단계가 활성화 되어 있었던 시간 얻기** |

| **string GetPhaseName\(\)** |
| :--- |
| **이름 얻기** |

