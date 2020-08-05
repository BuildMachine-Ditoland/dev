
Color 객체에요. 
## **생성자**

| **Color.new()** |
| :--- |

Color를 생성해요 
| **Color.new(number R, number G, number B, number A)** |
| :--- |

Color를 R, G, B, A 값으로 세팅하여 생성해요 
## **속성**

| **number R** |
| :--- |

빨간 색을 나타내요. (0 ~ 255) 
| **number G** |
| :--- |

초록 색을 나타내요. (0 ~ 255) 
| **number B** |
| :--- |

파란 색을 나타내요. (0 ~ 255) 
| **number A** |
| :--- |

투명도를 나타내요. (0 ~ 255) 

샘플 

```lua
color = Color.new(255, 0, 0, 255)

Timer = UI:GetUIScene("Timer")

--Timer라는 UI의 TimerText라는 글자를 빨간색으로 세팅
Timer:SetTextColor("TimerText", color)

color2 = Color.new(0, 255, 255, 0)

color = color + color2	--> color는 하얀색
```
