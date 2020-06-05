# **Color**


Color 객체에요 
## **생성자**

| **Color.new()** |
| :--- |

Color를 생성한다. 
| **Color.new(number A, number R, number G, number B)** |
| :--- |

Color를 A, R, G, B 값으로 세팅하여 생성한다. 
## **속성**

| **number A** |
| :--- |

투명도 0~255 
| **number R** |
| :--- |

빨간 색 0~255 
| **number G** |
| :--- |

초록 색 0~255 
| **number B** |
| :--- |

파란 색 0~255 
## **예제**


```lua
color = Color.new(255, 0, 0, 255)

Timer = UI:GetUIScene("Timer")

--Timer라는 UI의 TimerText라는 글자를 빨간색으로 세팅
Timer:SetTextColor("TimerText", color)

color2 = Color.new(0, 255, 255, 0)

color = color + color2	--> color는 하얀색
```
