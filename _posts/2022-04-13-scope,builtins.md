---
layout: post
title:  "scope, builtins, == 과 === 차이"
date:   2022-04-12 20:50:30 +0900
categories: JavaScript bootcamp
---

항상 3주째가 고비인것 같다. 오늘치 분량 겨우겨우 클리어!!  

## scope(범위)
- 변수에 접근할 수 있는 범위
- global(전역)과 local(지역)으로 나눠짐
- 전역 스코프는 전역에 선언되어있어 어느 곳에서든지 해당 변수에 접근할 수 있음
- 지역 스코프는 변수를 선언한 해당 지역에서만 접근이 가능하기 때문에 지역을 벗어난 곳에서는 접근할 수 없음
  ```javascript
  var a = 1;//global scope
  
  function abcc(){//local scope
    var b = 2;
    console.log(a+","+b);
  }
  abcc();//result: 1,2

  console.log(a);//result: 1
  console.log(b);//result: error
  ```

## Builtins(내장함수)
- 자바스크립트 자체에 등록되어 있는 함수
- sentence.toLowerCase(), Math.round(), string.substr() 등등...
  ```javascript
  const sentence = "ThIs HaS wEiRd CaSiNg On It";
  console.log(sentence.toLowerCase());
  //result: this has weird casing on it
  console.log(Math.round(5.1));
  //result: 5
  const name = "Brian";
  console.log(name.substr(2,2));
  //result: ia
  ```

## ==, === 차이
- ==는 양 옆의 값을 비교하기 전에 강제 형변환(Type Coercion)을 수행하는데 강제 형변환 과정을 통해 피 연산자들을 공통 타입으로 만들고 그 안에 있는 값만을 비교하는 '느슨한 비교'
- ===의 경우는 강제 형변환을 수행하지 않는 '엄격한 비교'
  ```javascript
  let a = 3;
  let b = '3';
  let c = 3;

  a == b;//true
  b == c;//true
  a == c;//true
  a === b;//false
  b === c;//false
  a === c;//true
  ```
