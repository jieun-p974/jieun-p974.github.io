---
layout: post
title: "width와 flex-basis 차이"
date: 2022-07-04 18:50:30 +0900
categories: CSS
---

flex-basis와 width 둘 다 똑같이 너비를 제어하는데 둘의 차이를 정확하게 알고 싶어서 검색해봄

## flex-basis와 width 차이점

- flex-basis는 flex-item에만 적용되고 width는 전부 적용 가능(flex-basis는 container에는 적용 안됨)
- flex-basis는 flex-direction의 방향에 따라 가로로 늘리거나 세로로 늘림
- 절대적으로 배치된 flex항목은 flex-basis의 영향을 받지 않음

```css
.container {
  display: flex;
  flex-direction: row;
  width: 800px;
}
.item {
  flex-basis: 100px;
}
```
