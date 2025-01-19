# Starbucks Clone Coding ☕️

스타벅스 페이지를 클론 코딩하면서 학습한 내용을 정리한 문서입니다.🥳✨

## 📚 학습 내용

### 1. `position: absolute`, `position: fixed`
- `position: absolute`와 `position: fixed`를 사용하는 경우, `display` 속성이 기본적으로 `block`으로 처리된다.
- 별도의 `display`를 지정하지 않아도 블록 레벨 요소처럼 동작한다.

---

### 2. 헤더 고정 CSS
```css
header {
  width: 100%;
  background-color: #f6f5f0;
  border-bottom: 1px solid #c8c8c8;
  position: fixed;
  top: 0;
}
```
- 헤더를 화면 상단에 고정시키는 스타일이다
- 배경색과 아래 테두리를 추가해 고정된 헤더를 구현했다


### 3. _.throttle(함수, 시간)
- Lodash의 throttle 함수는 이벤트 호출 횟수를 제한할 때 사용된다 
- 스크롤 이벤트와 같은 빈번한 이벤트를 제어하는 데 유용하다

```js
// 300ms마다 스크롤 이벤트 핸들러 실행
window.addEventListener('scroll', _.throttle(() => {
  console.log('스크롤 이벤트!>_<');
}, 300));
```

### 4. BEM (Block Element Modifier)
- CSS 클래스 네이밍 방법론으로, 가독성과 유지보수성을 높인다
  
```html
<div class="header">
  <div class="header__logo"></div>
  <div class="header__menu">
    <a href="#" class="header__menu-item header__menu-item--active">Home</a>
  </div>
</div>
```
### 5. a href="javascript:void(0)
- 클릭 이벤트를 처리하지만, 페이지 이동을 막기 위해 사용된다
```html
<a href="javascript:void(0)">Click Me</a>
```

### 6. Flexbox로 가운데 정렬
- 수평 정렬: `justify-content: center`
- 수직 정렬: `align-items: center`

```css
.container {
  display: flex;
  justify-content: center; /* 수평 정렬 */
  align-items: center;    /* 수직 정렬 */
}
```

### 7.Swiper.js
- **Swiper.js**는 터치 스와이프 기능이 포함된 슬라이드 라이브러리
- `min.js` 파일을 통해 최적화된 코드로 제공(권장)

### 8.ScrollMagic
- **ScrollMagic**은 스크롤 기반 애니메이션을 구현하기 위한 라이브러리
- CDN으로 사용 가능(권장)
```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/ScrollMagic/2.0.8/ScrollMagic.min.js"></script>
```
-------------


## 🛠️ Git convention
| Type       | Description                                                                          |
|------------|--------------------------------------------------------------------------------------|
| feat       | 새로운 기능 추가                                                                     |
| fix        | 버그 수정                                                                           |
| docs       | 문서 수정                                                                           |
| style      | 코드 스타일 변경 (코드 포매팅, 세미콜론 누락 등)                                     |
| design     | 사용자 UI 디자인 변경 (CSS 등)                                                      |
| test       | 테스트 코드, 리팩토링 (Test Code)                                                   |
| refactor   | 리팩토링 (Production Code)                                                         |
| build      | 빌드 파일 수정                                                                     |
| ci         | CI 설정 파일 수정                                                                  |
| perf       | 성능 개선                                                                          |
| chore      | 자잘한 수정이나 빌드 업데이트                                                      |
| rename     | 파일 혹은 폴더명을 수정만 한 경우                                                  |
| remove     | 파일을 삭제만 한 경우                                                              |

