---
layout: post
title:  "두더지 밥주기 게임"
date:   2022-04-28 11:10:30 +0900
categories: HTML CSS bootcamp
---

귀여운 두더지한테 밥주는 미니 게임을 만드는 실습을 진행  

## HTML
- 두더지가 나올 구멍을 9개 뚫어주고 두더지한테 줄 지렁이, 게임을 끝냈을 때 보여줄 화면을 설정
- 두더지가 나올 구멍을 hole-container로 지정하고 각각의 구멍은 hole-1, hole-2등 숫자를 붙여줌
- 지렁이가 있는 컨테이너는 worm-container
- 게임 종료시 나오는 화면은 win

## CSS
- 배경과 두더지가 나오는 구멍을 설정하고 지렁이와 게임종료 화면은 숨김
  ```css
    ///배경 이미지
    background-image: url(~~.png);
    //각 클래스를 flex로 설정한 다음 전부 가운데 정렬시켜서 지렁이 박스 숨김
    display: flex;
    justify-content: center;
    align-items: center;
  ```