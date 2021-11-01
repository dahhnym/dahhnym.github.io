---
layout: post
title: HTML 시맨틱 태그(Semantic Tag) - 텍스트 콘텐츠
author: Tina
date: 2021-11-01
tags: htmlElement html
categories: [content]
--- 

## 텍스트 콘텐츠
`body` 태그 내에 있는 콘텐츠를 블록 혹은 섹션 단위로 나눠 정리할 수 있다. 웹 접근성과 SEO를 고려하여 목적에 맞는 태그를 적절하게 사용할 필요가 있다.

### `<br>`
줄바꿈 태그.
#### `<wbr>`
텍스트 박스 내의 텍스트가 한줄로 표시되지 않을때 강제 줄바꿈하게 해준다.

### `<hr>`
단락 구별 시 사용하는 태그. 구분선을 표시해준다

### `<a>`
`a(anchor)` 태그는 링크를 설정할 때 사용한다.
{% highlight markdown %}
<!-- 절대경로 -->
<a href="https://www.naver.com">naver</a>

<!-- 새창 띄워서 링크 이동 -->
<a href="https://www.naver.com" target="_blank">naver 새창열기</a>

<!-- 상대경로-->
<a href="./index.html">상대경로</a>  <!-- ./ 는 현재경로이고 ../ 는 상위폴더-->

<!-- 페이지 내 해당 id를 갖고 있는 요소 부분으로 스크롤 이동-->
<a href="#three">페이지 내 해당 id로 이동</a>

<!-- href 경로에 적혀있는 html 파일 다운로드 -->
<a href="./index.html" download>html파일 다운로드</a>

<p id="one">id가 one인 문단입니다. Lorem ipsum dolor sit amet consectetur <mark>adipisicing</mark> elit. Deserunt deleniti, <i>debitis</i> suscipit impedit <em>eaque</em> necessitatibus aliquid asperiores aperiam fugiat quisquam dolorum nihil totam, distinctio cumque harum dolorem aut perferendis molestias?</p>
<p id="two">id가 two인 문단입니다.Optio molestiae nihil accusantium necessitatibus, deleniti, mollitia placeat eum minima rem voluptas fugit suscipit vel cupiditate veritatis, illo sapiente at. Earum quis consequatur vero voluptate maiores debitis, quisquam quasi voluptas.</p>
<p id="three">id가 three인 문단입니다. Impedit quibusdam voluptas nesciunt vitae cumque saepe quae nam eum officiis perferendis ullam accusantium cupiditate nobis quia nulla rem fugiat enim exercitationem reprehenderit molestias molestiae, ad optio quos? Sequi, ipsa!</p>

{% endhighlight %}

▶️ 코드 실행 결과<br>
<a href="https://www.naver.com">naver</a><br>
<a href="https://www.naver.com" target="_blank">naver 새창열기</a><br>
<a href="#three">페이지 내 해당 id로 이동</a><br>

<p id="one">id가 one인 문단입니다. Lorem ipsum dolor sit amet consectetur <mark>adipisicing</mark> elit. Deserunt deleniti, <i>debitis</i> suscipit impedit <em>eaque</em> necessitatibus aliquid asperiores aperiam fugiat quisquam dolorum nihil totam, distinctio cumque harum dolorem aut perferendis molestias?</p>
<p id="two">id가 two인 문단입니다.Optio molestiae nihil accusantium necessitatibus, deleniti, mollitia placeat eum minima rem voluptas fugit suscipit vel cupiditate veritatis, illo sapiente at. Earum quis consequatur vero voluptate maiores debitis, quisquam quasi voluptas.</p>
<p id="three">id가 three인 문단입니다. Impedit quibusdam voluptas nesciunt vitae cumque saepe quae nam eum officiis perferendis ullam accusantium cupiditate nobis quia nulla rem fugiat enim exercitationem reprehenderit molestias molestiae, ad optio quos? Sequi, ipsa!</p>

### `<b>`, `<strong>`
&lt;b&gt; 태그는 굵은 글꼴 표현할 때 사용. &lt;strong&gt; 태그는 굵은 글씨와 더불어 텍스트에 중요도를 더해준다.
예를 들어 페이지를 스크린 리더기가 읽어주는 경우 &lt;strong&gt; 태그가 있는 부분은 강조해서 읽어준다.
{% highlight markdown %}
<p> <b>To be</b>, or <b>not to be</b>: <strong>that</strong> is the question.</p>
{% endhighlight %}
<br>
▶️ 코드 실행 결과<br>
<b>To be</b>, or <b>not to be</b>: <strong>that</strong> is the question.
<br><br>
### `<i>`, `<em>`
&lt;i&gt; 태그는 텍스트를 기울임 글꼴로 표시한다. 문단에서 다른 언어나 필체로 표기되어 있는 부분 등을 표현할 때 사용한다.&lt;em&gt; 태그는 기울임 글꼴 표시와 함께 강조의 의미도 부여한다.
{% highlight markdown %}
<p>
  <i>Life</i>’s but a walking shadow, a poor player, that struts and frets his hour upon the stage, and then is heard no more; it is a tale told by an idiot, full of sound and fury, signifying <em>nothing</em>.
</p>
{% endhighlight %}
<br>
▶️ 코드 실행 결과<br>
<i>Life</i>’s but a walking shadow, a poor player, that struts and frets his hour upon the stage, and then is heard no more; it is a tale told by an idiot, full of sound and fury, signifying <em>nothing</em>.
<br><br>

### `<mark>`
텍스트에 하이라이트 표시를 해준다.
{% highlight markdown %}
<p>Love looks not with the eyes, but <mark>with the mind</mark>; and therefore is winged Cupid painted blind.</p>
{% endhighlight %}
<br>
▶️ 코드 실행 결과<br>
<p>Love looks not with the eyes, but <mark>with the mind</mark>; and therefore is winged Cupid painted blind.</p>
<br><br>

### `<abbr>`
abbr(abbreviation) 태그는 준말, 약자를 나타낼 때 사용한다. 해당 요소의 텍스트에 마우스오버를 하면 풀네임이 표시된다.
{% highlight markdown %}
<p>
  <abbr title="Korea Internet & Security Agency">KISA</abbr>는 대한민국의 인터넷 진흥, 인터넷 정보보호 및 그에 대한 국제 협력 업무를 수행하는 과학기술정보통신부 산하 위탁집행형 준정부기관이다.
  - 위키백과
</p>
{% endhighlight %}
<br>
▶️ 코드 실행 결과<br>
<p>
  <abbr title="Korea Internet & Security Agency">KISA</abbr>는 대한민국의 인터넷 진흥, 인터넷 정보보호 및 그에 대한 국제 협력 업무를 수행하는 과학기술정보통신부 산하 위탁집행형 준정부기관이다.
  - 위키백과
</p>
<br><br>
### `<sup>`, `<sub>`
&lt;sup&gt; 태그는 윗첨자, &lt;sub&gt; 태그는 아랫첨자를 나타낸다. 화학기호나 수학공식 등의 첨자 기호를 나타낼 때 사용한다.
{% highlight markdown %}
<p>H<sub>2</sub>0</p>
<p>x<sup>2</sup>=4</p>
{% endhighlight %}
▶️ 코드 실행 결과<br>
<p>H<sub>2</sub>0</p>
<p>x<sup>2</sup>=4</p>
<br>
<br>
참고자료: [HTML elements reference](https://developer.mozilla.org/ko/docs/Web/HTML/Element)
