---
layout: post
title: "react - context API"
date: 2022-07-11 11:27:30 +0900
categories: JavaScript
---

context를 이용하면 단계마다 일일이 props를 넘겨주지 않고도 컴포넌트 트리 전체에 데이터를 제공할 수 있음

## context

- react 컴포넌트 트리 안에서 전역적이라고 볼 수 있는 데이터를 공유할 때 사용(로그인한 유저, 테마, 선호하는 언어 등)
- context를 사용하면 엘리먼트들에게 props를 넘겨주지 않아도 됨
- createContext를 사용해 상태를 저장(initialState에 초기 상태값을 객체 형태로 넣으면 됨)
  ```js
  const SomethingStateContext = createContext(initialState);
  ```

## redux와 contextAPI 차이

- 둘다 전역 상태를 관리한다는 점에서는 유사하지만 사용법에 차이가 있음
- 단순 전역 상태 관리만 필요하다면 ContextAPI, 디버깅이나 로깅 등의 기능이 필요하다면 Redux를 사용하는 것이 좋음
- ContextAPI는 dependency 없이 사용할 수 있어서 가볍게 사용할 수 있다는 장점이 있지만 상태를 넘겨줄 상태가 여러 개일때는 Provider를 중첩해야한다는 단점
- Redux는 saga, thunk와 같은 미들웨어를 추가적으로 사용해 비동기처리를 따로 할 수 있다는 장점이 있지만 미들웨어를 사용하기 위해 관련 개념을 이해해야 하기 때문에 어렵다는 단점
