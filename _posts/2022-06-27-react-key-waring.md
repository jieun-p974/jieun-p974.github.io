---
layout: post
title: "key warning이 뜨는 이유"
date: 2022-06-27 23:20:30 +0900
categories: JavaScript
---

map 함수를 쓰는데 key warning이 발생  
key warning은 왜 생기는 걸까?

## Key warning

- key
  - 리액트가 어떤 항목을 변경, 추가 또는 삭제할 지 식별하는 것을 돕는 것이 key의 역할
  - 요소에 안정적인 고유성을 부여하고 배열 내부의 요소에 지정해야 한다.
- 즉 key warning이 발생하는 이유는 요소들을 구분할 고유성 있는 key가 없어서
- 이 경고를 해결하려면 각 요소마다 고유의 key 값을 설정해주면 되는데 보통 데이터의 id를 key로 사용(고유성 때문)
