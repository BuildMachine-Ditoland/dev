
키 버튼 타입이에요 
<br>
## **Enums**

 **이름** | **설명** |
 --- | --- |
**MouseX** |Input Key Binding |
**MouseY** |Input Key Binding |
**MouseScrollUp** |Input Key Binding |
**MouseScrollDown** |Input Key Binding |
**MouseWheelAxis** |Input Key Binding |
**LeftMouseButton** |Input Key Binding |
**RightMouseButton** |Input Key Binding |
**MiddleMouseButton** |Input Key Binding |
**BackSpace** |Input Key Binding |
**Tab** |Input Key Binding |
**Enter** |Input Key Binding |
**Pause** |Input Key Binding |
**CapsLock** |Input Key Binding |
**Escape** |Input Key Binding |
**SpaceBar** |Input Key Binding |
**PageUp** |Input Key Binding |
**PageDown** |Input Key Binding |
**End** |Input Key Binding |
**Home** |Input Key Binding |
**Left** |Input Key Binding |
**Up** |Input Key Binding |
**Right** |Input Key Binding |
**Down** |Input Key Binding |
**Insert** |Input Key Binding |
**Delete** |Input Key Binding |
**Zero** |Input Key Binding |
**One** |Input Key Binding |
**Two** |Input Key Binding |
**Three** |Input Key Binding |
**Four** |Input Key Binding |
**Five** |Input Key Binding |
**Six** |Input Key Binding |
**Seven** |Input Key Binding |
**Eight** |Input Key Binding |
**Nine** |Input Key Binding |
**A** |Input Key Binding |
**B** |Input Key Binding |
**C** |Input Key Binding |
**D** |Input Key Binding |
**E** |Input Key Binding |
**F** |Input Key Binding |
**G** |Input Key Binding |
**H** |Input Key Binding |
**I** |Input Key Binding |
**J** |Input Key Binding |
**K** |Input Key Binding |
**L** |Input Key Binding |
**M** |Input Key Binding |
**N** |Input Key Binding |
**O** |Input Key Binding |
**P** |Input Key Binding |
**Q** |Input Key Binding |
**R** |Input Key Binding |
**S** |Input Key Binding |
**T** |Input Key Binding |
**U** |Input Key Binding |
**V** |Input Key Binding |
**W** |Input Key Binding |
**X** |Input Key Binding |
**Y** |Input Key Binding |
**Z** |Input Key Binding |
**NumPadZero** |Input Key Binding |
**NumPadOne** |Input Key Binding |
**NumPadTwo** |Input Key Binding |
**NumPadThree** |Input Key Binding |
**NumPadFour** |Input Key Binding |
**NumPadFive** |Input Key Binding |
**NumPadSix** |Input Key Binding |
**NumPadSeven** |Input Key Binding |
**NumPadEight** |Input Key Binding |
**NumPadNine** |Input Key Binding |
**Multiply** |Input Key Binding |
**Add** |Input Key Binding |
**Subtract** |Input Key Binding |
**Decimal** |Input Key Binding |
**Divide** |Input Key Binding |
**F1** |Input Key Binding |
**F2** |Input Key Binding |
**F3** |Input Key Binding |
**F4** |Input Key Binding |
**F5** |Input Key Binding |
**F6** |Input Key Binding |
**F7** |Input Key Binding |
**F8** |Input Key Binding |
**F9** |Input Key Binding |
**F10** |Input Key Binding |
**F11** |Input Key Binding |
**F12** |Input Key Binding |
**NumLock** |Input Key Binding |
**ScrollLock** |Input Key Binding |
**LeftShift** |Input Key Binding |
**RightShift** |Input Key Binding |
**LeftControl** |Input Key Binding |
**RightControl** |Input Key Binding |
**LeftAlt** |Input Key Binding |
**RightAlt** |Input Key Binding |
**LeftCommand** |Input Key Binding |
**RightCommand** |Input Key Binding |
**Semicolon** |Input Key Binding |
**Equals** |Input Key Binding |
**Comma** |Input Key Binding |
**Underscore** |Input Key Binding |
**Hyphen** |Input Key Binding |
**Period** |Input Key Binding |
**Slash** |Input Key Binding |
**Tilde** |Input Key Binding |
**LeftBracket** |Input Key Binding |
**Backslash** |Input Key Binding |
**RightBracket** |Input Key Binding |
**Apostrophe** |Input Key Binding |
**Ampersand** |Input Key Binding |
**Asterisk** |Input Key Binding |
**Caret** |Input Key Binding |
**Colon** |Input Key Binding |
**Dollar** |Input Key Binding |
**Exclamation** |Input Key Binding |
**LeftParentheses** |Input Key Binding |
**RightParentheses** |Input Key Binding |
**Quote** |Input Key Binding |
**Gamepad_LeftX** |Input Key Binding |
**Gamepad_LeftY** |Input Key Binding |
**Gamepad_RightX** |Input Key Binding |
**Gamepad_RightY** |Input Key Binding |

샘플 

```lua
Input:AddGroup("UIInput") --조작그룹을 추가해요.
Input:AddActionKeyEvent("UIInput", "MenuKey", Enum.Key.M) --조작 키 이벤트를 추가해요.
Input:ActiveGroup("UIInput") --조작그룹을 활성화해요.
```
