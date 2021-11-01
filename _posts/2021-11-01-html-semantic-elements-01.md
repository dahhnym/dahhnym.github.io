---
layout: post
title: HTML 시맨틱 태그(Semantic Tag) - 콘텐츠 구획
author: Tina
date: 2021-11-01
tags: htmlElement html
categories: [content]
--- 

## 콘텐츠 구획 요소
문서 내 콘텐츠를 논리적 블록으로 만들어 구획을 나누어 준다

### `<main>`
문서의 주요 콘텐츠를 나타낸다. 즉, 해당 문서의 핵심 주제, 혹은 앱의 핵심 기능들과 직접 연결되어 있거나 확장되는 콘텐츠로 구성되어야 하며,  문서 전반에 걸쳐 반복되는 내용을 포함해서는 안 된다. main 요소가 사이트의 메인 컨텐츠를 모두 담고 있어야하며 header, nav 등의 다른 요소의 자식 요소가 되어서는 안된다. IE에서는 지원하지 않는 태그이므로 사용에 주의 필요.
<br><br>
![main tag usage example - uber](https://user-images.githubusercontent.com/74545780/139697271-a97fcfa5-14eb-4021-b12b-8bb8212c74bf.png "main-tag-usage-exmaple-uber")
_main 태그 내에 메인 컨텐츠를 담고 있는 예시_우버 홈페이지_

### `<h1>~<h6>`
6단계의 구획 제목을 나타낸다. `<h1>`이 가장 높고 `<h6>`이 가장 낮다.
주의할 점은, 글씨 크기를 크게 표시하기 위해서 사용하면 안된다. 가급적 단계를 h1, h2, h3 이런 식으로 순차적으로 사용할 것. 건너뛰는 것은 피하도록 한다. 
페이지 당 하나의 `<h1>`만 사용해야 한다. `<h1>`는 해당 전체 페이지의 목적을 간략하게 설명하는 역할을 한다.

### `<section>`
문서 내의 독립적인 구획 나타내며 한 사이트 내의 연관 콘텐츠를 나타낼 때 사용된다. 여러 개의 섹션을 사용하는 경우 제목을 포함시켜 식별해야 한다.

### `<article>`
페이지 내에서 독립적으로 구분해 배포하거나 재사용할 수 있는 구획을 나타낸다. 게시판, 블로그 글, 뉴스 기사 등을 예로 들 수 있다.
{% highlight markdown %}
<!-- 예시 코드 01 -->
<section>
  <h1>오늘의 뉴스</h1>
  <article>
    <header>기사제목1</header>
    기사내용
  </article>
  <article>
    <header>기사제목2</header>
    기사내용
  </article>
</section>
<section>
  <h1>오늘의 날씨</h1>
  <article>
    <header>2021.10.31 날씨</header>
    맑아요
  </article>
  <article>
    <header>2021.11.01 날씨</header>
    추워요
  </article>
</section>
{% endhighlight %}
<br>
![section-article](https://user-images.githubusercontent.com/74545780/139701059-23372f8e-3091-4162-80e4-702c1ac0466c.png)
_예시 코드 01 실행 결과 화면_

### `<nav>`
nav(navigation) 요소는 주로 메뉴에 사용된다
{% highlight markdown %}
<nav>
  <ul>
    <li><a href="#">home</a></li>
    <li><a href="#">about</a></li>
    <li><a href="#">FAQ</a></li>
  </ul>
</nav>
{% endhighlight %}
<br>
### `<aside>`
별도 구획 요소로 문서의 주요 내용과 간접적으로 연관된 내용을 나타낸다. 주로 사이드바나 광고 영역 등에 활용된다.

#### aside 태그 활용 예시 코드
{% highlight markdown %}
<!-- 예시 코드 02 -->
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>semantic tag</title>
    <style>
      body {
        padding: 10px;
        margin: 0;
      }
      p.main-para{
        width: 60%;
        float:left;
        border: solid 1px blue;
        margin: 0;
      }
      aside{
        float: right;
        width: 35%;
        border: solid 1px rosybrown;
      }
      aside > img{
        padding: 15px;
        width: 85%;
      }
    </style>
</head>
<body>
  <p class="main-para-1">
  소리다.이것은 피부가 꽃이 날카로우나 길을 맺어, 자신과 그것은 있는 철환하였는가? 사랑의 같은 인간의 날카로우나 아름다우냐? 이상의 우리 사랑의 못할 인간에 있으랴? 현저하게 있으며, 황금시대를 것은 뜨고, 고행을 산야에 옷을 피에 것이다.      
  낙원을 하는 것이 밥을 바이며, 피가 얼마나 같이, 생의 철환하였는가? 찾아다녀도, 피가 피부가 것이다. 무엇을 보내는 옷을 보이는 피부가 이는 사막이다. 놀이 고동을 기관과 생명을 이상의 사막이다.</p>
  <aside>
  <b>&lt;aside&gt;</b>
  <p>천고에 피에 예가 봄바람이다. 창공에 청춘 우리의 기쁘며, 모래뿐일 뛰노는 너의 싶이 하여도 있으랴? 그들의 있는 노래하며 안고, 그들의 바이며, 봄날의 사람은 약동하다. 밝은 새 타오르고 우리 운다.</p>
  </aside>
  <p class="main-para-2">얼마나 가는 그것을 인간의 것은 곳으로 있는가? 발휘하기 가치를 것은 그들의 뼈 찾아 피부가 천자만홍이 있는 운다.
  구할 목숨을 풀밭에 얼음 길을 가치를 피에 뿐이다. 그들의 심장의 광야에서 심장은 그들은 지혜는 위하여서. 그들에게 풍부하게 하는 이 이것이다. 우리 날카로우나 피가 인류의 가진 설산에서 않는 우리 황금시대다. 심장은 우리 인생을 사랑의 인간이 청춘 않는 운다.</p>
</body>
</html>
{% endhighlight %}
<br>
![aside](https://user-images.githubusercontent.com/74545780/139708355-e1faf690-3d3c-4b93-8e39-34eb5257de9a.png)
_예시 코드 02 실행 결과 화면_
<br>
<br>
참고자료: [HTML elements reference](https://developer.mozilla.org/ko/docs/Web/HTML/Element)
