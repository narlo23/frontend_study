## HTML(HyperText Markup Language)
웹 콘텐츠의 의미와 구조를 정의할 때 사용하는 마크업 언어를 말한다.   
Hypertext란 웹 페이지를 다른 페이지로 연결하는 링크를 말한다.

### 태그
HTML 요소는 태그를 사용해서 문서의 다른 텍스트와 구분한다.  
태그는 "<" 태그 이름 ">" 로 이루어진다.  
태그 안의 요소 이름은 대소문자를 구분하지 않는다.  

### HTML 문서 해부
<!DOCTYPE html>
- html 파일에서 가장 먼저 선언되어야 하는 구문이다.
- HTML 표준에서 권장하는 DOCTYPE이다.
- 웹 브라우저가 html 문서를 읽을 때, 이 선언을 보고 문서의 버전을 판단한다.

```
HTML5 이전의 DOCTYPE은 DTD(Document Type Definition)를 참조하여 문서의 구조와 규칙을 정의한다.
DOCTYPE 선언은 HTML 문서가 어떤 DTD를 사용할 것인지 명시하여, 브라우저가 문서를 올바르게 해석하고 렌더링 할 수 있도록 한다.

HTML5부터는 DTD를 통해 문서의 구조를 정의하지 않고, 브라우저가 내장된 파서로 HTML5 문서를 해석한다.

렌더링 모드에는 표준 모드(Standard Mode)와 비표준모드(Quirks Mode)가 있다.
Quirks Mode는 오래된 웹 브라우저를 보여줄 때, 하위 호환성을 유지하기 위해서 표준모드를 대신해 쓰이는 모드이다.
오래된 웹 페이지들이 최신 버전의 브라우저에서 깨져 보이지 않으려고 주로 사용한다.
```

#### DOCTYPE을 작성하지 않는다면?
```
HTML을 작성할 때 DOCTYPE을 선언하면 Standard Mode로 실행하고,
DOCTYPE 선언이 따로 없으면 Quirks Mode로 실행한다.

* 따라서 DOCTYPE을 선언하지 않는다면 의도한 디자인, 기능과 다른 결과물을 보게 될 수 있다.
```

### html
페이지 전체의 콘텐츠를 감싸며, 루트 요소라고도 한다.
문서의 고유 언어를 설정하는 lang 속성을 포함한다.

```html
  <html lang="en-US"></html>
```

```
  HTML 문서는 언어가 설정되어 있으면 검색 엔진에 보다 효과적으로 색인화된다.
```

### Head
head는 페이지 로딩 시 웹 브라우저에는 보이지 않는 부분이다.
페이지의 title, css 링크, 파비콘 링크, 메타데이터와 같은 정보를 담고 있다.
- title : 페이지의 제목을 설정한다. 북마크나 즐겨찾기에서 페이지를 설명하는 것으로도 사용된다.

#### meta 태그
1. 인코딩 표시
```html
  <meta charset="utf-8" />
```
문서에서 허용하는 encoding에 대해 표시한다.

2. 저자, 머릿말 요약
```html
  <meta name="author" content="Chris Mills" />
  <meta
    name="description"
    content="The MDN Learning Area aims to provide
    complete beginners to the Web with all they need to know to get
    started with developing web sites and applications." />
```
페이지 작성를 정하고, 머릿말을 요약하는 데 유용하게 쓰인다.
- name : 메타 요소가 어떤 정보를 가지고 있는지 알려준다.
- content : 실제 메타데이터의 컨텐츠를 의미한다.

3. 스타일 시트 연결
```html
  <link rel="stylesheet" href="my-css-file.css" />
```
- rel="stylesheet" : 이 링크의 문서가 스타일 시트임을 나타낸다.
- href : 스타일 시트의 파일 경로를 의미한다.

4. 뷰포트 설정
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
- width=device-width : 페이지의 너비를 스크린 너비로 설정한다. (렌더링 영역을 기기의 뷰포트 크기와 같게 만들어준다.)
- initial-scale=1.0 : 처음 페이지 로딩 시 확대/축소가 되지 않은 원래 크기를 사용하도록 한다. (0~10 사이 값을 가진다.)
- minimum-scale
- maximum-scale
- user-scalable : yes 또는 no 값을 가지며 사용자가 화면을 확대/축소 할 수 있는지를 지정한다.

