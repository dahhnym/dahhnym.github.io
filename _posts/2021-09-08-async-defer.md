---
layout: post
title: async와 defer
author: Tina
date: 2021-09-08
tags: JavaScript
categories: [content]
---

기본적으로 브라우저는 HTML 파싱을 하다가 &lt;script&gt;를 만나면 HTML 파싱을 중단하고 스크립트 리소스를 다운로드, 파싱, 실행한다 이럴 경우 화면을 렌더링하는데 그만큼 시간이 소모되므로 사용성이 떨어진다

&nbsp;
![default-parse-graph](https://user-images.githubusercontent.com/74545780/132536510-815f7a68-508a-40c1-8be9-51e9e33ee0de.png)


&nbsp;

### `async` 를 사용했을 때 

![async-parse-graph](https://user-images.githubusercontent.com/74545780/132536705-38c3675a-ff3d-4107-82ba-e420e850185a.png)

&nbsp;
HTML 파싱을 계속하다가 &lt;script&gt;를 만나면 스크립트 리소스를 다운로드하되 파싱을 중단하지 않는다 다운로드가 완료되면 파싱을 중단하고 스크립트를 실행한다

### 특징

스크립트의 실행 순서는 다운로드가 완료된 시점에 결정된다

```jsx
<script src="a.js" async>
<script src="b.js" async>
<script src="c.js" async>
```

위의 코드처럼 `a.js` `b.js` `c.js` 순서로 정의했어도 다운로드하는데 걸린시간이 다음과 같다면

 `a.js` : 3초<br>
 `b.js` : 1초<br>
 `c.js` : 2초<br>

 `b.js`  `c.js`  `a.js` 순으로 실행이 된다

정의한 순서대로 스크립트 실행되기를 보장하기 위해 HTML5에서 `async=false` 가 추가되었다 기본값은  `async=true` 이다

### `defer` 를 사용했을 때
 
![defer-parse-graph](https://user-images.githubusercontent.com/74545780/132536753-7daebffa-1325-4390-a3bb-81cbf4ad9626.png)

&nbsp;
HTML파싱하는 동안 &lt;script&gt;를 만나면 파싱 중단없이 스크립트 리소스를 다운로드하고 HTML 파싱이 완료되면 스크립트가 실행이 된다

정의된 순서대로 스크립트가 실행된다

## 어떤 속성을 사용할 것인가

&lt;body&gt; 태그가 닫히기 직전 &lt;script&gt; 태그를 선언한다면 이미 거의 모든 HTML 파싱이 종료된 상태이므로 async 속성이든 defer 속성이든 큰 의미가 없다
하지만 그렇게 하지 않은 경우에는 어떤 속성을 사용하는 것이 좋을까
  
### `async`를 사용해야 할 때

- 스크립트 파일에 종속성이 없는 경우
- DOM에 종속성이 없어서 HTML 파싱 중 어느 시점에 스크립트가 실행되든 상관없는 경우
- `async=true`인 경우, 스크립트 리소스 다운로드가 완료된 순서대로 스크립트가 실행되므로, 여러 스크립트가 정의된 경우 스크립트 파일 간 종속성이 없어서 어떤 스크립트가 먼저 실행되도상관없는 경우

### `defer`를 사용해야 할 때

- DOM과 종속성이 있어서, DOM이 전부 생성되어야 정상적인 동작을 할 수 있는 경우
- 스크립트 간 종속성이 있어서 정의된 순서대로 스크립트가 실행되어야 되는 경우
<br>
<br>
<br> 
[참고자료 https://beomy.github.io/tech/browser/async-defer/] (https://beomy.github.io/tech/browser/async-defer/)
