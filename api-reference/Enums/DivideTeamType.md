
팀 인원 설정을 정하는 타입이에요. 
<br>
## **Enums**

 **이름** | **설명** |
 --- | --- |
**Equal** |플레이어들을 균등하게 팀을 나눠요. |
**Order** |플레이어들을 순서에 따라 팀을 나눠요. |
**Rate** |플레이어들을 비율에 따라 팀을 나눠요. |

샘플 

```lua
Game:SetTeamSetting(Enum.DivideTeamType.Order) --팀에 플레이어를 분배하는 방식을 설정해요.
```
