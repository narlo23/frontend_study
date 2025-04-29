## 반응형 이미지
```html
  <img
  srcset="elva-fairy-480w.jpg 480w, elva-fairy-800w.jpg 800w"
  sizes="(max-width: 600px) 480px,
         800px"
  src="elva-fairy-800w.jpg"
  alt="요정 옷을 입은 엘바" />
```
srcset, sizes 속성을 통해 사용자 디바이스 화면 크기에 따라 로드할 이미지의 최적의 해상도를 결정할 수 있다.
=> 이를 통해 모바일 사용자의 대역폭을 절약할 수 있다.

```html
  <img
  srcset="elva-fairy-320w.jpg, elva-fairy-480w.jpg 1.5x, elva-fairy-640w.jpg 2x"
  src="elva-fairy-640w.jpg"
  alt="요정 옷을 입은 엘바" />
```
여러 디스플레이 해상도를 지원하지만 모든 사람이 화면에서 동일한 실제 크기로 이미지를 보는 경우
브라우저는 표시되는 디스플레이의 해상도를 파악하여 srcset에 참조된 가장 적합한 이미지를 제공한다.

### picture
```html
  <picture>
  <source media="(max-width: 799px)" srcset="elva-480w-close-portrait.jpg" />
  <source media="(min-width: 800px)" srcset="elva-800w.jpg" />
  <img src="elva-800w.jpg" alt="딸 엘바를 안고 서 있는 크리스" />
</picture>
```
브라우저가 선택할 수 있는 다양한 소스를 제공할 수 있다.
picture를 지원하지 않는 브라우저를 위해 <img> 태그가 필수적이다.
