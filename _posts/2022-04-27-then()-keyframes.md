---
layout: post
title:  "JS .then(), CSS @keyframes"
date:   2022-04-27 11:21:30 +0900
categories: CSS javascript bootcamp
---

.then()함수 자주 보기는 했는데 항상 "대충 이런 느낌이지~" 하고 넘어가다가 오늘 갑자기 의문이 들었다.  
.then()함수를 쓰는 이유와 이 함수는 무엇을 의미하는가?

## Promise와 then()
- js에서는 대부분의 작업들이 비동기로 이루어짐
- 어떤 작업을 요청하면서 콜백 함수를 등록하면 작업이 수행되고 나서 결과를 나중에 콜백 함수를 통해 알려주는 방식
- 복잡도가 높아지면 콜백이 중첩되기도 하는데 하나의 작업을 콘백으로 결과를 받은 뒤 순차적으로 다음 작업을 진행할 때 이런 중첩이 발생
- 콜백의 중첩을 극복하기 위해 Promise라는 패턴이 제안되었고 Promise 패턴을 사용하면 비동기 작업들의 순차적 진행, 병렬 진행등이 수월해짐
- Promise를 사용할때 콜백으로 사용할 함수를 지정할 수 있는 메서드가 **then**

## CSS Animation과 keyframes
- @keyframes
  - CSS의 문법 중 하나로 애니메이션이 만들어지는 부분
  - 애니메이션을 적용할 요소의 animation-name을 정의하고 그 코드 블럭에 재생할 프레임별 시간 비율을 작성하는 방식으로 사용
    ```css
    //애니메이션 spin이 Z방향으로 360도 회전
    @keyframes spin{
        to{
            transform: rotateZ(360deg);
        }
    }
    //spin 애니메이션이 2초 동안 일정한 속도로 진행
    .spinner{
        font-size: 50px;
        text-align: center;
        animation: 2s spin linear;
        display: none;
    }
    ```