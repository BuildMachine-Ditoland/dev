# **RCharacterClient**


클라이언트에서 사용되는 캐릭터 개체에요. 
## **함수**

| **string GetPlayerName()** |
| :--- |

플레이어 이름 얻기 
| **FRModeAnimStateMachine AddAnimStateMachine(string StateMachineName)** |
| :--- |

Game:AddAnimStateMachineSetting로 추가된 상태 머신 중 애니메이션 상태 머신을 추가 (상태 머신 이름) 
| **FRModeAnimStateMachine GetAnimStateMachine(string StateMachineName)** |
| :--- |

해당 애니메이션 상태 머신 얻기 (얻고싶은 상태 머신 이름) 
| **RModeAnimStateBase GetCurAnimState()** |
| :--- |

현재 애니메이션 상태 얻기 
| **ChangeAnimState(string AnimState)** |
| :--- |

해당 애니메이션 상태로 변경 (변경하고 싶은 애니메이션 상태 이름) 
| **ChangeAnimStateMachine(string ChangeStateMacnine)** |
| :--- |

해당 애니메이션 상태 머신 변경 (변경하고 싶은 상태 머신 이름) 
| **bool IsFly()** |
| :--- |

캐릭터가 공중에 떠 있는지 나타낸다. 
| **bool IsDriving()** |
| :--- |

캐릭터가 탈 것을 운전 중인지 나타낸다. 
| **float GetMoveSpeed()** |
| :--- |

현재 이동 속도 얻기 
| **ObjectFXClient CreateFX(ObjectFXClient FXObject, Bone BoneType)** |
| :--- |

캐릭터 특정 위치에 FX 생성 (생성 하고싶은 FX 오브젝트, [Enum.BoneType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/bone)) 
| **ObjectFXClient CreateFX(String FXName, Bone BoneType)** |
| :--- |

캐릭터 특정 위치에 FX 생성 (생성 하고싶은 FX 이름, [Enum.BoneType.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/bone)) 
| **ObjectSoundClient CreateSound(ObjectSoundClient SoundObject)** |
| :--- |

캐릭터의 위치에 Sound 생성 (생성 하고싶은 Sound 오브젝트) 
| **AddPlayerHUD(string UIName)** |
| :--- |

UI HUD 붙이기 (붙이고 싶은 UI 이름) 
| **RemovePlayerHUD(string UIName)** |
| :--- |

UI HUD 제거하기 (제거하고 싶은 UI 이름) 
| **GetPlayerHUD(string UIName)** |
| :--- |

UI HUD 얻기 (얻고싶은 UI 이름) 
| **bool IsMyCharacter()** |
| :--- |

플레이어 자신의 캐릭터인지 확인 
| **Vector GetLocation()** |
| :--- |

현재 캐릭터 위치 얻기 
