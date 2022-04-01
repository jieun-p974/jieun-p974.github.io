---
layout: post
title:  "CSS rem, selector, cascade"
date:   2022-03-30 21:27:00 +0900
categories: CSS bootcamp
---

## Bootcamp(´▽`ʃ♡ƪ)
인터넷에서 무료 [bootcamp][boot-camp] 코스가 있길래 요즘 듣는 중인데 기본적인 html, css, js를 가르쳐주는 코스다.  
영어로 진행한다고 해서 걱정했는데 생각보다 할만하다. 요즘 영어권 vlog를 많이 본 효과가 여기서...  

### em과 rem
- em 
	- 상대적인 단위
	- 상위 요소를 기준으로 하며 상위 요소 크기의 몇 배인지로 크기를 지정하는 단위
	- 상위 요소에 따라 같은 1em이라도 크기가 들쭉날쭉할 수 있음
- rem
	- root + em
	- 상대적인 단위
	- 루트 요소인 html을 기준으로 하기 때문에 한 문서 안에서 1rem은 모두 같은 사이즈
	- 상위 요소가 영향을 끼치지 않음

### selector
- class
  - 태그 별로 스타일을 지정할 수도 있지만 같은 태그 내에서도 예외를 두고 싶을 때 사용
  - html 태그에서는 class="클래스명"으로 지정
  - css에서 해당 클래스를 지정할 때는 .클래스명
	```html
	<h1 class="bigbold">
	```
	```css
	.bigbold{
		font-size: 1.5rem;
	}
	```
- grouped selector
  - 여러가지 요소를 한번에 묶어서 스타일을 적용할 수 있다
	```css
		h2, h3, .bigbold, a:link {
			color: orange;
		}
	```	
  - a:link는 a태그 중 방문한 적 없는 요소
  - a:visited는 a태그 중 방문한 적 있는 요소
  - a:hover는 a태그위에 마우스가 올라갔을 때
- descendant selector
  - 한국어로 번역하면 자손 선택자
  - 공백을 사용해서 지정
  - ul a라고 적으면 ul태그 내의 a태그를 선택한다는 뜻
	```css
		ul a {
			font-weight: bold;
			/*밑줄 없음*/
			text-decoration: none; 
		}
	```

### cascade
- html element는 하나 이상의 스타일에 영향을 받을 수 있기 때문에 어떤 스타일을 적용 받을지에 대해 우선순위가 필요
- css가 어디에서 선언되었는지, 대상을 명확하게 지정했는지, 코드 순서에 따라 우선순위가 결정됨
- html문서에서 style을 선언할 수도 있는데 이 경우를 embedded style이라고 부름
- 중요도는 embedded style > link로 연결된 CSS파일 > 브라우저의 기본 CSS
- embedded style안에서도 늦게 선언된 스타일이 우선도가 높음
- 아래의 경우 적용되는 색은 purple!
	```html
	<style>
		p {color: pink;}
		p {color: purple;}
	</style>
	<div>
		<p>Hi!!!!</p>
	</div>
	```

[boot-camp]: https://frontendmasters.com/dashboard
