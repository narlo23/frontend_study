## HTML(HyperText Markup Language)
웹 콘텐츠의 의미와 구조를 정의할 때 사용하는 마크업 언어를 말한다.   
Hypertext란 웹 페이지를 다른 페이지로 연결하는 링크를 말한다.

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
