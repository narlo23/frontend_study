## CSS (Cascading Style Sheets)

HTML이나 XML로 작성된 문서의 표시 방법을 기술하기 위한 스타일 시트 언어

### CSS ruleset
![Image](https://github.com/user-attachments/assets/ccdb73d5-ad69-4180-8eb5-ef2d86fcdd49)
1) 선택자(selector) : HTML 요소 이름, 꾸밀 요소를 선택
2) 선언 : 꾸미기 원하는 요소의 속성 명시 (속성과 속성 값으로 이루어짐)
3) 속성(property) : HTML 요소를 꾸밀 수 있는 방법, rule 내에서 영향을 줄 속성을 선택
4) 속성 값 : 주어진 속성을 위한 많은 가능한 결과 중 하나를 선택

#### 여러 요소 선택
여러 타입을 선택하고 모두에게 하나의 rule set을 적용
```css
  p, li, h1 {
    color: red;
  }
```

#### 선택자
- 요소 선택자(타입 선택자) : p
- 아이디 선택자 : #my-id
- 클래스 선택자 : .my-class
- 속성 선택자 : img[src]
```
  <img src="myimage.png">는 선택하지만
  <img>는 선택 안함
```
- 수도(pseudo) 클래스 선택자 (특정 요소이지만 특정 상태에 있을 때)
```
  a:hover <a>를 선택하지만 마우스 포인트가 링크 위에 있을 때(hover 상태일 때)만 선택함
```

#### 결합자
하위 결합자 (>)
```css
  article > p {
  }
```
article 요소의 자식인 p를 선택
