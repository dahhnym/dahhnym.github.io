---
layout: post
title: 조건문
author: Tina
date: 2021-09-03
tags: JavaScript BasicSyntax
categories: [content]
---


## switch 조건문

값에 따라서 조건 분기를 걸어주는 조건문

## 조건부 연산자

`삼항 연산자` 라고도 하며 피연산자 3개를 갖는 연산자 

`조건문 표현식?참일 때 리턴값:거짓일때 리턴값`

## 짧은 조건문

논리 연산자의 특이한 성질을 사용해어 조건 분기에 활용하는 코드

### if 조건문을 switch 조건문으로 변환하기

```jsx
const date = new Date();
const hour = date.getHours();

// 조건문
if(hour < 11){
		alert('아침 먹을 시간입니다.');
} else if (hour < 15){
		alert('점심 먹을 시간입니다.');
} else{
		alert('저녁 먹을 시간입니다.');
}

// switch문으로 바꾸기
switch (true){
	case hour < 11:
		alert('아침 먹을 시간입니다');
		break;
	case hour < 15:
		alert('점심 먹을 시간입니다.');
		break;
	default:
		alert('저녁 먹을 시간입니다.');
		break;
}
```

## 짧은 조건문

### 논리합 연산자 사용했을때

`불린 표현식 || 불린 표현식이 거짓일 때 실행할 문장`

```jsx
true || console.log('실행될까요?');   // 좌변이 참이므로 우변이 실행되지 않음
false || console.log('실행될까요?');  // 실행될까요?
																		 // 좌변이 거짓이므로 우변이 실행됨
```

### 논리곱 연산자 사용했을때

`결과가 거짓인 불린 표현식 && 불린 표현식이 참일 때 실행할 문장`
