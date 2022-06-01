---
layout: post
title:  "Hacker rank 8일차 딕셔너리와 맵 code solution"
date:   2022-06-01 18:50:30 +0900
categories: JavaScript
---

hacker rank 사이트에서 진행하는 30일 튜토리얼 문제를 푸는데 7일차까지는 쉬웠다.  
그런데 오늘 8일차 문제를 푸는데 좀 오래 걸려서 풀이를 기록하기로 했다.  

## 문제 조건
- 이름과 번호의 묶음의 갯수인 숫자 n이 주어진다.
- 한 줄에 이름과 번호가 같이 적혀있으면 그 값을 딕셔너리나 맵에 저장한다. 
- 출력형태는 이름=번호, 만약 존재하지 않는 값이라면 'Not found'를 출력한다.

## 코드
```js
function processData(input) {
    //input을 개행 기준으로 잘라서 input 배열에 저장
    var input = input.split('\n');
    // numLines에 input[0](번호 갯수) 저장
    var numLines = parseInt(input[0],10);
    // 전화번호부 역할
    var phoneBook = new Map();

    // 전부 개행으로 저장했으니까 저장된 연락처는 총 numLines*2개(원래는 이름, 번호가 한줄이어서)
    //그 뒷 줄은 출력할 이름들이라서 phoneBook에 저장 안함
    for (var i = 1; i < numLines; i++){
        // 키값으로 이름, 벨류로 번호 저장하고 i가 2씩 증가하니까 1,2; 3,4; 5,6처럼 이름, 번호 쌍으로 저장
        var inputValues = input[i].split(' ');
        phoneBook.set(inputValues[0], inputValues[1]);
    }
    // 출력은 이름 = 번호로 해야함
    // 출력할 사람의 이름은 input[numLines*2+1]부터 저장되있음
    for (var j = numLines + 1; j < input.length; j++){
        // 만약 phoneBook에 출력할 이름이 있으면 이름 = 번호 형식으로 출력
        var values = input[j].split(' ');
        // Map.has(key): 해당 key가 Map에 포함되어 있는지 확인
        if(phoneBook.has(values[0])){
          console.log(`${values[0]}=${phoneBook.get(values[0])}`);
        }
        else // 출력할 정보가 없다면 Not Found출력
          console.log('Not found');
    }
}
```

## 헤맨 부분
- let input으로 선언해서 오류 발생 => 다른 변수명을 선언하거나 var를 사용해서 해결
- numLines 이후의 값들을 어떻게 처리할지 고민 => split(' ')으로 다시 쪼개서 저장
- Map에 키,값 같이 넣는 방법이 기억 안남 => 검색결과 맵.set(키, 값) 사용