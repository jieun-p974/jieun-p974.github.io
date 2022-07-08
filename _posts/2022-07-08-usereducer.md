---
layout: post
title: "react - useReducer"
date: 2022-07-08 19:49:30 +0900
categories: JavaScript
---

useReducer는 React 내장 훅으로 useState와 비슷한 역할을 하지만 더 복잡한 State 관리에 적합

## useReducer

- useState처럼 State를 관리하고 업데이트 할 수 있는 Hook
- 한 컴포넌트 내에서 State를 업데이트하는 로직 부분을 그 컴포넌트로부터 분리시키는 것을 가능하게 해줌
- useState의 경우 컴포넌트 내부에 State 업데이트 로직이 존재하는 반면 useReducer는 컴포넌트 외부에 State 업데이트 로직이 존재
- 컴포넌트 외부에서 State 업데이트를 하기 때문에 컴포넌트로부터 State 관리 로직을 분리시킬 수 있음

## useState와 useReducer

- useState
  - 관리해야 할 state가 1개일 경우 추천
  - state가 단순한 숫자, 문자열 또는 boolean 값일 경우에 사용
- useReducer
  - 관리할 state가 1개 이상
  - 단일 state라도 유동적인 값을 가질 경우
  - 스케일이 큰 프로젝트
  - state 구조가 복잡할 때
