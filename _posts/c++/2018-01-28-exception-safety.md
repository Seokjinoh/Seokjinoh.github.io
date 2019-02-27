---
layout: post
title: C++ 예외 안전성 보장
tags: [c++, programming, effective]
category : C++
---



layout: post
title: C++ 예외 안전성 보장
excerpt: "Effective C++"
tags: [c++, programming, effective]
modified: 2019-01-28
comments: true
category : C++



# C++ 예외 안전성 보장

`
예외 안전성을 갖춘 함수는 아래의 세 가지 보장 중 하나를 반드시 제공해야 한다. 
아무 보장도 제공하지 않으면 예외에 안전한 함수가 아니다.
`

1. 기본적인 보장 (basic guarantee)
```
함수 동작 중에 예외가 발생하면, 실행 중인 프로그램에 

관련된 모든 것들을 유효한 상태로 유지한다. 

어떤 객체나 자료구조도 더렵혀지지 않으며, 모든 객체의 상태는 내부적으로 일관성을 유지한다.

```

2. 강력한 보장 (strong guarantee)
```
함수 동작 중에 예외가 발생하면, 프로그램의 상태를 절대로 변경하지 않겠다는 보장이다. 이런 함수를 호출하는 것은 원자적인 동작이다. 

'복사-후-맞바꾸기' 방법을 써서 구현할 수 있지만,
모든 함수에 대해 강력한 보장이 실용적인 것은 아니다.
```

3. 예외불가 보장 (nothrow guarantee)
```
예외를 절대로 던지지 않겠다는 보장이다. 약속한 동작은 언제나 끝까지 완수하는 함수라는 뜻이다. 
```



출처 : Effective C++ 항목 29