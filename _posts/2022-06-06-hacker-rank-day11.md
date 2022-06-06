---
layout: post
title:  "Hacker rank 30Days of Code_Day11:2D Arrays"
date:   2022-06-06 17:30:30 +0900
categories: JavaScript
---

6x6 배열을 3x3인 부분 배열로 분해해서 그 부분 배열의 값을 모래시계 모양(위 3줄, 가운데 1줄, 아래 3줄)으로 더하고 그 값들 중 최대 값을 찾아라.  

## Day11: 2D Arrays
```js
function hourglass() {
    var arr = [];
    for(var arr_i = 0; arr_i < 6; arr_i++){
       arr[arr_i] = readLine().split(' ');
       arr[arr_i] = arr[arr_i].map(Number);
    }
    var arrs = []
    for (var i = 1; i < arr.length - 1;i++){
        for (var j = 1; j < arr[i].length - 1; j++){
            var sum = 0;
            // top
            sum = parseInt(arr[i-1][j-1]) + parseInt(arr[i-1][j]) + parseInt(arr[i-1][j+1]);
            // middle
            sum = sum + parseInt(arr[i][j]);
            // bottom
            sum = sum + parseInt(arr[i+1][j-1]) + parseInt(arr[i+1][j]) + parseInt(arr[i+1][j+1]);
            arrs.push(sum);
        }
    }
    //console.log(arrs);
    console.log(Math.max.apply(null, arrs));
}
```

## 어려웠던 점
1. 3x3 부분 배열을 생성하는 부분을 구현 못하겠어서 고민함
  - 해결: 3x3을 구할 필요 없이 처음부터 모래시계 모양으로 값을 더하면 됨
2. 모래시계 모양으로 더한 값 중 최대값을 구하는 방법
  - 해결: 더한 결과값을 모아두는 배열을 따로 만들어서 저장한 다음 max 함수를 사용해서 최대 값 출력