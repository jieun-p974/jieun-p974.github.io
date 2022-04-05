---
layout: post
title:  ""
date:   2022-04-05 20:02:00 +0900
categories: HTML CSS bootcamp
---

## input태그의 hidden 타입은 언제 쓰는거지?
- hidden은 사용자에게는 보이지 않는 숨겨진 필드를 정의
- 폼 제출 시 사용자가 변경해서는 안되는 데이터를 함께 보낼 때 유용하게 사용됨
- 업데이트 되어야하는 데이터베이스의 레코드를 저장하거나, 고유한 보안 토큰 등을 서버로 보낼 때 주소 사용

## POST/GET
- get
  - 서버에서 어떤 데이터를 가져와서 보여줄때 사용
  - 클라이언트에서 서버로 어떤 리소스로부터 정보를 요청하기 위해 사용되는 method
  - 읽기, 검색에 사용
  - 요청을 전송할 때 url 주소 끝에 파라미터로 포함되어 전송(쿼리스트링)
- post
  - 서버상의 데이터 값이나 상태를 바꾸기 위해서 사용
  - 리소스를 생성/업데이트하기 위해 서버에 데이터를 보내는 데 사용
  - get과 달리 전송할 데이터를 http메시지의 body에 담아서 전송  
|                  | get         | post         |
|------------------|-------------|--------------|
| 캐시             | ⭕           | ❌            |
| 브라우저 기록    | ⭕           | ❌            |
| 북마크 추가      | ⭕           | ❌            |
| 데이터 길이 제한 | ⭕           | ❌            |
| HTTP 응답 코드   | 200(ok)     | 201(created) |
| 용도             | 리소스 요청 | 리소스 생성  |
| 전달 방식        | 쿼리 스트링 | HTTP body    |

## :not()선택자
- 이미 지정된 css 스타일에서 특정한 요소를 제외시킬 경우 사용
- 선택할 요소:not(제외시킬 요소)의 형태로 사용
  ```css
  input:not([type="radio"]):not([type="checkbox"]) {
      display: block;
      margin-bottom: 2rem;
      padding: 0 1rem;
      border-radius: 10px;
      border: none;
  }
  ```

## 속성 선택자
- []안에 스타일을 적용하려는 속성을 지정
- [속성 = 값]: 일치하는 요소에 적용
   ```css
  [for="name"]{
    padding: 0 1rem;
  }
  ```
- [속성 ~= 값]: 하나만 일치해도 적용  
  [class~="button"]일때 class="flat button"같은 경우에도 적용됨
- [속성 ^= 값]: 지정한 문자로 시작하는 속성에 적용
  ```css
  /*href 속성 값이 http://로 시작하면 폰트 크기가 2rem*/
  a [href^="http://"]{
    font-size: 2rem;
  }
  ```
- [속성 $= 값]: 지정한 문자로 끝나는 속성에 적용
  ```css
  /*압축파일이면 폰트 크기 2rem*/
  a [href$=".zip"]{
    font-size: 2rem;
  }
  ```
- [속성 |= 값]: 지정한 값으로 시작하면 적용
  ```css
  /*a태그 중 class 이름이 red로 시작하는 모든 요소의 폰트 사이즈 2rem*/
  a [class|="red"]{
    font-size: 2rem;
  }
  ```
- [속성 *= 값]: 위치와 상관없이 해당 값이 포함되어 있으면 적용
  ```css
  /*p태그 중 class 이름에 bigger이 들어가 있으면 폰트 사이즈 2rem*/
  p [class*="bigger"]{
    font-size: 2rem;
  }
  ```