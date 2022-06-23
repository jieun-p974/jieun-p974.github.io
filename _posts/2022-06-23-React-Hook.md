---
layout: post
title: "React Hook - useState"
date: 2022-06-23 21:20:30 +0900
categories: JavaScript
---

React Hook은 React에서 기존에 사용하던 Class를 이용한 코드를 작성할 필요 없이, state와 여러 React 기능을 사용할 수 있도록 만든 라이브러리

## React Hook

- 함수 컴포넌트도 클래스 컴포넌트처럼 사용할 수 있음
- Hook은 여러번 호출 가능
- useState, useEffect, useContext, useReducer 등이 있음

## useState

- 컴포넌트의 상태(state)를 관리할 수 있음
- 상태에 따라 다른 화면 출력
- react에서 사용자의 반응에 따라 화면을 바꿔주기 위해 사용되는 트리거 역할을 함

```js
import { useState } from "react";

// const [state, state변경함수] = useState(기본 값);
const [title, setTitle] = useState("");

// state값을 Update로 변경
// "="를 사용하는 것이 아니라 state 변경함수를 사용해야 함
setTitle("Update");
```
