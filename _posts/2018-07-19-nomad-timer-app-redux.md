---
layout: post
title:  "Nomad Timer App (Redux)"
date:   2018-07-19 00:09:11 +0900
categories: react redux
---

#5 Creating Button : Component

```
import {FontAwesome} from "@expo/vector-icons";
```

expo.github.io/vector-icons

TouchableOpacity component: 눌렀을 때 투명도가 높아짐

onPressOut: 버튼을 뗄 때 실행되도록.

#6 Installing Redux and React Redux
redux 는 다른 프래임워크나 라이브러리 (angular, jquery) 등에 쓰일 수 있음
redux 와 react-redux 설치

#7 Intro to Redux
Redux: state management for react

- component 는 local state 가 있고 app 은 global state 가 있음
- 가끔은 state 가 공유되어야 함 (e.g, 로그인 여부)
- global shared state 를 저장하는 것이 redux 의 역할
- Redux = State container

- Redux 를 쓰지 않을 때 문제점: flying props. prop 이 필요하지 않은 component 도 하위 component 에 전달을 위해서 있어야 함

- global state 는 한 object(store)에 저장됨
- state 가 복잡해 질 수 있기 때문에 수정할 때 엄격한 룰이 있음
  - state 를 수정하려면 'dispatch (send) an action'을 해야함
  - 이 action 은 reducer 에게 보내지고, reducer 는 여러분을 대신해서 state 를 수정

#9 Practicing Javascript Switch
switch statement

#10 Creating the tomato reducer
redux ducks 방식 사용 (기존 책, 사이트에서 설명하는 방식과 다르다고 함)

```
//import

//Actions

// Action Creators

// Reducer

// Reducer functions

// Export Action Creators

// Export Reducer
```

functional programming

액션을 보낼 때마다 redux 는 자동으로 reducer 를 실행

#11 Connecting the Components to State
Provider 의 역할: 스토어를 복사해서 children 컴포넌트에 넣는 것

컴포넌트는 props 를 리덕스 store 에서 얻는다.

`connect(mapStateToProps)(Timer)`
`Timer`의 `index` 컴포넌트는 리듀서에게 state 를 받아오고 (`mapStateToProps`), `Timer`의 `presenter` 컴포넌트에 state 전달

`mapStateToProps`은 `Timer`에서 사용할 state 속성을 선택하는 역할을 함. store 에 모든 state 속성이 필요한 건 아니기 때문.

#12
컴포넌트에서 액션을 reducer 로 보내는 방법

디스패치는 액션을 리듀서로 보내는 function
`bindActionCreators(tomatoActions.startTimer, dispatch)`로 액션을 dispatch 에 묶어줌
`connect(mapStateToProps, mapDispatchToProps)(Timer)`로 dispatch 를 `Timer`로 전달

#13 Practicing Interval

```
var interval = setInterval(function(){console.log("hello")}, 1000);
clearInterval(interval);
```

#14 Adding seconds to the counter
`ComponentWillReceiveProps`: Props 가 변경될 때 호출됨. Mount 되었을땐 호출 안됨.
