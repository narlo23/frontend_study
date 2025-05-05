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
  
