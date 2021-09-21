# prepare_frontend_interview

## JavaScript

<b>프론트엔드 기술 면접을 위한 핸드북 만들기</b>

면접의 인터뷰어 분들이 JS의 수 많은 개념들을 순서대로 질문을 하지는 않습니다.

하지만 자바스크립트의 연관되어 있는 개념들을 순서대로 나열하고 핸드북 형식으로 보다 보면,

모르는 개념을 파악하고 한눈에 보는 것에 있어서 도움이 되지 않을까 싶어 제작하게 되었습니다.

목차는 모던 자바스크립트 deep dive를 기준으로 제작하였고 자세한 정리 내용은

[링크](https://github.com/junh0328/upgrade_javascript) 클릭 시에 해당 레포지토리에서 볼 수 있습니다.

질문에 대한 3-5줄 정도의 짧은 길이로 핵심 키워드를 체크하고 헷갈리는 용어들을 반복적으로 보게 됨으로써, 핵심 키워드를 기억할 수 있도록 만드는 것이 목표입니다!

## 목차

- [프로그래밍 🔥](#프로그래밍)

  - 프로그래밍이란 뭐라고 생각하나요?
  - 컴파일러는 뭐고 인터프리터는 뭔가요?

- [자바스크립트란 🔥](#자바스크립트란)

  - 자바스크립트의 특징은 뭐가 있나요?

- [변수 🔥](#변수)

  - 변수란 무엇인가요?
  - 식별자란 무엇인가요?
  - 변수를 선언한다는 것은 어떤 것을 의미하나요?
  - var 키워드는 뭔가요?
  - 호이스팅이 뭔가요?
  - var 키워드의 문제점은 무엇이 있나요?
  - let 키워드는 var 키워드와 어떤 점이 다른가요?
  - TDZ가 뭔가요?
  - const 키워드는 어떤 특징이 있나요?
  - 식별자 네이밍 규칙은 어떤 것들이 있나요?
  - 네이밍 컨벤션은 어떤 것들이 있나요?
  - 리터럴이 뭔가요?

- [데이터 타입 🔥](#데이터-타입)

  - 데이터 타입의 종류는 어떤 것들이 있나요?
  - 심벌 타입은 뭐죠?
  - 데이터 타입은 왜 필요할까요?
  - 정적 타이핑이 뭔가요?
  - 동적 타이핑이 뭔가요?

- [타입변환과 단축 평가 🔥](#타입변환과-단축-평가)

  - 명시적 타입 변환이 뭔가요?
  - 명시적 타입 변환 함수를 예를 들어볼 수 있나요?
  - 암묵적 타입 변환이 뭔가요?
  - truthy / falsy 한 값이 뭔가요?

- [객체 리터럴 🔥](#객체-리터럴)

  - 자바스크립트에서 객체란 뭘까요?
  - 함수와 메서드의 차이점에 대해 알고 계신가요?
  - 자바스크립트에서 객체를 생성하는 방법은 어떤 것들이 있나요?

- [원시 값과 객체 비교 🔥](#원시-값과-객체-비교)

  - 동적 타이핑을 지원하는 자바스크립트에서 데이터의 타입을 크게 2개로 나누는 이유가 있을까요?
  - 값에 의한 전달이 뭔가요?
  - 참조에 의한 전달이 뭔가요?

- [함수 🔥](#함수)

  - 자바스크립트에서 함수를 정의하는 방법은 몇가지가 있나요?
  - 함수 선언문과 함수 표현식은 어떤 차이가 있나요?
  - 즉시 실행 함수(IIFE)에 대해 알고 있나요? 알고 있다면 아는 내용에 대해 말해보세요

- [스코프 🔥](#스코프)

  - 스코프가 뭔가요?
  - 스코프에는 어떤 종류가 있죠?
  - 렉시컬 스코프를 아나요? 안다면 렉시컬 스코프는 무엇을 의미하나요?
  - 전역 변수로 변수를 선언하면 생기는 문제점은 무엇이 있을까요?

- 생성자 함수에 의한 객체 생성
- 함수와 일급 객체
- 프로토타입
- strict mode
- 빌트인 객체
- this
- 실행 컨텍스트
- 클로저
- 클래스
- ES6 함수의 추가 기능
- 배열
- Number
- Math
- Date
- RegExp
- String
- Symbol
- 이터러블
- 스프레드(...) 문법
- 디스트럭처링 할당(구조 분해 할당)
- 브라우저 렌더링 과정
- DOM
- 이벤트
- 타이머
- 비동기 프로그래밍
- Ajax
- REST API
- Promise
- 제너레이터와 async/await
- 에러처리
- 모듈

## 프로그래밍

### 프로그래밍이란 뭐라고 생각하나요?

프로그래밍이란 컴퓨터에게 실행을 요구하는 일종의 커뮤니케이션이다.해결해야 할 문제(요구사항)를 명확히 이해한 후 적절한 문제 해결 방안을 정의할 필요가 있다.0과 1밖에 알지 못하는 기계가 실행할 수 있을 정도로 정확하고 상세하게 요구를 설명하는 작업이며, 그 결과물이 바로 코드다.

<br/>

### 컴파일러는 뭐고 인터프리터는 뭔가요?

우리가 코드를 통해 내린 명령을 수행할 주체는 컴퓨터이다. 따라서 사람이 이해할 수 있는 자연어가 아니라 컴퓨터가 이해할 수 있는 언어, 즉 기계어로 명령을 전달해야 한다.

기계어는 우리가 사용하는 언어와는 너무나도 체계가 다르기 때문에 사람이 기계어로 직접 명령을 전달하는 것은 매우 어렵다. 기계어로 직접 명령을 전달하는 것을 대신할 가장 유용한 대안은 사람이 애해할 수 있는 약속된 구문으로 구성된 프로그래밍 언어를 사용해 프로그램을 작성한 후, 그것을 컴퓨터가 이해할 수 있는 기계어로 변환하는 일종의 번역기를 이용하는 것이다.

이 일종의 번역기를 컴파일러(compiler) 혹은 인터프리터(interpreter)라고 한다.

```
compile:변환하다
interpret:해석하다
```

## 자바스크립트란

### 자바스크립트의 특징은 뭐가 있나요?

자바스크립트는 HTML, CSS와 함께 웹을 구성하는 요소 중 하나로 웹 브라우저에서 동작하는 유일한 프로그래밍 언어다.

자바스크립트는 개발자가 별도의 컴파일 작업을 수행하지 않는 **인터프리터 언어이다.** **인터프리터는 소스코드를 즉시 실행하고** **컴파일러는 빠르게 동작하는 머신 코드를 생성하고 최적화한다.** 이를 통해 컴파일 단계에서 추가적인 시간이 필요함에도 더욱 빠르게 코드를 실행할 수 있다.

자바스크립트는 **런타임에 컴파일되며 실행 파일이 생성되지 않고 인터프리터의 도움 없이 실행할 수 없기 때문에 컴파일러 언어라고 할 수는 없다.**

## 변수

### 변수란 무엇인가요?

변수는 하나의 값을 저장하기 위해 확보한 메모리 공간 자체 또는 그 메모리 공간을 식별하기 위해 붙인 이름을 말한다.

<br/>

### 식별자는 무엇인가요?

변수의 이름을 식별자(identifier)라고도 한다. 식별자는 어떤 값을 구별해서 식별할 수 있는 고유한 이름을 말한다. **식별자는 값이 아니라 메모리 주소를 기억하고 있다.**

또한 식별자라는 용어는 변수 이름에만 국한해서 사용하지 않는다. 예를 들어, 변수, 함수, 클래스 등의 이름은 모두 식별자다. 식별자인 변수 이름으로는 메모리 상에 존재하는 변수 값을 식별할 수 있고, 함수 이름으로는 메모리 상에 존재하는 함수를 식별할 수 있다. **즉, 메모리 상에 존재하는 어떤 값을 식별할 수 있는 이름은 모두 식별자라고 부른다.**

<br/>

### 변수를 선언한다는 것은 어떤 것을 의미하나요?

```js
var score;
```

변수 선언이란 **변수를 생성하는 것**을 말한다. 좀 더 자세히 말하면 **값을 저장하기 위한 메모리 공간을 확보하고 변수 이름과 확보된 메모리 공간의 주소를 연결해서 값을 저장할 수 있게 준비하는 것이다.** 변수를 사용하려면 반드시 선언이 필요하다. 변수를 선언할 때는 var, let, const 키워드를 사용한다.

<br/>

### var 키워드는 뭔가요?

var 키워드는 뒤에 오는 변수 이름을 새로운 변수를 선언할 것을 지시하는 키워드이다. 키워드는 자바스크립트 코드를 해석하고 실행하는 자바스크립트 엔진이 수행할 동작을 규정한 일종의 명령어이다. 자바스크립트 엔진은 키워드를 만나면 자신이 수행해야 할 약속된 동작을 수행한다. 예를 들어, var 키워드를 만나면 자바스크립트 엔진은 뒤에 오는 변수 이름으로 새로운 변수를 선언한다.

변수를 선언한 이후, 아직 변수에 값을 할당하지 않았다. 따라서 변수 선언에 의해 확보된 메모리 공간은 비어 있을 것으로 생각할 수 있으나 확보된 메모리 공간에는 자바스크립트 엔진에 의해 undefined라는 값이 암묵적으로 할당되어 초기화된다. 이것이 자바스크립트의 독특한 특징이다.

<br/>

### 호이스팅이 뭔가요?

```js
console.log(score); // undefined;

var score; // 변수 선언문
```

js 엔진은 변수 선언(을 포함한 모든 선언문)이 소스코드의 어디에 있든 상관없이 다른 코드보다 먼저 실행한다. 런타임 이전에 실행 컨텍스트에 의해 소스코드 평가 과정에서 스코프에 등록되고 이를 마치 코드의 제일 위에 있는 것처럼 변수가 어디에 위치하던지와 상관없이 어디서든지 변수를 참조할 수 있는 것처럼 만드는 특징을 변수 호이스팅이라고 합니다.

**사실 변수 선언뿐 아니라 var, let, const, function, function\*, class 키워드를 사용해서 선언하는 모든 식별자(변수, 함수, 클래스 등)는 호이스팅된다. 모든 선언문은 런타임 이전 단계에서 먼저 실행되기 때문이다.**

<br/>

### var 키워드의 문제점은 무엇이 있나요?

var 키워드로 선언된 변수는 다음과 같은 특징이 있다.

1. 변수 중복 선언 허용
2. 함수 레벨 스코프
3. 변수 호이스팅

<details>
<summary>① 변수 중복 선언 허용</summary>

var 키워드로 선언된 변수는 같은 스코프 내에서 중복 선언이 허용되는데, 이는 의도치 않게 변수값이 재할당되어 변경되는 부작용을 발생시킨다.

```js
function foo() {
  var x = 1;
  // var 키워드로 선언된 변수는 같은 스코프 내에서 중복 선언을 허용한다.
  // 아래 변수 선언문은 자바스크립트 엔진에 의해 var 키워드가 없는 것처럼 동작한다.
  var x = 2;
  console.log(x); // 2
}
foo();
```

</details>

<details>
<summary>② 함수 레벨 스코프</summary>

대부분의 프로그래밍 언어는 함수 몸체만이 아니라 모든 코드 블록(if, for, while, try/catch 등)이 지역 스코프를 만든다. 이러한 특성을 **블록 레벨 스코프**라 한다. 하지만 var 키워드로 선언된 변수는 오로지 함수의 코드 블록(함수 몸체)만을 지역 스코프로 인정한다. 이러한 특성을 **함수 레벨 스코프**라 한다.

```js
case 1 : var 키워드로 변수 선언

var x = 1;

if (true) {
  // var 키워드로 선언된 변수는 함수의 코드 블록(함수 몸체)만을 지역 스코프로 인정한다.
  // 함수 밖에서 var 키워드로 선언된 변수는 코드 블록 내에서 선언되었다 할지라도 모두 전역 변수다.
  // 따라서 x는 전역 변수다. 이미 선언된 전역 변수 x가 있으므로 x 변수는 중복 선언된다.
  // 이는 의도치 않게 변수 값이 변경되는 부작용을 발생시킨다.
  var x = 10;
}
console.log(x); // 10


case 2 : var 키워드로 for문 안의 변수 선언

var i = 10;

// for 문에서 선언한 i는 전역 변수다. 이미 선언된 전역 변수 i가 있으므로 중복 선언된다.
for (var i = 0; i < 5; i++) {
  console.log(i); // 0 1 2 3 4
}

// 의도치 않게 변수의 값이 변경되었다.
console.log(i); // 5
```

</details>

<details>
<summary>③ 변수 호이스팅</summary>

var 키워드로 선언된 변수는 선언과 동시에 undefined로 초기화되며, 런타임 즉 소스코드 평가 단계에서 스코프에 등록되기 때문에 실행 단계에서 실제 값이 할당되지 않더라도 undefined를 가지고있다. 이를 변수 호이스팅이라 한다.

```js
console.log(score); // undefined;

var score; // 변수 선언문
```

</details>

<br/>

### let 키워드는 var 키워드와 어떤 점이 다른가요?

let 키워드는 var 키워드의 단점을 보완하기 위해 ES6에서 도입된 새로운 키워드입니다.

```
1. 변수 중복 선언 금지
2. 블록 레벨 스코프
3. 변수 호이스팅
4. 전역 객체와 let
```

1. 변수 중복 선언 금지

var 키워드로 이름이 동일한 변수를 중복 선언하면 아무런 에러가 발생하지 않는다. 이때 변수를 중복 선언하면서 값까지 할당했다면 의도치 않게 먼저 선언된 변수 값이 재할당되어 변경되는 부작용이 발생한다. 하지만 let 키워드로 이름이 같은 변수를 중복 선언하면 문법 에러(SyntaxError)가 발생한다.

```js
let bar = 123;
// let이나 const 키워드로 선언된 변수는 같은 스코프 내에서 중복 선언을 허용하지 않는다.
let bar = 456; // SyntaxError: Identifier 'bar' has already been declared
```

2. 블록 레벨 스코프

let 키워드를 통해 선언된 변수는 블록 레벨 스코프를 따른다. 함수 뿐만 아니라 모든 코드 블록 내에 선언된 변수(지역 변수)는 해당 유효 범위(스코프)를 벗어나면 사용할 수 없다.

```js
let foo = 1; // 전역 변수

{
  let foo = 2; // 지역 변수
  let bar = 3; // 지역 변수
}

console.log(foo); // 1
console.log(bar); // ReferenceError: bar is not defined
```

3. 변수 호이스팅

var 키워드로 선언한 변수와 달리 let 키워드로 선언한 변수는 변수 호이스팅이 발생하지 않는 것처럼 동작한다.

```js
console.log(foo); // Cannot access 'foo' before initialization
let foo;
```

var 키워드였다면 변수 호이스팅에 의해 런타임 이전에 변수가 선언되어 undefined를 출력해야 한다. 하지만 let 키워드에서는 참조에러가 나타난다.

let 키워드로 선언한 변수는 '선언 단계'와 '초기화 단계'가 분리되어 진행된다. 즉, 런타임 이전에 자바스크립트 엔진에 의해 암묵적으로 선언 단계가 먼저 실행되지만 초기화 단계는 변수 선언문에 도달했을 때 실행된다. 만약 초기화 단계가 실행되기 이전에 변수에 접근하려고 하면 참조 에러가 발생한다.

let 키워드로 선언한 변수는 스코프의 시작 지점부터 초기화 단계 시작 지점(변수 선언문)까지 변수를 참조할 수 없다. 스코프의 시작 지점부터 초기화 시작 지점까지 변수를 참조할 수 없는 구간을 **일시적 사각지대(TDZ: Temporal Dead Zone)**라 부른다.

<img src="./images/15_3.jpg" alt="TDZ">

```js
// 런타임 이전에 선언 단계가 실행된다. 아직 변수가 초기화되지 않았다.
// 초기화 이전의 일시적 사각 지대에서는 변수를 참조할 수 없다.
console.log(foo); // ReferenceError: foo is not defined

let foo; // 변수 선언문에서 초기화 단계가 실행된다.
console.log(foo); // undefined

foo = 1; // 할당문에서 할당 단계가 실행된다.
console.log(foo); // 1
```

4. 전역 객체와 let

let 키워드로 선언한 전역 변수는 전역 객체의 프로퍼티가 아니다. 즉, window.foo와 같이 접근할 수 없다.

```js
let x = 1;

// let, const 키워드로 선언한 전역 변수는 전역 객체 window의 프로퍼티가 아니다.
console.log(window.x); // undefined
console.log(x); // 1
```

<br/>

### const 키워드는 어떤 특징이 있나요?

const 키워드는 상수(constant)를 선언하기 위해 사용하지만, 반드시 상수만을 위해 사용하지는 않는다. const 키워드의 특징은 let과 대부분 동일하므로 let 키워드와 다른 점을 중심으로 살펴볼 필요가 있다.

```
1. 선언과 초기화
2. 재할당 금지
3. 상수
```

1. 선언과 초기화

const 키워드로 선언한 변수는 반드시 선언과 동시에 초기화해야 한다. 그렇지 않을 경우 문법 에러(SyntaxError)가 발생한다.

```js
const bar = 1;
console.log(bar); >>> 1

const foo;
console.log(foo); >>> // SyntaxError: Missing initializer in const declaration
```

2. 재할당 금지

var 또는 let 키워드로 선언한 변수는 재할당이 자유로우나 const 키워드로 선언한 변수는 재할당이 금지된다.

```js
const foo = 1;
foo = 2; // TypeError: Assignment to constant variable.
```

3. 상수

const 키워드로 선언한 변수에 원시 값을 할당한 경우 변수 값을 변경할 수 없다. 원시 값은 변경 불가능한 값이므로 재할당 없이 값을 변경할 수 있는 방법이 없기 때문이다. 이러한 특징을 이용해 const 키워드를 상수를 표현하는 데 사용하기도 한다.

```js
// 세율을 의미하는 0.1은 변경할 수 없는 상수로서 사용될 값이다.
// 변수 이름을 대문자로 선언해 상수임을 명확히 나타낸다.
const TAX_RATE = 0.1;

// 세전 가격
let preTaxPrice = 100;

// 세후 가격
let afterTaxPrice = preTaxPrice + preTaxPrice * TAX_RATE;

console.log(afterTaxPrice); // 110
```

<br/>

### 한 줄 요약

|           var 키워드           | let 키워드  |     const 키워드     |
| :----------------------------: | :---------: | :------------------: |
| 선언 및 초기화 단계(undefined) |  선언 단계  | 선언 + 초기화 + 할당 |
|           할당 단계            | 초기화 단계 |                      |
|               -                |  할당 단계  |                      |

### 식별자 네이밍 규칙은 어떤 것들이 있나요?

식별자는 특수문자를 제외한 문자, 숫자, 언더스코어(\_), 달러 기호($)를 포함할 수 있다.

단 식별자는 특수문자를 제외한 문자, 언더스코어(\_), 달러 기호로 시작해야 한다. 숫자로 시작하는 것은 허용하지 않는다.

<br/>

### 네이밍 컨벤션은 어떤 것들이 있나요?

```js
// 카멜 케이스 (camelCase)
var firstName;

// 스네이크 케이스 (snake_case)
var first_name;

// 파스칼 케이스 (PascalCase)
var FirstName;

// 헝가리언 케이스 (typeHungarianCase)
var strFirstName; // type + identifier
var $elem = document.getElementById("myId"); // DOM 노드
var observable$ = fromEvent(document, "click"); // RxJS 옵저버블
```

<br/>

### 리터럴이 뭔가요?

리터럴(literal)은 사람이 이해할 수 있는 문자 또는 약속된 기호를 사용해 값을 생성하는 표기법(=notation) 을 말합니다.

```
<!-- 숫자 리터럴 3 -->
3
```

위 예제의 3은 단순한 아라비아 숫자가 아니라 숫자 리터럴이다. 사람이 이해할 수 있는 아라비아 숫자를 사용해 숫자 리터럴 3을 코드에 기술하면 자바스크립트 엔진은 이를 평가해 숫자 값 3을 생성한다. 자바스크립트 엔진은 코드가 실행되는 시점인 런타임에 리터럴을 평가해 값을 생성한다.

## 데이터 타입

### 데이터 타입의 종류는 어떤 것들이 있나요?

|   구분    |     데이터 타입     |                        설명                         |
| :-------: | :-----------------: | :-------------------------------------------------: |
| 원시 타입 |  숫자(number)타입   | 숫자, 정수와 실수 구분 없이 하나의 숫자 타입만 존재 |
| 원시 타입 | 문자열(string)타입  |                       문자열                        |
| 원시 타입 | 불리언(boolean)타입 |            논리적 참(true)과 거짓(false)            |
| 원시 타입 |    undefined타입    |  var 키워드로 선언된 변수에 암묵적으로 할당되는 값  |
| 원시 타입 |      null 타입      |  값이 없다는 것을 의도적으로 명시할 때 사용하는 값  |
| 원시 타입 |  심벌(symbol) 타입  |              ES6에서 추가된 7번째 타입              |
| 객체 타입 |                     |                 객체, 함수, 배열 등                 |

<br/>

### 심벌 타입은 뭐죠?

심벌은 ES6에서 추가된 7번째 타입으로, 변경 불가능한 원시 타입의 값이다. 심벌 값은 다른 값과 중복되지 않는 유일무이한 값이다. 따라서 주로 이름이 충동할 위험이 없는 객체의 유일한 프로퍼티 키를 만들기 위해 사용한다.

```js
// 위, 아래, 왼쪽, 오른쪽을 나타내는 상수를 정의한다.
// 중복될 가능성이 없는 심벌 값으로 상수 값을 생성한다.
const Direction = {
  UP: Symbol("up"),
  DOWN: Symbol("down"),
  LEFT: Symbol("left"),
  RIGHT: Symbol("right"),
};

const myDirection = Direction.UP;

if (myDirection === Direction.UP) {
  console.log("You are going UP.");
}
```

<br/>

### 데이터 타입은 왜 필요할까요?

1. 값을 저장할 때 확보해야 하는 메모리 공간의 크기를 결정하기 위해
2. 값을 참조할 때 한 번에 읽어 들여야 할 메모리 공간의 크기를 결정하기 위해
3. 메모리에서 읽어 들인 2진수를 어떻게 해석할지 결정하기 위해

<br/>

### 정적 타이핑이 뭔가요?

C나 자바 같은 정적 타입언어는 변수를 선언할 때 변수에 할당할 수 있는 값의 종류, 즉 데이터 타입을 사전에 선언해야 한다. 이를 명시적 타입 선언이라 한다. 다음은 C에서 정수 타입의 변수를 선언하는 예이다.

```
// c 변수에는 1바이트 정수 타입의 값(-128 ~ 127)만을 할당할 수 있다.
char c;

// num 변수에는 4바이트 정수 타입의 값(-2,124,483,648 ~ 2,124,483,647)만을 할당할 수 있다.
int num;
```

정적 타입 언어는 변수의 타입을 변경할 수 없으며, 변수에 선언한 타입에 맞는 값만 할당할 수 있다. 정적 타입 언어는 컴파일 시점에서 타입 체크를 수행한다. 만약 타입 체크를 통과하지 못했다면 에러를 발생시키고 프로그램의 실행 자체를 막는다. 대표적인 정적 타입 언어로 C, C++, 자바, 코틀린, 고, 러스트 등이 있다.

<br/>

### 동적 타이핑이 뭔가요?

자바스크립트는 정적 타입 언어와 다르게 변수를 선언할 때 타입을 선언하지 않는다. 다만 var, let, const 키워들 사용해 변수를 선언할 뿐이다.

```js
var foo;
console.log(typeof foo); // undefined

foo = 3;
console.log(typeof foo); // number

foo = null;
console.log(typeof foo); // object

foo = Symbol(); // 심벌
console.log(typeof foo); // symbol

foo = {}; // 객체
console.log(typeof foo); // object

foo = []; // 배열
console.log(typeof foo); // object

foo = function () {}; // 함수
console.log(typeof foo); // function
```

자바스크립트의 변수는 선언이 아닌 할당에 의해 타입이 결정 **(타입 추론)**된다. 그리고 **재할당에 의해 변수의 타입은 언제든지 동적으로 변할 수 있다.** 이러한 특징을 동적 타이핑이라고 하며, 자바스크립트를 정적 타입 언어와 구별하기 위해 동적 타입 언어라고 한다. 대표적인 동적 타입 언어로는 자바스크립트, 파이썬, PHP 등이 있다.

## 타입변환과 단축 평가

### 명시적 타입 변환이 뭔가요?

자바스크립트의 모든 값은 타입이 있다. 값의 타입은 개발자의 의도에 따라 다른 타입으로 변환할 수 있다. 개발자가 의도적으로 값의 타입을 변환하는 것을 **명시적 타입 변환 또는 타입 캐스팅**이라 한다.

```js
var x = 10;

// 숫자를 문자열로 타입 캐스팅한다.
var str = x.toString();
console.log(typeof str, str); // string 10

// x 변수의 값이 변경된 것은 아니다.
console.log(typeof x, x); // number 10
```

<br/>

### 명시적 타입 변환 함수를 예를 들어볼 수 있나요?

문자열이 아닌 값을 문자열 타입으로 변환하는 방법

1. String 생성자 함수를 new 연산자 없이 호출하는 방법
2. Object.prototype.toString 메서드를 사용하는 방법
3. 문자열 연결 연산자를 이용하는 방법

```js
// 1. String 생성자 함수를 new 연산자 없이 호출하는 방법
String(1); // -> "1"

// 2. Object.prototype.toString 메서드를 사용하는 방법
(1).toString(); // -> "1"

// 3. 문자열 연결 연산자를 이용하는 방법
1 + ""; // -> "1"
```

숫자 타입이 아닌 값을 숫자 타입으로 변환하는 방법

1. Number 생성자 함수를 new 연산자 없이 호출하는 방법
2. parseInt, parseFloat 함수를 사용하는 방법(문자열만 변환 가능)
3. `+` 단항 산술 연산자를 이용하는 방법
4. `*` 산술 연산자를 이용하는 방법

```js
// 1. Number 생성자 함수를 new 연산자 없이 호출하는 방법
Number("0"); // -> 0

// 2. parseInt, parseFloat 함수를 사용하는 방법(문자열만 변환 가능)
parseInt("0"); // -> 0

// 3. + 단항 산술 연산자를 이용하는 방법
+"0"; // -> 0

// 4. * 산술 연산자를 이용하는 방법
"0" * 1; // -> 0
```

불리언 타입이 아닌 값을 불리언 타입으로 변환하는 방법

1. Boolean 생성자 함수를 new 연산자 없이 호출하는 방법
2. ! 부정 논리 연산자를 두번 사용하는 방법

```js
// 1. Boolean 생성자 함수를 new 연산자 없이 호출하는 방법
// 문자열 타입 => 불리언 타입
Boolean("x"); // -> true
Boolean(""); // -> false
Boolean("false"); // -> true
// 숫자 타입 => 불리언 타입
Boolean(0); // -> false
Boolean(1); // -> true
Boolean(NaN); // -> false
Boolean(Infinity); // -> true
// null 타입 => 불리언 타입
Boolean(null); // -> false
// undefined 타입 => 불리언 타입
Boolean(undefined); // -> false
// 객체 타입 => 불리언 타입
Boolean({}); // -> true
Boolean([]); // -> true

// 2. ! 부정 논리 연산자를 두번 사용하는 방법
// 문자열 타입 => 불리언 타입
!!"x"; // -> true
!!""; // -> false
!!"false"; // -> true
// 숫자 타입 => 불리언 타입
!!0; // -> false
!!1; // -> true
!!NaN; // -> false
!!Infinity; // -> true
// null 타입 => 불리언 타입
!!null; // -> false
// undefined 타입 => 불리언 타입
!!undefined; // -> false
// 객체 타입 => 불리언 타입
!!{}; // -> true
!![]; // -> true
```

<br/>

### 암묵적 타입 변환이 뭔가요?

개발자의 의도와는 상관없이 표션식을 평가하는 도중에 자바스크립트 엔진에 의해 암묵적으로 타입이 자동 변환되기도 한다. 이를 **암묵적 타입 변환 또는 강제 타입 변환**이라 한다.

```js
var x = 10;

// 문자열 연결 연산자 ( + )는 숫자 타입 x의 값을 바탕으로 새로운 문자열을 생성한다.
var str = x + "";
console.log(typeof str, str); // string 10

// x 변수의 값이 변경된 것은 아니다.
console.log(typeof x, x); // number 10
```

<br/>

### truthy / falsy 한 값이 뭔가요?

자바스크립트 엔진은 불리언 타입이 아닌 값을 Truthy 값(참으로 평가되는 값) 또는 Falsy 값(거짓으로 평가되는 값)으로 구분한다. 즉, 제어문의 조건식과 같이 불리언 값으로 평가되어야 할 문맥에서 Truthy값은 true로, Falsy값은 false로 암묵적 타입 변환된다.

아래 값들은 false로 평가되는 Falsy 값이다.

```js
false
undefined
null
0, -0
NaN
' '(빈 문자열)
```

Falsy값에 ! 연산자를 붙이면, 모두 Truthy 값으로 평가되어 실행 가능해진다.

```js
// 아래의 조건문은 모두 코드 블록을 실행한다.
if (!false) console.log(false + " is falsy value");
if (!undefined) console.log(undefined + " is falsy value");
if (!null) console.log(null + " is falsy value");
if (!0) console.log(0 + " is falsy value");
if (!NaN) console.log(NaN + " is falsy value");
if (!"") console.log("" + " is falsy value");
```

## 객체 리터럴

### 자바스크립트에서 객체란 뭘까요?

자바스크립트는 객체 기반의 프로그래밍 언어이며, 자바스크립트를 구성하는 거의 '모든 것'이 객체다. 원시 값을 제외한 나머지 값(함수, 배열, 정규 표현식 등)은 모두 객체이다. 원시 타입은 단 하나의 값만 나타내지만 객체 타입은 다양한 타입의 값(원시 값 또는 다른 객체)을 하나의 단위로 구성한 복합적인 자료구조이다. 또한 원시 타입의 값, 즉 원시 값은 변경 불가능한 값이지만 객체 타입의 값, 즉 객체는 변경 가능한 값이다.

객체는 0개 이상의 프로퍼티로 구성된 집합이며, 프로퍼티는 키(key)와 값(value)으로 구성된다.

```js
var person = {
  name: "Lee",
  age: 20,
};
```

### 함수와 메서드의 차이점에 대해 알고 계신가요?

자바스크립트에서 사용할 수 있는 모든 값은 프로퍼티 값이 될 수 있다. **프로퍼티 값이 함수일 경우**, 일반 함수와 구분하기 위해 메서드(method)라 부른다. 객체 내부에서 객체의 프로퍼티(상태)를 참조하고 조작할 수 있는 동작을 메서드라 부른다.

즉, **메서드는 객체에 묶여 있는 함수를 의미한다.**

```js
var person = {
  name: "Lee",
  age: 20,
  hello: function () {
    console.log("hello :" + this.name);
  },
};

console.log(person);
>>>
{ name: 'Lee', age: 20, hello: [Function: hello] }
```

<br/>

### 자바스크립트에서 객체를 생성하는 방법은 어떤 것들이 있나요?

자바스크립트는 **'프로토타입 기반 객체지향 언어'** 로서 **'클래스 기반 객체지향 언어'** 와는 달리 다양한 객체 생성 방법을 지원한다.

```
1.객체 리터럴
2.Object 생성자 함수
3.생성자 함수
4.Object.create 메서드
5.클래스(ES6)
```

## 원시 값과 객체 비교

### 동적 타이핑을 지원하는 자바스크립트에서 데이터의 타입을 크게 2개로 나누는 이유가 있을까요?

1. 원시 타입의 값, 즉 원시 값은 변경 불가능한 값(immutable value)이다. 이에 비해 객체(참조)타입의 값, 즉 객체는 변경 가능한 값(mutable value)이다.

2. 원시 값을 변수에 할당하면 변수(확보된 메모리 공간)에는 실제 값(100, 실제로는 2진수)이 저장된다.
   이에 비해 객체를 변수에 할당하면 변수(확보된 메모리 공간)에는 참조 값(메모리 주소, 0x00000613)이 저장된다.

3. 원시 값을 갖는 변수를 다른 변수에 할당하면 원본의 원시 값이 복사되어 전달된다. 이를 값에 의한 전달이라 한다.
   이에 비해 객체를 가리키는 변수를 다른 변수에 할당하면 원본의 참조 값(메모리 주소, 0x00000613)이 복사되어 전달된다. 이를 참조에 의한 전달이라 한다.

<br/>

### 값에 의한 전달이 뭔가요?

변수에 원시 값을 갖는 변수를 할당하면 할당받는 변수(copy)에는 할당하는 변수(score)의 원시 값이 복사되어 전달된다. 이를 **'값에 의한 전달'**이라 한다.

```js
var score = 80;

// copy 변수에는 score 변수의 값 80이 복사되어 할당된다.
var copy = score;

console.log(score, copy); // 80  80
console.log(score === copy); // true

// score 변수와 copy 변수의 값은 다른 메모리 공간에 저장된 별개의 값이다.
// 따라서 score 변수의 값을 변경해도 copy 변수의 값에는 어떠한 영향도 주지 않는다.
score = 100;

console.log(score, copy); // 100  80
console.log(score === copy); // false
```

score 변수와 copy 변수의 값 80은 다른 메모리 공간에 저장된 별개의 값이라는 것에 주의하기 바란다. 따라서 score 변수의 값을 변경해도 copy 변수의 값에는 어떠한 영향도 주지 않는다.

<img src="./images/11_4.jpg" alt="값에의한전달">

<br/>

### 참조에 의한 전달이 뭔가요?

객체는 프로퍼티의 개수가 정해져 있지 않으며, 동적으로 추가되고 삭제할 수 있다. 또한 프로퍼티의 값에도 제약이 없다. 따라서 객체는 원시 값(문자열 2바이트\*문자, 숫자 8바이트)과 같이 확보해야 할 메모리 공간의 크기를 사전에 정해 둘 수 없다. 이러한 객체의 가변성의 성질 때문에 객체를 할당한 변수가 기억하는 메모리 주소를 통해 메모리 공간에 접근하면 참조 값에 접근할 수 있다. 참조 값은 생성된 객체가 저장된 메모리 공간의 주소, 그 자체이다.

```js
var person = {
  name: "Lee",
};

// 참조값을 복사(얕은 복사)
var copy = person;
```

객체를 가리키는 변수(원본, person)를 다른 변수(사본, copy)에 할당하면 원본의 참조 값이 복사되어 전달된다. 이를 **'참조에 의한 전달'**이라 한다.

<img src="./images/11_9.jpg" alt="참조에의한전달">

<br/>

## 함수

### 자바스크립트에서 함수를 정의하는 방법은 몇가지가 있나요?

1. 함수 선언문
2. 함수 표현식
3. Function 생성자 함수
4. 화살표 함수 (ES6)

```js
case 1 :함수 선언문

function add(x,y){
  return x+y;
}

case 2: 함수 표현식
var add = function(x,y){
  return x + y;
}

case 3: Function 생성자 함수
var add = new Function('x','y', 'return x+y');

case 4: 화살표 함수(ES6)
var add = (x,y) => x+y;

```

### 함수 선언문과 함수 표현식은 어떤 차이가 있나요?

```js
// 함수 참조
console.dir(add); // ƒ add(x, y)
console.dir(sub); // undefined

// 함수 호출
console.log(add(2, 5));
// 7 why? 함수 선언문은 표현식이 아닌 문으로, 런타임 이전에 js 엔진에 의해 실행된다.

console.log(sub(2, 5));
// TypeError: sub is not a function, why? 함수 표현식(표현식인 문)은 런타임에 값을 할당하기 때문에 sub는 현재 undefined로만 초기화된 상태이다.

// ① 함수 선언문
function add(x, y) {
  return x + y;
}

// ② 함수 표현식
var sub = function (x, y) {
  return x - y;
};
```

코드가 한 줄씩 순차적으로 실행되기 시작하는 런타임에는 이미 함수 객체가 생성되어 있고 함수 이름과 동일한 식별자에 할당까지 완료된 상태이다. 따라서 함수 선언문의 소스코드가 평가되고 실행되기 이전에 함수를 참조할 수 있으며 호출할 수도 있다. 이처럼 **함수 선언문이 코드의 선두로 끌어 올려진 것처럼 동작하는 자바스크립트 고유의 특징을 함수 호이스팅**이라 한다.

변수 호이스팅에 의해 var 키워드로 선언된 함수 표현식은 undefined로 초기화되고, **함수 선언문을 통해 암묵적으로 생성된 식별자는 함수 객체로 초기화된다.** 따라서 var 키워드를 사용한 변수 선언문은 이전에 변수를 참조하면 변수 호이스팅에 의해 undefined로 평가되지만, **함수 선언문으로 정의한 함수를 함수 선언문 이전에 호출하면 함수 호이스팅에 의해 호출이 가능하다.**

<br/>

### 즉시 실행 함수(IIFE)에 대해 알고 있나요? 알고 있다면 아는 내용에 대해 말해보세요

1. **함수 정의와 동시에 즉시 호출되는 함수를 즉시 실행 함수 (IIFE, Immediately Invoked Function Expression)**라고 한다. 즉시 실행 함수는 단 한 번만 호출되며 다시 호출할 수 없다.

```js
//익명 즉시 실행함수
(function () {
  var a = 3;
  var b = 5;
  return a * b;
})();
```

2. 즉시 실행 함수는 함수 이름이 없는 익명 함수를 사용하는 것이 일반적이다. 함수 이름이 있는 기명 즉시 실행 함수도 사용할 수 있다. 하지만 즉시 실행 함수를 다시 호출할 수는 없다.

```js
//기명 즉시 실행 함수
(function foo() {
  var a = 3;
  var b = 5;
  return a * b;
})();

foo(); //ReferenceError: foo is not defined
```

3. 즉시 실행 함수는 반드시 그룹 연산자 (...)로 감싸야 한다.

```js
function () {
 //SyntaxError: Function statements require a function name
...
}
```

함수 정의가 함수 선언문의 형식에 맞지 않기 때문이다. > 그룹 연산자로 함수를 묶은 이유는 먼저 함수 리터럴을 평가해서 함수 객체를 생성하기 위해서다

## 스코프

### 스코프가 뭔가요?

스코프는 유효 범위라는 뜻으로, 식별자(변수)가 유효한 범위를 말합니다.

자바스크립트 엔진은 스코프를 통해 어떤 변수를 참조해야 할 것인지 결정한다. 따라서 스코프란 자바스크립트 엔진이 식별자를 검색할 때 사용하는 규칙이라고도 할 수 있다.

<br/>

### 스코프에는 어떤 종류가 있죠?

스코프는 크게 전역 스코프와 지역 스코프로 구분됩니다.

이는 상대적인 개념이며 전역이란 코드의 가장 바깥 영역을 말합니다. 전역에 변수를 선언하면 전역 스코프를 갖는 전역 변수가 됩니다. 이 전역 변수는 어디서든 참조할 수 있습니다.

지역이란 함수 몸체 내부를 말합니다. 지역은 지역 스코프를 만드는데, 지역에 변수를 선언하면 지역 스코프를 갖는 지역 변수가 됩니다. 지역 변수는 자신의 스코프와 하위 지역 스코프에서 유효합니다.

<br/>

### 렉시컬 스코프를 아나요? 안다면 렉시컬 스코프는 무엇을 의미하나요?

함수를 어디서 '호출' 했는지가 아닌 어디서 '정의' 했는지에 따라 함수의 상위 스코프를 결정하는 것이 정적 스코프 즉, 렉시컬 스코프를 의미합니다.

```js
var x = 1;

function foo() {
  var x = 10;
  bar();
}

function bar() {
  console.log(x);
}

foo(); // ?
bar(); // ?
```

소스코드의 실행에 있어서 foo 함수 내부에서 bar 함수를 '호출' 하더라도, bar 함수는 foo 함수와 동일한 스코프인 전역 스코프에 '정의'되어 있기 때문에 foo 함수 내부의 x=10을 참조할 수 없습니다.

따라서 foo, bar의 호출한 결과는 모두 1로 반환됩니다. 이러한 자바스크립트의 정적인 스코프 특징을 '렉시컬 스코프', '정적 스코프' 라고 부릅니다.

<br/>

### 전역 변수로 변수를 선언하면 생기는 문제점은 무엇이 있을까요?

1. 암묵적 결합
2. 변수의 긴 생명주기
3. 스코프 체인 상에서 종점에 존재
4. 네임스페이스 오염

① 전역 변수를 선언한 의도는 전역, 즉 코드 어디서든 참조하고 할당할 수 있는 변수를 사용하겠다는 것이다. 이는 모든 코드가 전역 변수를 참조하고 변경할 수 있는 암묵적 결합을 허용하는 것이다. 변수의 유효 범위(스코프)가 클수록 코드의 가독성은 나빠지고 의도치 않게 상태가 변경될 수 있는 위험성도 높아진다.

② 전역 변수는 생명 주기가 길다. 따라서 메모리 리소스도 오랜 기간 소비한다. 또한 전역 변수의 상태를 변경할 수 있는 시간도 길고 기회도 많다. 변수 이름이 중복되기라도 한다면 의도치 않은 재할당이 이뤄지기도 한다.

③ 전역 변수는 스코프 체인 상에서 종점에 존재한다. 이는 변수를 검색할 때 전역 변수가 가장 마지막에 검색된다는 것을 말한다. 즉, 전역 변수의 검색 속도가 가장 느리다. 검색 속도의 차이는 그다지 크지 않지만 속도의 차이는 분명히 있다.

④ 자바스크립트의 가장 큰 문제점 중 하나는 파일이 분리되어 있다 해도 하나의 전역 스코프를 공유한다는 것이다. 따라서 다른 파일 내에서 동일한 이름으로 명명된 전역 변수나 전역 함수가 같은 스코프 내에 존재할 경우 예상치 못한 결과를 가져올 수 있다.

## 생성자 함수에 의한 객체 생성

## 함수와 일급 객체

## 프로토타입

## strict mode

## 빌트인 객체

## this

## 실행 컨텍스트

## 클로저

## 클래스

## ES6 함수의 추가 기능

## 배열

## Number

## Math

## Date

## RegExp

## String

## Symbol

## 이터러블

## 스프레드(...) 문법

## 디스트럭처링 할당(구조 분해 할당)

## 브라우저 렌더링 과정

## DOM

## 이벤트

## 타이머

## 비동기 프로그래밍

## Ajax

## REST API

## Promise

## 제너레이터와 async/await

## 에러처리

## 모듈
