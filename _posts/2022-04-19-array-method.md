---
layout: post
title:  "Array.prototype.includes"
date:   2022-04-19 19:50:30 +0900
categories: JavaScript bootcamp
---

์ผ์ดํฌ๐ฐ ๋จน์ด์ ํ๋ณตํ ๊ธฐ๋ถ์ผ๋ก ๊ณต๋ถ ์๋ฃ! 
ํด์ฆ ํ์๋๋ฐ ๋ช๊ฐ๋ ํผ์์ ๋ช๊ฐ๋ ๋ต์ง ๋ณด๊ณ  ํ์๋ค...  
์์ง ํ์ฐธ ๋ฉ์๋ค.. ๊ทธ๋๋ ํ์ดํ! ํ  ์ ์๋ค.  
ํด์ฆ์์ ํ๋ฆฐ ๋ฌธ์ ๋ฅผ ์ ๋ฆฌ GOGO  

## ๋ฐฐ์ด ๋ด์์ ๊ฐ์ฅ ํฐ ์ซ์ ์ฐพ๊ธฐ ํจ์
- ์กฐ๊ฑด: ๋ฐฐ์ด list ๋ด์์ ๊ฐ์ฅ ํฐ ๊ฐ์ ์ฐพ์์ ๋ฐํ
- ํ๋ฆฐ ์ด์  return์ ์ํจ
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

## ๋ชจ๋  Engineer๋ค์ ์ด๋ฆ ์ฐพ๊ธฐ ํจ์
- ์กฐ๊ฑด: ๊ฐ์ฒด list์์ jobTitle์ด "Engineer"์ธ ์ฌ๋๋ค์ name์ ๋ฐํ
- ํ๋ฆฐ ์ด์ : ๋ฐ๋ณต ํ์๋ฅผ list.length๋ก ํด์ผํ๋๋ฐ name.length๋ก ํจ
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
- includes method: ํน์  ๋ฌธ์์ด์ด ํฌํจ๋์ด ์๋์ง ํ์ธํ๋ ๋ฉ์๋
- push method: ๋ฐฐ์ด์ ๋์ ํ๋ ์ด์์ ์์๋ฅผ ์ถ๊ฐํ๊ณ , ๋ฐฐ์ด์ ์๋ก์ด ๊ธธ์ด๋ฅผ ๋ฐํ