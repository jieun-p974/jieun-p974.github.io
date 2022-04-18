---
layout: post
title:  "Looping Array"
date:   2022-04-18 20:00:30 +0900
categories: til
---

기운차게 시작하는 월요일🌟  
객체랑 배열 차이, 배열을 반복하는 방법, 배열의 메소드들을 정리!  

## 객체와 배열의 차이
||객체|배열|
|----|-------|-------|
|정의|현실의 사물을 프로그래밍에 반영|단순하게 같은 자료형의 나열|
|index|❌|⭕|
|data type|object|object|
|key|⭕|❌|
- [배열]은 index가 있어서 틀이 있고 순서가 있는 데이터를 다룰 때 좋고 {객체}는 틀이 불특정한 Thing(물건, 물체)를 다룰 때 좋음

## 배열의 반복
1. for: 가장 기본적인 반복문
    ```javascript
    const arr = [10,20,30]
    for(let i = 0; i < arr.length; i++)
    {console.log(arr[i])}
    //result: 10
    //20
    //30
    ```
2. for of: String, Array, Map, Set, DOM컬랙션등의 이터러블 순회 전용
   ```javascript
   const arr = [10,20,30]
   for(const item of arr)
   {console.log(item)}
   //result: 10
   //20
   //30
   ```
3. forEach(): 배열 길이 만큼 반복하여 콜백함수를 호출
   ```javascript
   const arr = [10,20,30]
   arr.forEach(function(item.index,arr2){
     console.log(`${index}: ${value}`);
     //result
     //0: 10
     //1: 20
     //2: 30
   })
   ```

## 배열의 메소드
- map()
  - 주로 주어진 배열의 값을 재정의 할 때 사용
  - 객체를 직접 사용하거나 변형시키지 않지만 callback을 통해 수정할 수 있음
  ```javascript
  const arrs = [10,20,30,40];
  const result = arr.map(arr => arr*arr);

  console.log(arrs);
  //[100,400,900,1600]
  ```
- filter()
  - 특정 조건을 만족하는 새로운 배열을 필요로 할 때 사용
  ```javascript
  const arrs = [1,2,3,4]
  const result = arrs.filter(arr => arr<3);
  console.log(arrs);
  //[1,2,3,4]
  console.log(result);
  //[1,2]
  ```