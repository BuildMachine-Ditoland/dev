
로그를 종류별로 출력하는 객체에요. 
<br>
## **Enums**

 **이름** | **설명** |
 --- | --- |
<br>
## **함수**

<br>
| **Log(string message)** |
| :--- |

일반 로그 메시지를 출력해요. (메시지 내용) 

샘플 

```lua
Logger:Log(Enum.LogType.Log, "Hello Log!") --로그창에 일반 로그를 출력해요.
Logger:Log(Enum.LogType.Warning, "Hello Warning!") --로그창에 경고 로그를 출력해요.
Logger:Log(Enum.LogType.Error, "Hello Error!") --로그창에 에러 로그를 출력해요.
Logger:Log(Enum.LogType.Log, "You're the %d %s", 100, "th Player.") --로그창에 숫자와 문자열을 참조하는 메시지를 출력해요. (%d는 숫자, %s는 문자열을 참조하는 기호에요.)
```
