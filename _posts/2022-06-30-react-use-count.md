---
layout: post
title: "React - useCount"
date: 2022-06-30 22:50:30 +0900
categories: JavaScript
---

사전 과제를 하면서 가장 애먹고 있는 부분인 숫자 카운팅...  
숫자 카운팅 애니메이션을 검색해보니까 많은 결과가 있었다.  
첫 번째는 jQuery로 작성하는 것  
두 번째는 React CountUp
세 번째는 use-count-up
현재 두 번째와 세 번째 모두 사용해보는 중이고 완성할때 되서야 결정할 듯

## react count up

- npm i react-countup 으로 설치하고 import해서 사용
- <CountUp start={0} end={100}/> 형태로 사용
- start는 시작 숫자, end는 끝나는 숫자
- delay값을 줘서 시작하는 타이밍을 조절할 수 있음
- duration값으로 지속시간 설정가능
- useEasing으로 Easing을 활성화할 수 있음(재생속도) false를 하면 선형전환(일정한 속도), true를 하면 다른 값으로 설정 가능
- easingFn에서 재생속도를 세세하게 설정가능 기본은 easeInExpo

## use count up

- npm i use-count-up 으로 설치하고 import해서 사용
- <CountUp isCounting start={0} end={100}/> 형태로 사용
- isCounting으로 시작 정지 설정(기본값은 false)
- start는 시작하는 숫자, end는 끝나는 숫자
- duration값으로 지속시간 설정 가능
- string이나 function을 값으로 가지는 easing으로 재생속도 조절 가능(기본값은 easeOutCubic)