```
모바일 기기는 다양한 모양과 크기를 가지고 있으며, 화면의 픽셀 비율도 각기 다르다.
모바일 브라우저에서의 뷰포트는 웹 콘텐츠가 표시되는 창 영역을 의미한다.
모바일 브라우저는 일반적으로 화면보다 넓은 980px 크기의 가상 창 또는 뷰포트에 페이지를 렌더링 한 후,
렌더링 된 결과를 축소하여 모든 화면을 한 번에 볼 수 있도록 한다.
사용자는 이동 및 확대/축소를 통해 페이지의 여러 영역을 볼 수 있다.
모바일 브라우저가 화면 너비로 기본 980px 대신 뷰포트 너비를 사용하도록 위 태그를 이용해 설정할 수 있다.
``` 

### HTML 태그
HTML 요소는 태그를 사용해서 문서의 다른 텍스트와 구분한다.  
태그는 "<" 태그 이름 ">" 로 이루어진다.  
태그 안의 요소 이름은 대소문자를 구분하지 않는다.  

### HTML 문서 해부
<!DOCTYPE html>
- html 파일에서 가장 먼저 선언되어야 하는 구문이다.
- HTML 표준에서 권장하는 DOCTYPE이다.
- 웹 브라우저가 html 문서를 읽을 때, 이 선언을 보고 문서의 버전을 판단한다.

```
HTML5 이전의 DOCTYPE은 DTD(Document Type Definition)를 참조하여 문서의 구조와 규칙을 정의한다.
DOCTYPE 선언은 HTML 문서가 어떤 DTD를 사용할 것인지 명시하여, 브라우저가 문서를 올바르게 해석하고 렌더링 할 수 있도록 한다.

HTML5부터는 DTD를 통해 문서의 구조를 정의하지 않고, 브라우저가 내장된 파서로 HTML5 문서를 해석한다.

렌더링 모드에는 표준 모드(Standard Mode)와 비표준모드(Quirks Mode)가 있다.
Quirks Mode는 오래된 웹 브라우저를 보여줄 때, 하위 호환성을 유지하기 위해서 표준모드를 대신해 쓰이는 모드이다.
오래된 웹 페이지들이 최신 버전의 브라우저에서 깨져 보이지 않으려고 주로 사용한다.
```

#### DOCTYPE을 작성하지 않는다면?
```
HTML을 작성할 때 DOCTYPE을 선언하면 Standard Mode로 실행하고,
DOCTYPE 선언이 따로 없으면 Quirks Mode로 실행한다.

* 따라서 DOCTYPE을 선언하지 않는다면 의도한 디자인, 기능과 다른 결과물을 보게 될 수 있다.
```

### Head
head는 페이지 로딩 시 웹 브라우저에는 보이지 않는 부분이다.
페이지의 title, css 링크, 파비콘 링크, 메타데이터와 같은 정보를 담고 있다.

#### meta 태그
1. 인코딩 표시
```html
  <meta charset="utf-8" />
```
문서에서 허용하는 encoding에 대해 표시한다.

2. 저자, 머릿말 요약
```html
  <meta name="author" content="Chris Mills" />
  <meta
    name="description"
    content="The MDN Learning Area aims to provide
    complete beginners to the Web with all they need to know to get
    started with developing web sites and applications." />
```
페이지 작성를 정하고, 머릿말을 요약하는 데 유용하게 쓰인다.
- name : 메타 요소가 어떤 정보를 가지고 있는지 알려준다.
- content : 실제 메타데이터의 컨텐츠를 의미한다.

3. 스타일 시트 연결
```html
  <link rel="stylesheet" href="my-css-file.css" />
```
- rel="stylesheet" : 이 링크의 문서가 스타일 시트임을 나타낸다.
- href : 스타일 시트의 파일 경로를 의미한다.

4. 문서의 기본 언어 설정
```html
  <html lang="en-US"></html>
```
HTML 문서는 언어가 설정되어 있으면 검색 엔진에 보다 효과적으로 색인화되며, 화면 판독기를 사용하는 시각장애인 사용자에게 유용하다.




----
### 참조
[MDN](https://developer.mozilla.org/ko/docs/Learn_web_development/Core/Structuring_content)
