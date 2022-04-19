---
layout: post
title:  "Array.prototype.includes"
date:   2022-04-19 19:50:30 +0900
categories: JavaScript bootcamp
---

케이크🍰 먹어서 행복한 기분으로 공부 완료! 
퀴즈 풀었는데 몇개는 혼자서 몇개는 답지 보고 풀었다...  
아직 한참 멀었네.. 그래도 파이팅! 할 수 있다.  
퀴즈에서 틀린 문제를 정리 GOGO  

## 배열 내에서 가장 큰 숫자 찾기 함수
- 조건: 배열 list 내에서 가장 큰 값을 찾아서 반환
- 틀린 이유 return을 안함
  ```javascript
  function findLargestNumber(list){
    let largest = list[0];
    for(let i = 0; i < list.length; i++){
      if(list[i]>largest){
        largest = list[i];
      }
    }
    return largest;
  }
  ```

## 모든 Engineer들의 이름 찾기 함수
- 조건: 객체 list에서 jobTitle이 "Engineer"인 사람들의 name을 반환
- 틀린 이유: 반복 횟수를 list.length로 해야하는데 name.length로 함
  ```javascript
  function getAllEngineers(list){
    const name = [];
    for(let i = 0; i < list.length; i++){
      if(list[i].jobTitle.includes("Engineer")){
        names.push(list[i].name);
      }
    }
    return names;
  }
  ```
- includes method: 특정 문자열이 포함되어 있는지 확인하는 메서드
- push method: 배열의 끝에 하나 이상의 요소를 추가하고, 배열의 새로운 길이를 반환