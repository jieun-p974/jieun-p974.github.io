---
layout: post
title: "react - useEffect"
date: 2022-07-07 20:06:30 +0900
categories: JavaScript
---

useEffect는 리액트의 주 역할(UI 렌더링, 사용자 입력에 반응)을 제외한 다른 모든 작업(side effect)을 실행할 수 있도록 하는 react hook

## useEffect

- useEffect는 인자가 2개 필요함
  - 첫번째 인자: 의존성이 변경될때마다 실행할 함수
  - 두번째 인자: 배열형태로 함수를 실행시킬 조건
- 두번째 인자에 넣은 값이 업데이트될 때마다 useEffect가 실행됨
- 두번째 인자는 생략가능한데 만약 생략했다면 해당 컴포넌트가 렌더링될 때마다 useEffect가 실행됨
- cleanup
  - useEffect가 반환하는 함수
  - 특정 값이 업데이트되기 직전에 cleanup 함수를 실행하고 싶다면 두번째 인자에 값을 넣으면 됨
