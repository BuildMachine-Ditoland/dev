# **RGameClient**


게임 전반적인 역할을 하는 객체에요. 여기 있는 기능들은 클라이언트에서만 사용할 수 있어요. 
## **이벤트**

| **ReceiveGameStatisticsDataEvent** |
| :--- |

서버로 부터 게임 통계 데이터 받았을 때 발생하는 이벤트 
## **함수**

| **RModeRemotePlayer GetRemotePlayer(string PlayerName);** |
| :--- |

이름으로 플레이어 얻기 (플레이어 이름) 
| **RGameClientCharacter GetRemotePlayerCharacter(string PlayerName)** |
| :--- |

플레이어 이름으로 해당 플레이어 캐릭터 얻기 (플레이어 이름) 
| **int GetPlayerCount** |
| :--- |

현재 게임에 참여하고 있는 플레이어 수 얻기 
| **SendEventToServer(string EventName, Args ... )** |
| :--- |

서버에 커스텀 이벤트 보내기 (이벤트 이름, 전달하고 싶은 변수들 ...) 
| **RModeSequenceAnimStateSetting AddAnimStateMachineSetting(string StateMachineName)** |
| :--- |

캐릭터에 사용될 애니메이션 상태머신 설정 추가 (설정할 상태머신 이름) 
| **RModeSequenceAnimStateSetting GetAnimStateMachineSetting(string StateMachineName)** |
| :--- |

설정된 애니메이션 상태머신 얻기 (얻고 싶은 상태머신 이름) 
| **SetCharacterAnimStateMachine(string CharacterSettingName, string AnimStateMachineSettingName)** |
| :--- |

해당 캐릭터 설정, 해당 애니메이션 상태 머신 사용하게 설정 (설정한 캐릭터세팅 이름, 애니메이션 상태 머신 이름) 
| **SetNPCAnimStateMachine(string NPCSettingName, string AnimStateMachineSettingName)** |
| :--- |

해당 NPC 설정, 해당 애니메이션 상태 머신 사용하게 설정 (설정한 NPC 이름, 애니메이션 상태 머신 이름) 
| **RModeCameraSetting AddCameraSetting(string CameraSettingName)** |
| :--- |

카메라 설정을 추가한다 (설정한 카메라 세팅 이름) 
| **ChangeCameraOffsetDelta(Vector Offset, float Time)** |
| :--- |

카메라를 주어진 시간 동안 해당 값만큼 이동 시킨다 (이동 시킬 Vector 값, 이동 시간) 
| **ChangeCameraOffsetAbs(Vector Offset, float Time)** |
| :--- |

카메라를 주어진 시간 동안 해당 값으로 이동 한다. (이동 할 Vector 값, 이동 시간) 
| **RestoreCameraOffset(float Time)** |
| :--- |

카메라를 초기 Offset으로 주어진 시간 동안 이동 시킨다. (이동 시간) 
| **ObjectFXClient CreateFX(ObjectFXClient FXObject, Vetor Location)** |
| :--- |

FX 생성 (생성 할 FX 오브젝트, 생성할 위치) 
| **ObjectFXClient CreateFX(String FXName, Vetor Location)** |
| :--- |

FX 생성 (생성 할 FX 이름, 생성할 위치) 
| **DeleteFX(ObjectFXClient Object)** |
| :--- |

FX 제거 (FX 오브젝트) 
| **ObjectSoundClient PlaySound(ObjectSoundClient SoundObject, Vetor Location)** |
| :--- |

사운드 플레이 (플레이 할 Sound 오브젝트, 플레이 할 위치 Vector) 
| **ObjectSoundClient PlaySound(String SoundObjectName)** |
| :--- |

사운드 플레이 (플레이 할 Sound 이름) 
| **ObjectSoundClient PlaySound(String SoundObjectName, Vector Location)** |
| :--- |

사운드 플레이 (플레이 할 Sound 이름, 플레이 할 위치 Vector) 
| **StopSound(String SoundName)** |
| :--- |

플레이 중인 사운드 정지 (정지할 Sound 이름) 
| **CreateObject(string ObjectName, Vector Location)** |
| :--- |

지정된 위치에 오브젝트를 생성 한다 (생성 할 Object 이름, 생성 할 위치 Vector) 
| **CreateObject(RScriptWorldObject Object, Vector Location)** |
| :--- |

지정된 위치에 오브젝트를 생성한다 (생성 할 Object, 생성 할 위치 Vector) 
