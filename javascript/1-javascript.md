## JavaScript

웹 페이지를 대화식으로 만드는 데 사용되는 크로스 플랫폼, 객체 지향 스크립팅 언어
프로토타입 기반, 다중 패러다임, 단일 스레드, 동적 언어
객체지향형, 명령형, 선언형 스타일 지원

1. 클라이언트 측

- 브라우저와 문서 객체 모델(DOM)을 제어하는 객체를 제공하여 코어 언어를 확장한다.
- 클라이언트 측 확장을 사용하면 애플리케이션이 HTML 양식에 요소를 배치하고 마우스 클릭, 양식 입력, 페이지 탐색과 같은 사용자 이벤트에 응답할 수 있다.

2. 서버 측

- 서버에서 JS를 실행하는 것과 관련된 객체를 제공하여 핵심 언어를 확장한다.
- 서버측 확장을 사용하면 애플리케이션이 데이터베이스와 통신하고, 애플리케이션의 한 호출에서 다른 애플리케이션으로 연속적인 정보를 제공하거나 서버에서 파일을 조작할 수 있다.

### 선언

#### var

중복 선언 가능
변수 값 재할당 가능
함수 단위 스코프(function level scope)

#### let

같은 이름의 변수를 두 번 이상 재선언 할 수 없음 (SyntaxError 에러 발생)
변수 값 재할당 가능
블록 단위 스코프(block level scope)

#### const

같은 이름의 변수를 두 번 이상 재선언 할 수 없음 (SyntaxError 에러 발생)
변수 값 재할당 불가능 (오브젝트를 담으면 오브젝트 내의 데이터는 변경 가능)
블록 단위 스코프(block level scope)
const는 반드시 값을 선언과 동시에 정의해야 함

### 호이스팅(Hoisting)

변수 및 함수 선언문이 스코프 내의 최상단으로 끌어올려지는 현상
=> 선언하기 전에 해당 변수를 사용할 수 있다. 하지만 초기화 전까지는 undefined 값을 가진다.

```
    1) 기본적으로 const
    2) 재할당이 필요한 경우 let
    3) var은 사용하지 말자 (실수가 발생하기 쉽다)
```

함수 표현식은 호이스팅 되지 않는다.

```javascript
    foo(); // "bar"

    /* 함수 선언 */
    function foo() {
        console.log("bar");
    }

    baz(); // TypeError: baz is not a function

    /* 함수 표현식 */``
    var baz = function () {
        console.log("bar2");
    }
```

### 예외 처리
throw : 예외 던지기
try...catch : 실행을 시도할 블록을 표시하고, 그 안에서 예외가 발생할 경우 처리를 맡을 하나 이상의 반응 명령문을 지정
finally : try, catch 블록이 끝난 후 이어서 실행할 명령문을 지정

### Error
Error 객체의 name, message 속성으로부터 오류의 유형에 따라 좀 더 정제된 메시지를 가져올 수 있다.

### 루프와 반복
**1. for문**
```javascript
for ([초기문]; [조건문]; [증감문])
  문장
   ``` 
**2. do...while문**  
특정한 조건이 거짓으로 판별될 때까지 반복 (조건문 확인 전에 문장 한 번 실행)
```javascript
do
    문장
while (조건문);
```
**3. while문**  
어떤 조건문이 참이기만 하면 문장을 계속해서 수행
```javascript
while (조건문)
   문장
```
**4. 레이블문**  
프로그램에서 다른 곳으로 참조할 수 있도록 식별자로 문을 제공
```javascript
label:
    statement
```
**5. for...in문**  
객체의 열거 속성 이름을 통해 지정된 변수를 반복
```javascript
for (variable in object) {
    statements
}
```
**6. for...of문**  
각각의 고유한 특성의 값을 실행할 명령과 함께 사용자 지정 반복 후크를 호출하여, 반복 가능한 객체를 통해 반복하는 루프 생성
```javascript
for (variable of object) {
    statement
}
```

#### for...in과 for...of의 차이
```javascript
let arr = [3, 5, 7];
arr.foo = "hello";

for (let i in arr) {
  console.log(i); // logs "0", "1", "2", "foo"
}

for (let i of arr) {
  console.log(i); // logs "3", "5", "7"
}
```

### 함수 표현식
함수 표현식(function expression) = 익명 함수
``` javascript
const square = function (number) {
    return number * number;
};

const x = square(4);
```

함수 표현식에서도 함수 이름 지정 가능
```javascript
const factorial = function fac(n) {
  return n < 2 ? 1 : n * fac(n - 1);
};

console.log(factorial(3));
```

### 나머지 매개변수
```javascript
function multiply(multiplier, ...theArgs) {
  return theArgs.map((x) => multiplier * x);
}

var arr = multiply(2, 1, 2, 3);
console.log(arr); // [2, 4, 6]
```

### 화살표 함수
```javascript
var a3 = a.map((s) => s.length);
```

### instanceof
지정한 객체가 지정한 객체 타입에 속하면 true를 반환
```javascript
objectName instanceof objectType;
```
