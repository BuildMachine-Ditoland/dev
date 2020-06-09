# **RCharacterSetting**


게임에서 사용 될 캐릭터를 설정 할 때 사용되는 객체에요. [Game:AddCharacterSetting](https://ditoland-utplus.gitbook.io/ditoland/api-reference/server/rgameserver)함수를 이용해요 
## **속성**

| **UseSelfcharacter** |
| :--- |

자신의 캐릭터의 사용 여부 

true로 설정하면 자신의 아바타 사용, false시 ResourcePath 에 설정된 캐릭터 사용- 현재는 무조건 false 처리됨 
| **string ResourcePath** |
| :--- |

캐릭터 리소스 경로 (현재 언리얼 리소스 참조경로, 추후 리소스 아이디로 대체) 
| **int MaxLife** |
| :--- |

최대 생명 설정 

캐릭터는 해당 생명만큼 리스폰된다. -1로 설정 시 무한 리스폰 디폴트 값은 -1 
| **float RespawnTime** |
| :--- |

리스폰 타임 
| **float MoveSpeed** |
| :--- |

이동 스피드 
| **float JumpSpeed** |
| :--- |

점프 높이 
| **float FlyControlRate** |
| :--- |

공중에서 컨트롤 비율 
