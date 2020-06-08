# **RRemotePlayer**


클라이언트 스크립트에서 사용되는 플레이어 객체에요. [Game:GetRemotePlayer(PlayerName)](https://ditoland-utplus.gitbook.io/ditoland/api-reference/client/rgameclient)혹은 [LocalPlayer:GetRemotePlayer()](https://ditoland-utplus.gitbook.io/ditoland/api-reference/client/localplayer#undefined-1) 함수를 이용하면 얻을 수 있어요. 
| **RGameClientCharacter GetCharacter()** |
| :--- |

플레이어의 캐릭터를 얻기 
| **string GetPlayerName()** |
| :--- |

플레이어의 이름 얻기 
| **ObjectFXClient CreateFX(ObjectFXClient FXObject, Bone BoneType)** |
| :--- |

캐릭터 특정 위치에 FX 생성 (생성 할 FX 오브젝트, [Enum.Bone.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/bone)) 
| **ObjectFXClient CreateFX(String FXName, Bone BoneType)** |
| :--- |

캐릭터 특정 위치에 FX 생성 (생성 할 FX 이름, [Enum.Bone.타입](https://ditoland-utplus.gitbook.io/ditoland/api-reference/enums/bone)) 
| **ObjectSoundClient CreateSound(ObjectSoundClient SoundObject)** |
| :--- |

캐릭터의 위치에 Sound 생성 (생성 할 Sound 오브젝트) 
| **RModeHitResult LineTrace(Vector Start, Vector Dir, float Distance)** |
| :--- |

두 지점 간의 오브젝트 충돌 체크 (시작 지점 Vector, 원하는 지점 Vector, 지점 간의 거리) 
| **bool IsMyPlayer()** |
| :--- |

플레이어 자신의 플레이어인지 확인 
