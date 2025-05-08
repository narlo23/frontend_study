## JS 코딩테스트 문법 정리

### 반복문
1. forEach
- 각 배열 요소에 대해 제공된 함수를 한 번씩 실행
```javascript
arr.forEach((element, index) => {
  console.log(element);
});
```
2. map
- 호출한 배열의 모든 요소에 주어진 함수를 호출한 결과로 채운 새로운 배열을 생
```javascript
arr.map((element) => {
  return element * 2;
});
```

3. filter
- 배열의 일부에 대한 얕은 복사본을 생성하고, 주어진 배열에서 제공된 함수에 의해 구현된 테스트를 통과한 요소로만 필터링
```javascript
const words = ["spray", "elite", "exuberant", "destruction", "present"];
const result = words.filter((word) => word.length > 6);
console.log(result);
// Expected output: Array ["exuberant", "destruction", "present"]
```

4. reduce
- 배열의 각 요소에 대해 주어진 리듀서 함수를 실행하고, 하나의 결과값을 반환
```javascript
  arr.reduce(callback[, initialValue])
```

5. some
- 배열 안의 어떤 요소라도 주어진 판별 함수를 적어도 하나라도 통과하는지 테스트
```javascript
array.some((element) => element % 2 === 0);
/* 짝수가 하나라도 존재한다면 true, 하나도 없으면 false */
```

6. every
- 배열의 모든 요소가 제공된 함수로 구현된 테스트를 통과하는지 테스트
```javascript
array.every((value) => value < 40);
/* 모든 원소가 40보다 작다면 true, 하나라도 40보다 크거나 같은 값이 있다면 false) */
```

매개변수
callback
- 배열의 각 요소에 대해 실행할 함수
- accumulator : 콜백의 반환값을 누적
- currentValue: 처리할 현재 요소
- currentIndex : 처리할 현재 요소의 인덱스
- array : reduce를 호출한 배열
initialValue
- callback의 최초 호출에서 첫 번째 인수에 제공하는 값, 초기값을 제공하지 않으면 배열의  번째 요소를 사용

```javascript
const array1 = [1, 2, 3, 4];

const initialValue = 0;
const sumWithInitial = array1.reduce((accumulator, currentValue) => accumulator + currentValue, initialValue,);
console.log(sumWithInitial);
// Expected output: 10
```

### 함수
join
- 배열의 모든 요소를 쉼표나 지정된 구분 문자열로 구분하여 연결한 새 문자열을 만들어 반환
```javascript
const elements = ["Fire", "Air", "Water"];

console.log(elements.join());
// Expected output: "Fire,Air,Water"
```

### 자료형 변환
#### 1. int to str  
**String**
```javascript
  const num = 123;
  console.log(String(num));
```

**toString**
- 숫자와 기수를 인자로 받음
```javascript
  const str = (3).toString(2); /* 숫자 3을 2진수로 변환하여 문자열로 리턴 */
```

#### 2. str to int  
**Number**
- 숫자로 변환될 수 없는 값을 넘겨준다면 NaN 반환
```javascript
const str = "123";
console.log(Number(str));
```

**parseInt**
- 문자열과 기수를 인자로 받음
```javascript
const str = "123";
console.log(parseInt(str, 10)); /* str을 10진수로 변경 */
```

**단항 더하기 연산자**  
![Image](https://github.com/user-attachments/assets/6ae4050c-551e-44f2-a8e1-63fda576d36a)

#### 3. str to float  
**parseFloat**
- 값을 받아 실수를 반환
- 문자열의 첫 글자가 숫자로 변환할 수 없는 경우 NaN 반환

### 얕은 복사와 깊은 복사
#### 얕은 복사
- 인스턴스가 메모리에 새로 생성되지 않음
- 값 자체를 복사하는 것이 아니라 주소값을 복사하여 같은 메모리를 가리킴

**slice()** 이용  
slice메서드는 배열의 일부를 추출하여 새로운 배열을 생성한다.  
인자를 제공하지 않으면 배열 전체를 복사한다.  

**스프레드 연산자**를 사용한 얕은 복사  
```javascript
const copiedArr = [...originalArr];
```

**Array.from()을** 이용한 얕은 복사  
유사 배열 객체나 반복 가능한 객체를 새로운 배열로 변환

**concat** 메서드를 사용한 얕은 복사
기존 배열을 변경하지 않고, 새로운 배열을 반환
```javascript
const copiedArr = [].concat(originarArr);
```

#### 깊은 복사
- 깊은 복사는 데이터 자체를 통째로 복사
- 복사된 두 객체는 완전히 독립적인 메모리를 차지
- 데이터 무결성이 중요한 복잡한 데이터 구조에 적

### 정규표현식
문자열에서 특정 문자 조합을 찾기 위한 패턴
RegExp의 exec()와 test() 메서드를 사용할 수 있다.
String의 match(), matchAll(), replace(), replaceAll(), search(), split() 메서드도 사용할 수 있다.

#### 정규표현식 리터럴
```javascript
const re = /ab+c/; /* 정규 표현식 리터럴, 스크립트를 불러올 때 컴파일 됨 */

const re = new RegExp("ab+c"); /* 생성자 함수 사용, 런타임에 컴파일 됨 */
```
- 슬래시로 패턴을 감싸 작성한다.

**escape**
역슬래시(\) 이용
```
ex) a*b와 일치해야 한다면 /a\*b/를 사용
ex) "A:\", "B:\", "C:\", ..., "Z:\"와 일치해야 할 때, 역슬래시의 경우에도 /[A-Z]:\\/처럼 앞에 \를 하나 더 붙여서 사용
```

정규표현식 뒤의 g는 전체 문자열을 탐색해서 모든 일치를 반환하도록 지정하는 "전역 탐색 플래그"이다.
```javascript
function escapeRegExp(string) {
  return string.replace(/[.*+?^${}()|[\]\\]/g, "\\$&"); // $&은 일치한 문자열 전체를 의미
}
```

**문자 횟수**  
? : 최대 1번 (없거나 1개)   
\* : 여러 개 (0개 이상)  
\+ : 최소 1개 (1개 이상)   
{n} : n개   
{min, } : 최소 min개 이상  
{min, max} : min개 이상 max개 이하  

```javascript
  const result = str.match(new RegExp(`.{1, ${n}}`, "g"));
```
