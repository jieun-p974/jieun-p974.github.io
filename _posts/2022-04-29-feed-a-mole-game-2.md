---
layout: post
title:  "두더지 밥주기 게임2-JS"
date:   2022-04-29 12:10:30 +0900
categories: JavaScript bootcamp
---

귀여운 두더지한테 밥주는 미니 게임을 만드는 실습 완성

## 게임 실행 화면
![feed a mole](https://user-images.githubusercontent.com/84063843/165883143-e3179a2a-3d2e-4712-8f98-66289769232e.gif)
- 배고픈 두더지한테 밥을 주면 점수가 올라가는데 왕관을 쓴 왕두더지는 점수가 두배, 일정 점수를 채우면 게임 클리어

## JavaScript
- 두더지/왕두더지가 배고플때, 음식을 먹을 때, 떠날 때 각각의 이미지를 상황에 맞게 표시하는 코드
  ```js
  switch (mole.status) {
    case "sad":
    case "fed":
      mole.next = getSadInterval();
      if (mole.king) {
        mole.node.children[0].src = "./king-mole-leaving.png";
      } else {
        mole.node.children[0].src = "./mole-leaving.png";
      }
      mole.status = "leaving";
      break;
    case "leaving":
      mole.next = getInterval();
      mole.king = false;
      mole.node.children[0].classList.toggle("gone", true);
      mole.status = "gone";
      break;
    case "hungry":
      mole.node.children[0].classList.toggle("hungry", false);
      if (mole.king) {
        mole.node.children[0].src = "./king-mole-sad.png";
      } else {
        mole.node.children[0].src = "./mole-sad.png";
      }
      mole.status = "sad";
      mole.next = getSadInterval();
      break;
    case "gone":
      mole.status = "hungry";
      mole.king = getKingStatus();
      mole.next = getHungryInterval();
      mole.node.children[0].classList.toggle("hungry", true);
      mole.node.children[0].classList.toggle("gone", false);
      if (mole.king) {
        mole.node.children[0].src = "./king-mole-hungry.png";
      } else {
        mole.node.children[0].src = "./mole-hungry.png";
      }
      break;
  }
  ```
- 게임 클리어했을 때 화면 전환
  ```js
  const win = () => {
    document.querySelector(".bg").classList.toggle("hide", true);
    document.querySelector(".win").classList.toggle("show", true);
  };
  ```