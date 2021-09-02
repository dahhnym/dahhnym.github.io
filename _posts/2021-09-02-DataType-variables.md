---
layout: post
title: 자료형과 변수
author: Tina
date: 2021-09-02
tags: JavaScript BasicSyntax
categories: [content]
---

## 자료형

자료의 종류를 의미한다 자바스크립트의 자료형에는 **문자열 자료형**, **숫자 자료형**, **불린 자료형** 등이 있다

### 문자 선택 연산자

문자열 내부의 문자 하나를 선택할때 쓰인다

문자열 다음에 인덱스값을 쓰면 해당 인덱스의 문자열 하나만 선택할 수 있다

```jsx
> '안녕하세요'[0]
"안"
> '안녕하세요'[3]
"세"
```

### 문자열 길이 구하기

`.length` 를 사용한다

```jsx
> "안녕하세요".length
5
> "자바스크립트".length
6
> "".length
0   // 빈 문자열도 문자열이다
```

### 문자열 자료형 비교

```jsx
> '가방' > '하마'
false
```

문자열 자료형은 *사전의 앞쪽에 있을수록 값이 작다*. 따라서 위의 예시의 표현식에서 '가방'은 '하마'보다 사전의 앞쪽에 나오므로 false이다.

## 연산자

`!` : 논리 부정 연산자

`&&` 논리곱 연산자

`||` 논리합 연산자

### 단항 연산자, 이항 연산자, 삼항 연산자

피연산자의 개수에 따른 연산자 구분 

```jsx
> !true   // 피연산자가 true 1개임으로 단항 연산자
false
> 10 + 20  // 피연산자가 10과 20으로 2개이므로 이항 연산자
30
> true ? 10 : 20   // 피연산자가 true, 10, 20으로 3개이므로 삼항 연산자
10
```

### 복합대입연산자

`+=`, `-=`, `*=` , `/=` 

### `typeof` 연산자

피연산자를 1개만 갖는 단항 연산자

```jsx
>typeof('문자열')
"string"
> typeof(273)
"number"
> typeof true  // 연산자 뒤에 괄호 생략해도 됨
"boolean"

>typeof 10 === 'number'   // typeof 연산자 활용. 비교 연산자와 함께 쓰여 자료형 확인하는 경우가 많다
true
```

## 템플릿 문자열

문자열 내부에 `${...}` 기호를 사용하여 표현식을 넣으면 표현식이 문자열 안에서 계산된다

```jsx
>console.log(`표현식 273 + 52의 값은 ${273 + 52}입니다...!`)
표현식 273 + 52의 값은 325입니다...!
```

### `==`연산자와 `!=` 연산자

`===`와 `!==` 연산자는 값과 자료형이 같은지 비교하는 것이지만 `==`와 `!=` 연산자는 값이 같은지만 비교한다 정확한 비교를 위해서 `===`와 `!==` 연산자를 사용하는것을 권장

```jsx
> "" == []    // 빈 문자열은 false, 비어있는 배열 []은 false로 변환된 뒤 비교한다
true
> 0 == []   // 0 은 false, 빈 배열[]은 false로 변환된 뒤 비교한다
true
```


## 상수

항상 같은 수. 수식에서 변하지 않는 값. 한번 정의하면 변하지 않는 값.

한번 선언하면 같은 이름으로 또 상수를 선언할 수 없다.

```jsx
// 상수 선언
const myPhone = 'iphone';

const myPhone = 'galaxy';   // Uncaught SyntaxError: Identifier 'myPhone' has already been declared
```

상수는 한번만 선언할 수 있으므로 반드시 초기화를 동시해 줘야한다

```jsx
const name;   // Uncaught SyntaxError: Missing initializer in const declaration

const name = 'Tina';
```

상수값을 변경할 수 없다.

```jsx
const name = 'Tina';

name = 'Chris';   // TypeError: Assignment to constant variable.
```

## 변수

변수는 한번 선언 후 추후에 값을 변경할 수 있다.

```jsx
let myPhone = 'iphone';
myPhone = 'galaxy';    // 변수값 변경
```

`let`을 사용하여 변수를 선언한 경우 똑같은 이름으로 또 변수 선언을 할 수 없다.

```jsx
let name = 'name이라는 변수 선언합니다.';
let name = '다시 한번 선언해봅니다.';  // Uncaught SyntaxError: Identifier 'name' has already been declared
```

### `prompt()` 함수

사용자로부터 글자를 입력받을 때 사용한다

```jsx
// 상수를 선언합니다.
const input = prompt('message', '_default');

// 출력합니다.
alert(input);
```

> 실행결과

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ea5f3bd8-e036-4d12-99cd-669d5b6cea76/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/39e0533d-e376-46fb-96e7-fbe51c5817a4/Untitled.png)

입력창에 '안녕하세요'를 입력하고 OK를 누르면 입력한 '안녕하세요'를 리턴하고 상수 input에 이 값을 할당한다

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/01fcf291-9252-43a8-b797-91f96746a2cc/Untitled.png)

input값을 alert창으로 출력한다

## 불린 입력

### `confirm()` 함수

```jsx
// 상수를 선언합니다.
const input = confirm('수락하시겠습니까?')

// 출력합니다.
alert(input)
```

> 실행결과

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/eda2dea6-5622-43e5-b676-a769b0631236/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0f280fa3-6fb2-4224-801d-dc0bf32c4591/Untitled.png)

OK 클릭시 - true를 리턴하고 상수 input에 이 리턴값이 할당됨

## 숫자 자료형으로 변환하기

### `Number()` 함수

숫자가 적혀 있는 문자열을 숫자로 변환한다

```jsx
Number("273");   // 273
typeof(Number("273"));  // "number"
```

### `NaN`

Not a Number. 다른 문자가 들어 있어서 숫자로 변환할 수 없는 문자열의 경우 NaN가 출력된다
자바스크립트에서 NaN은 숫자이지만 숫자로 나타낼 수 없는 숫자를 뜻한다

```jsx
Number("$273");   // NaN
// 값은 숫자로 나타낼 수 없지만
typeof(Number("$273"));  // "number"
// 자료형은 숫자 자료형이다
```

불린의 경우  true는 1, false는 0이다

```jsx
Number(true);  // 1
Number(false);  // 0
```

산술연산자 `-`,  `*`, `/`를 사용하면 자동으로 숫자 자료형으로 변환되어 계산된다(`+` 는 해당되지 않으므로 주의!)

```jsx
5 - "5"; // 0
typeof(5-"5");  // "number"
```

## 문자열 자료형으로 변환하기

### `string()` 함수

```jsx
String(52.273);  // "52.273"
String(true);    // "true"
```

산술연산자 `+`를 사용하면 자동으로 문자 자료형으로 변환된다

```jsx
273 + "";   // "273"
true + "";  // "true"
5+"5";      // "55"
```

## 불린 자료형으로 변환하기

### `Boolean()` 함수

대부분의 자료는 불린으로 변환했을 때 true 값이 나온다 예외로는 0, NaN, 빈 문자열, null, undefined 이 5개의 자료형은 false로 변환된다

```jsx
Boolean(0);    // false
Boolean(NaN);  // false
Boolean("");   // false
Boolean(null); // false

let 변수;  // undefined
Boolean(변수);  // false
```

### 논리 부정 연산자 `!` 를 사용해 자료형 변환하기

논리부정연산자 `!`를 두번 사용하면 불린으로 변환된다

```jsx
!!273;  // true
!!0;    // false
!!'안녕하세요'  // true
!!''  // false
```
