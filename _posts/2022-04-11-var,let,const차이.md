---
layout: post
title:  "var, let, const 차이점"
date:   2022-04-11 21:44:30 +0900
categories: JavaScript bootcamp
---

부트캠프 자바스크립트 파트 드디어 입성!✨  
String, numbers, boolean 등 기본적인 자료형에 대해 강의가 진행됐는데 갑자기 드는 의문!  
var, let, const의 차이가 뭐지...?  
그래서 그 차이점에 대해 찾아봤다.  

## var
- 중복 선언이 가능하다는 것이 가장 큰 특징
  ```javascript
  var a = 100;
  console.log(a); //결과값 100

  var a = 200;
  console.log(a); //결과값 200
  ```
- 위의 코드처럼 같은 변수명을 계속 선언하고 값을 넣어도 에러가 나지 않음
- 같은 변수명으로 선언할 때 마다 값을 초기화하고 새로운 값으로 저장됨
- 중복 선언의 위험이 큰 단점, 이 문제를 해결하기 위해 let과 const가 추가됨

## let
- 변수명을 중복으로 선언하면 에러가 발생
- 값을 재할당하는 경우는 가능함
  ```javascript
  let a = 100;
  console.log(a); //결과값 100

  let a = 200;
  console.log(a); //에러발생
  //SyntaxError: Indentifier 'a' has already been declared
  //중복 선언 불가능

  a = 300;
  console.log(a); //결과값 300(재할당은 가능)
  ```

## const
- let과 마찬가지로 중복으로 선언하면 에러 발생
- let과의 차이점은 const는 재할당도 불가능
- 처음 선언하고 나면 다른 값을 넣을 수 없기 때문에 상수를 선언하는 키워드로 주로 사용
  ```javascript
  const a = 100;
  console.log(a); //결과값 100

  const a = 200;
  console.log(a); //에러발생
  //SyntaxError: Indentifier 'a' has already been declared
  //중복 선언 불가능

  a = 300;
  console.log(a); //에러발생
  //Assignment to constant variable
  //값을 재할당 하는 것도 불가능
  ``` 
