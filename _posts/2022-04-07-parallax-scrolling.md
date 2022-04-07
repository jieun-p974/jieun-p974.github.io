---
layout: post
title:  "Parallax Scrolling(패럴랙스 스크롤링)"
date:   2022-04-07 20:15:00 +0900
categories: HTML CSS
---

웹사이트에서 사용되는 기술인 패럴랙스 스크롤링.  
스크롤에 따라서 오브젝트와 배경 이미지가 시간차를 두고 변하는 기법이다.
여러 사이트들을 구경하다가 너무 멋진 페이지가 있길래 어떤 기술을 쓴 건지 찾아봤는데 그게 패럴랙스 스크롤링이었다.  
패럴랙스 스크롤링을 적용한 웹 페이지들도 더 찾아봤는데 동화처럼 스토리가 진행되는 페이지도 있고 점점 더 깊은 바닷속으로 들어가는 듯한 페이지도 있었다.  

## Parallax Scroll 적용 방법
- 영역 요소에 background-attachment: fixed;를 선언하고 background를 설정
  ```css
  div:nth-child(1){
  background : url(백그라운드 이미지 url) no-repeat center;
  background-size : cover;
  background-attachment : fixed;
  }
  ```
