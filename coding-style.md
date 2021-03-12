# Coding Style

## 지역 변수

local로 선언한 변수를 지역 변수라고 해요.

변수 이름은 첫 글자는 대문자로 시작하고 연결되는 단어는 대문자로 시작해요.

```lua
local WorldString = "Hello world!" 
```



### 함수 안에서 선언하는 지역 변수

함수안에서 변수를 local로 선언할때는

첫 글자는 소문자로 시작하고 연결되는 단어는 대문자로 시작해요.

```lua
local function SomeFunc()
	local worldString = "Hello world!"
end
```



## 전역 변수

변수 이름은 대문자로 시작하고 연결되는 단어도 대문자로 시작해요.

```lua
TestWorld = 1
```



## 함수

함수 이름은 대문자로 시작하고 연결되는 단어도 대문자로 시작해요.

```lua
local function WorldStart()
   print("Hello World!")
end
WorldStart()
```



## 모듈

다른 스크립트에서 require로 접근해서 사용할 수 있도록 제공하는 스크립트를 모듈이라고 해요.

모듈 이름은 대문자로 시작하고 연결되는 단어도 대문자로 시작해요.

```lua
local TestModules = {}
	...
return TestModules
```



## 코딩 스타일

오브젝트의 함수는 다음과 같이 ":"으로 표시해요.

```lua
Object:StartFunction()
Object:Function1():Function2()
```



오브젝트의 변수는 다음과 같이 "."으로 표시해요.

```lua
Object.Start = 10
```



함수의 인자 값은 다음과 같이 띄어쓰기합니다.

```lua
-- 잘된 예
Object:StartFunction(1, 3, "Test")
```

```lua
-- 잘못된 예
Object:StartFunction(1,3,"Test")
```



줄 바꿈은 다음과 같이 해요.

```lua
-- 잘된 예
local Color =
{
	blue = 1,
	red  = 2 
}
```

```lua
-- 잘못된 예
local Color = {
	blue = 1,
	red  = 2 
}
```



연산은 띄어쓰기를 다음과 같이 해요.

```lua
-- 잘된 예
local Result = 10 + 20 * 3 ^ 2
```

```lua
-- 잘못된 예
local Result = 10+ 20 *3^2
```



조건문의 띄어쓰기는 다음과 같이 해요.

```lua
-- 잘된 예
if object ~= nil and value == 3 then
	...
end
```

```lua
-- 잘못된 예
if object~=nil and value ==3 then
	...
end
```


