---
layout: post
title: "styled component와 css module"
date: 2022-06-27 23:50:30 +0900
categories: JavaScript
---

react에서 css를 동적으로 적용하기 위한 방법들 중 styled component와 css module을 강의에서 소개함

## styled component

- 라이브러리(npm으로 설치해야함)
- css를 포함한 컴포넌트를 생성할 수 있음
- props를 참조할 수 있으며 props의 값에 따라 동적인 코딩 가능

  ```js
  const Button = styled.button`
    width: 100%;
    font: inherit;
    padding: 0.5rem 1.5rem;

    &:focus {
      outline: none;
    }
  `;
  ```

## css module

- 따로 설치 필요 없음
- 클래스명이 충돌하는 단점을 극복할 수 있음
- 컴포넌트 단위로 스타일을 적용할 때 유용
- 클래스명.module.css 파일을 만들어서 일반적인 css 코드를 작성하고 css를 적용할 파일에서 import해줌
- 적용할 클래스명이 여러개면 ``(백틱)으로 감싸줌
  ```js
  import styles from './Button.module.css'
  ...
  <div className={styles.buttonColor}>
    click this button
  </div>
  <div className={`${styles.buttonColor} ${styles.fontColor}`}>
    이 버튼을 클릭하세요
  </div>
  ```
