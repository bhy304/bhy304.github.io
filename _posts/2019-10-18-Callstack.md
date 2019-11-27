---
layout: post
title: "자바스크립트 개발자가 알아야 하는 33가지 개념 #1 호출 스택"
tags: [JavaScript]
comments: true
---

호출 스택(Call Stack)

--- 

# 호출 스택(Call Stack)

**호출 스택**은 여러 함수들(Functions)을 호출하는 스크립트에서 해당 위치를 추적하는 인터프리터(웹 브라우저의 자바스크립트 인터프리터같은)를 위한 메커니즘이다. 
현재 어떤 함수가 동작하고 있는지, 그 함수 내에서 어떤 함수가 동작하는 지, 다음에 어떤 함수가 호출되어야 하는지 등을 제어한다. 

- 스크립트가 함수를 호출하면 인터프리터는 이를 호출 스택에 추가한 다음, 함수를 수행하기 시작한다. 

- 해당 함수에 의해 호출되는 모든 함수는 호출 스택에 추가되고 호출이 도달하는 위치에서 실행한다. 

- 메인 함수가 끝나면 인터프리터는 스택을 제거하고 메인 코드 목록에서 중단된 실행을 다시 시작한다. 

- 스택이 할당된 공간보다 많은 공ㅇ간을 차지하면 'stack overflow' 에러가 발생한다. 


Call Stack, 자바스크립트가 함수 실행을 핸들하는 방법 중 하나로 자바스크립트는 함수를 스택 위에 올리고 함수를 다 실행하면 제거한다. 

리스트가 존재한다. 함수는 리스트에 추가된다. 실행이 완료되면 함수는 리스트에서 제거된다. 

Call Stack은 자바스크립트의 To Do List와 같다. 

코드를 통해 알아보자. 

```javascript
function three() {
    console.log('I love JS');
    // throw Error('omg Im an Error');
}
function two() {
    three();
}
function one() {
    two();
}
function zero() {
    one();
    // throw Error('omg Im an Error');
}
zero();
```

![callstack](/assets/img/callstack.gif){: center-image}

---

# Reference
* [33-js-concepts](https://github.com/leonardomso/33-js-concepts)