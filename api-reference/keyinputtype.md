# KeyInputType

키를 입력 할 때 이벤트가 언제 발생할지 정하는 타입이에요.   


## **Enums**

| **이름** | **설명** |
| :--- | :--- |
| **Pressed** | 키를 눌렀을 때 이벤트가 발생해요. |
| **Released** | 키를 떼었을 때 이벤트가 발생해요. |
| **Repeat** | 키를 계속 누르고 있을 때 이벤트가 발생해요. |
| **DoubleClick** | 키를 더블 클릭 했을 때 이벤트가 발생해요. |

샘플

```lua
Input:AddGroup("UIInput") --조작그룹을 추가해요.
Input:AddActionKeyEvent("UIInput", "MenuKey", Enum.Key.M) --조작 키 이벤트를 추가해요.
Input:ActiveGroup("UIInput") --조작그룹을 활성화해요.

LocalPlayer:ProcessInputActionEvent("MenuKey", Enum.KeyInputType.Pressed, function() --조작이 발생했을때 처리할 이벤트를 등록해요.
    print("Input!")
end)
```

