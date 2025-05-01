### CSS Layout

#### display
- block
- inline
- inline-block
- grid
- flex

#### flexbox
1차원으로 수평, 수직 영역 중 하나의 방향으로만 레이아웃을 나눌 수 있다.

flex-direction : flex 방향 설정
- row
- row-reverse
- column
- column-reverse

justify-content : 가로 방향 정렬
- flex-start : 요소를 컨테이너의 왼쪽으로 정렬
- flex-end : 요소를 컨테이너의 오른쪽으로 정렬
- center : 요소를 컨테이너의 가운데로 정렬
- space-between : 요소 사이에 동일한 간격을 둠
- space-around : 요소 주위에 동일한 간격을 둠

align-items : 세로 방향 정렬
- flex-start : 요소를 컨테이너의 꼭대기로 정렬
- flex-end : 요소를 컨테이너의 바닥으로 정렬
- center : 요소를 컨테이너의 세로 상 가운데로 정렬
- baseline : 요소를 컨테이너의 시작 위치에 정렬
- stretch : 요소를 컨테이너에 맞도록 늘림

flex-wrap : flex 요소를 한 줄 또는 여러 줄에 걸쳐 정렬
- nowrap : 모든 요소들을 한 줄에 정렬
- wrap : 요소들을 여러 줄에 걸쳐 정렬
- wrap-reverse: 요소들을 여러 줄에 걸쳐 반대로 정렬

flex-flow : flex-direction과 flex-wrap 속성을 간략히 한 속성

#### grid
2차원으로 수평, 수직을 동시에 영역을 나눌 수 있다.

grid-column-start : 그리드 요소의 시작 열 위치 지정
grid-column-end : 그리드 요소의 마지막 열 위치 지정
grid-row-start : 그리드 요소의 시작 행 위치 지정
grid-row-end : 그리드 요소의 마지막 행 위치 지정


#### float
왼쪽이나 오른쪽으로 이동되어 일반 흐름에서 벗어나게 되며 주변 콘텐츠가 그 주위에 떠 있게 된다.
- left
- right
- none
- inherit

#### positioning
일반 흐름에서 배치되는 위치에서 다른 위치로 이동할 수 있다.
페이지에서 특정 항목의 위치를 관리하고 미세 조정하는 데 사용된다.
- static : default
- relative : 일반 흐름의 위치에 비해 상대적으로 이동
- absolute : 일반적 레이아웃 흐름에서 완전히 벗어나 별도의 레이어에 있는 거처럼 이동
             가장 가까운 위치에 있는 상위요소의 가장자리를 기준으로 한 위치를 고정할 수 있음
- fixed : viewport를 기준으로 요소를 고정
- sticky : viewport에서 사전에 정의된 오프셋에 도달할 때까지 요소가 relative처럼 작동하고, 그 시점부터는 fixed와 같이 작동하는 방법

### 반응형 디자인
웹 페이지가 모든 화면 크기와 해상도에서 잘 렌더링되도록 하면서도 사용성을 보장하는 웹 디자인 접근 방식
- 미디어 쿼리나 flex, grid 등의 레이아웃 방식을 활용하여 반응형 디자인을 구현할 수 있다. 
- 뷰포트 단위(vw)를 사용하여 반응형 디자인을 구현할 수 있다.

#### 미디어 쿼리
사용자의 화면이 특정 너비 또는 특정 해상도보다 큰지를 테스트하고 css를 선택적으로 적용하여
사용자의 요구에 맞게 페이지의 스타일을 지정할 수 있다.

```css
  @media media-type and (media-feature-rule) {
  /* CSS rules go here */
}
```
- orientation
```css
  @media (orientation: landscape) {
  body {
    color: rebeccapurple;
  }
}
```
orientation 기능으로 세로 모드인자 가로 모드인지 검사할 수 있다.
장치가 가로 방향인 경우 본문 텍스트 색상을 변경하는 코드이다.
