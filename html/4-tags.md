## Tags

### blockquote, q
#### blockquote
- 인용문 넣기
- 블록 레벨 태그
#### q
- 인용 표기
- 인라인 레벨 태그
- 줄바꿈 없이 한 줄로 표시되고 인용 내용을 구별할 수 이도록 따옴표를 붙여 표시

### pre
- preformat의 줄임말  
- 입력하는 그대로 화면에 표시하기  
- 웹 문서를 소리로 읽어 주는 기계나 점자로 표시해 주는 기계는  
pre 태그가 적용된 부분을 만나면 건너뛰어 버리기 때문에 접근성을 위해 대체 텍스트를 추가하는 것이 좋다.
```
html에서는 아무리 많은 공백을 넣어도 브라우저 창에는 한 개의 공백만 표시된다.
하지만 pre 태그를 사용하면 소스에 표시한 공백이 브라우저에 그대로 표시된다.
```

### strong, b
- 텍스트를 굵게 표시하고 싶을 때 사용
- strong : 굵게 강조할 텍스트
- b : 굵게 표시할 텍스트
```
강조 여부에 따라 화면 낭독기가 다르게 알려줌
```

### em, i
- 이탤릭체로 표시
- em : emphasis, 흐름 상 특정 부분을 강조하고 싶을 때 사용
- i : italic, 관용구에 사용

### mark
- 형광펜 효과
- 선택한 부분의 배경색이 노란색이 되며 형광펜으로 그어 놓은 듯한 효과를 냄

### ul ol dl
#### ul
- unordered list

#### ol
- ordered list
- type 속성을 이용해 숫자 종류를 조절할 수 있음

#### dl
- description list
- 제목과 설명이 한 쌍인 설명 목록
```html
<dl>
  <dt> 제목 </dt>
  <dd> 설명 </dd>
</dl>
```

### a
- 링크 만들기
- target
1. _blank : 링크 내용이 새 창이나 새 탭에서 열린다.
2. _self : target 속성의 기본 값으로 링크가 있는 화면에서 열린다.
3. _parent : 프레임을 사용했을 때 링크 내용을 부모 프레임에 표시한다.
4. _top : 프레임을 사용했을 때 프레임에서 벗어나 링크 내용을 전체 화면에 표시한다.

### form
- method : 사용자가 입력한 내용들을 서버 쪽 프로그램으로 어떻게 넘겨줄지 지정한다.
  1) get
  2) post
- action : form 태그 안의 내용들을 처리해 줄 서버 상의 프로그램을 지정한다.

### input
#### type 종류
- hidden : 사용자에게는 보이지 않지만 서버로 넘겨지는 값을 가짐
- text : 한 줄짜리 텍스트를 입력할 수 있는 텍스트 상자
- search : 검색 상자
- tel : 전화번호 입력 필드
- url : URL 주소 입력 필드
- email : 메일 주소를 입력할 수 있는 필드
- password : 비밀번호 입력 필드
- datetime : 국제 표준시(UTC)로 설정된 날짜와 시간
- datetime-local : 사용자가 있는 지역을 기준으로 날짜와 시간
- date : 사용자 지역을 기준으로 날짜(연, 월, 일)
- month : 사용자 지역을 기준으로 날짜(연, 월)
- week : 사용자 지역을 기준으로 날짜(연, 주)
- time : 사용자 지역을 기준으로 시간
- number : 숫자를 조절할 수 있는 화# Tags

### blockquote, q
#### blockquote
- 인용문 넣기
- 블록 레벨 태그
#### q
- 인용 표기
- 인라인 레벨 태그
- 줄바꿈 없이 한 줄로 표시되고 인용 내용을 구별할 수 이도록 따옴표를 붙여 표시

### pre
- preformat의 줄임말  
- 입력하는 그대로 화면에 표시하기  
- 웹 문서를 소리로 읽어 주는 기계나 점자로 표시해 주는 기계는  
pre 태그가 적용된 부분을 만나면 건너뛰어 버리기 때문에 접근성을 위해 대체 텍스트를 추가하는 것이 좋다.
```
html에서는 아무리 많은 공백을 넣어도 브라우저 창에는 한 개의 공백만 표시된다.
하지만 pre 태그를 사용하면 소스에 표시한 공백이 브라우저에 그대로 표시된다.
```

### strong, b
- 텍스트를 굵게 표시하고 싶을 때 사용
- strong : 굵게 강조할 텍스트
- b : 굵게 표시할 텍스트
```
강조 여부에 따라 화면 낭독기가 다르게 알려줌
```

### em, i
- 이탤릭체로 표시
- em : emphasis, 흐름 상 특정 부분을 강조하고 싶을 때 사용
- i : italic, 관용구에 사용

### mark
- 형광펜 효과
- 선택한 부분의 배경색이 노란색이 되며 형광펜으로 그어 놓은 듯한 효과를 냄

### ul ol dl
#### ul
- unordered list

#### ol
- ordered list
- type 속성을 이용해 숫자 종류를 조절할 수 있음

#### dl
- description list
- 제목과 설명이 한 쌍인 설명 목록
```html
<dl>
  <dt> 제목 </dt>
  <dd> 설명 </dd>
</dl>
```

### a
- 링크 만들기
- target
1. _blank : 링크 내용이 새 창이나 새 탭에서 열린다.
2. _self : target 속성의 기본 값으로 링크가 있는 화면에서 열린다.
3. _parent : 프레임을 사용했을 때 링크 내용을 부모 프레임에 표시한다.
4. _top : 프레임을 사용했을 때 프레임에서 벗어나 링크 내용을 전체 화면에 표시한다.

### form
- method : 사용자가 입력한 내용들을 서버 쪽 프로그램으로 어떻게 넘겨줄지 지정한다.
  1) get
  2) post
- action : form 태그 안의 내용들을 처리해 줄 서버 상의 프로그램을 지정한다.

### input
#### type 종류
- hidden : 사용자에게는 보이지 않지만 서버로 넘겨지는 값을 가짐
- text : 한 줄짜리 텍스트를 입력할 수 있는 텍스트 상자
- search : 검색 상자
- tel : 전화번호 입력 필드
- url : URL 주소 입력 필드
- email : 메일 주소를 입력할 수 있는 필드
- password : 비밀번호 입력 필드
- datetime : 국제 표준시(UTC)로 설정된 날짜와 시간
- datetime-local : 사용자가 있는 지역을 기준으로 날짜와 시간
- date : 사용자 지역을 기준으로 날짜(연, 월, 일)
- month : 사용자 지역을 기준으로 날짜(연, 월)
- week : 사용자 지역을 기준으로 날짜(연, 주)
- time : 사용자 지역을 기준으로 시간
- number : 숫자를 조절할 수 있는 화살표
- range : 숫자를 조절할 수 있는 슬라이드 막대
- color : 색상 표
- checkbox : 주어진 항목에서 2개 이상 선택 가능한 체크박스
- radio : 1개만 선택할 수 있는 라디오 버튼
- file : 파일을 첨부할 수 있는 버튼
- submit : 서버 전송 버튼
- image : submit 버튼 대신 사용할 이미지
- reset : 리셋 버튼
- button : 버튼
