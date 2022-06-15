---
layout: post
title: "Destructuring(구조 분해 할당)"
date: 2022-06-15 20:20:30 +0900
categories: JavaScript
---

리액트 강의인데 js를 한번 싹 복습해 주는 게 이 강의의 장점인 것 같다.  
까먹거나 헷갈렸던 부분 복습하는 기분으로 찬찬히 듣는 중

## Destructuring(구조 분해 할당)

- 스프레드와 비슷하다고 생각할 수 있지만 다름
- 스프레드: 모든 원소와 프로퍼티를 가져와서 새 배열이나 객체 또는 여러분이 사용하는 어떤 것에 전달
- Destructuring: 원소나 프로퍼티를 하나만 가져와 변수에 저장
  ```js
  const numbers = [1, 2, 3];
  [num1, , num3] = numbers;
  console.log(num1, num3); // 1 3
  ```

## 참조형 데이터 타입

- 객체와 배열은 참조형 데이터 타입
- 참조형을 복사하면 복사한 객체에 복사된 객체의 포인터가 저장됨
- 포인터를 복사하는 것이 아니라 프로퍼티를 복사해야 복사한 객체가 복사된 객체의 값의 변화에 영향을 받지 않음

  ```js
  const person = {
    name: "Jack",
  };
  //포인터를 복사
  const secondPerson = person;
  //프로퍼티를 복사
  const thirdPerson = {
    ...person,
  };
  person.name = "Maru";

  console.log(secondPerson); //name: "Maru"
  console.log(thirdPerson); //name: "Jack"
  ```
