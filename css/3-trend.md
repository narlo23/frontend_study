### Nesting
css 규칙 안에 다른 css 규칙을 중첩해서 작성할 수 있게 해 주는 기능
```css
  .card {
  padding: 1rem;

  &:hover {
    background-color: #f0f0f0;
  }

  h2 {
    font-size: 1.2rem;
  }
}
```

### Container Query
css에서 요소가 부모의 크기에 따라 반응하도록 만드는 기능
기존의 media query는 viewport 크기 기준이었지만,
container는 부모 컨테이너 크기를 기준으로 반응형 스타일을 적용할 수 있게 해 줌
컴포넌트 기반 프레임워크과 궁합이 좋음

```
  컴포넌트 기반 개발이 많아진 요즘, 뷰포트 기반 반응형만으로는 부족함
  ex) 같은 컴포넌트를 사이드바와 메인 영역에서 다르게 보이게 하고 싶을 때
```
```css
.article {
  container-type: inline-size;
  container-name: article-container;
}

@container article-container (max-width: 600px) {
  .title {
    font-size: 1.1rem;
  }
}
```

### has 선택자
css에서 부모 선택자처럼 동작할 수 있게 해 주는 기능
내부에 포함된 요소나 상태가 있을 때 조건을 만족하는 외부(부모나 형제) 요소에 스타일을 적용
```css
.card:has(img) {
  border: 2px solid blue;
}
```
.card 안에 img가 있으면 .card의 테두리를 2px solid blue로 설정

```css
.card:not(:has(*)) {
  display: none;
}
```
.card가 비어 있으면 숨김

### is 선택자
여러 셀렉터를 묶어 간결하게 스타일 적용
내부에서 가장 강한 선택자의 우선순위를 사용

### where 선택자
스타일 초기화 또는 낮은 우선순위 적용
항상 우선순위 0을 사용

### scope 규칙
css의 전역성 문제를 완화
특정 컨텍스트 내에서 스타일을 제한적으로 적용하는 방법
```css
@scope (.container) {
  h1 {
    color: red;
  }
}
```

### subgrid
자식 요소가 부모의 grid 구조를 그대로 상속받아 사용하는 기능
일관된 정렬을 유지하고자 할 때 유용
grid-template-rows, grid-template-columns, gap 지원
```css
  .parent {
  display: grid;
  grid-template-columns: 1fr 2fr;
}

.child {
  display: grid;
  grid-template-columns: subgrid;
}
```

### Layered css
스타일의 우선순위를 계층으로 관리할 수 있도록 도와줌
규모가 큰 프로젝트에서 스타일 충돌을 방지하고, 스타일 시스템을 체계적으로 구성하는 데 유용
@layer를 사용하여 레이어 별 우선순위를 명시적으로 지정할 수 있어
기본 스타일, 컴포넌트 스타일, 유저 커스텀 스타일 등을 명확하게 구분하고 순서를 지정할 수 있음
레이어에 속하지 않은 스타일은 가장 위 레이어로 간주됨

```css
@layer reset, base, components, utilities;
```
우선순위 : reset < base < components < utilities
