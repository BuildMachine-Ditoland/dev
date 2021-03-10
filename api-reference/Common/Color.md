
Color 객체에요. 
<br>
## **생성자**

<br>
<br>
| **Color.new()** |
| :--- |

Color를 생성해요 
<br>
<br>
| **Color.new(number R, number G, number B, number A)** |
| :--- |

Color를 R, G, B, A 값으로 세팅하여 생성해요 
<br>
## **속성**

<br>
<br>
| **number R** |
| :--- |

빨간 색을 나타내요. (0 ~ 255) 
<br>
<br>
| **number G** |
| :--- |

초록 색을 나타내요. (0 ~ 255) 
<br>
<br>
| **number B** |
| :--- |

파란 색을 나타내요. (0 ~ 255) 
<br>
<br>
| **number A** |
| :--- |

투명도를 나타내요. (0 ~ 255) 

<br>

샘플 

```lua
local color = Color.new(255, 0, 0, 255)
local ui = Workspace.ScreenUI.Text

ui:SetTextColor(color) --텍스트 UI의 글자 색상을 변경해요.

wait(1)
local newColor = Color.new(0, 255, 255, 0)
color = color + newColor --newColor.R = 255, newColor.G = 255, newColor.B = 255, newColor.A = 255로 할당돼요.
```
<br>
