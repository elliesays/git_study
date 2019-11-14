# Day 4 학습 내용

## 이디야(Ediya) 구조설계
### head 요소
- meta : view port meta 선언 (모바일 환경)
- title : 문서의 제목 
- link : 스타일 시트 (ediya.css, animation.css)
- link : favicon.ico

### body 요소
- 헤더 (header)
- 메인 (main)
- 푸터 (footer)

### 헤더(header)
- 로고 (h1>a>span) [IR 기법을 활용하여 배경이미지로 처리]
= 메인메뉴 열기 버튼 (button>span.ir)
- 내비게이션(nav)[비순차 목록을 활용하여 메뉴 링크 마크업]
- 메인메뉴 닫기 버튼 (button>span[aria-hidden="true"])

## 메인(main)
- 숨김 제목 (h2.a11y-hidden)
```css
.a11y-hidden{
    background-color: red;
    position: absolute;
    width: 1px;
    height: 1px;
    overflow: hidden;
    clip: rect(0,0,0,0);
    clip-path: polygon(0 0, 0 0, 0 0);
  }
  ```

  - 음료 목록 (ul>ki>a[role="button"]+div[role="dialog"])
  - 음료 버튼 (a[role="button"]>figure>img+figcaption)
  - 음료 상세정보 (div[role="dialog"]>h3+p+div+button)
  - 음료 상세정보 내용 (div>dl>dt+dd)

  ### 푸터(footer)
  - 저작권 정보 (small.copyright) : \&copy;

  ## 이디야(Ediya) 레이아웃 및 디자인

  ### 헤더(header)
  - position: fixed로 레이어 형태로 배치
  - fade-slide-in-from-top 애니메이션 지정
  ``` css
@keyframes face-slide-in-from-top {
    0% {
      transform: franslateY(-4rem);
      opacity: 0;
    }
    100%{
      transform: none:
      opacity: 1;
    }
}

.app-header{
    opacity: 0;
    animation: fade-slide-in-from-top 
    0.35s 
    0.4s 
    ease-out forwards;
}
  ```
- 브랜딩 로고 및 버튼도 배치 (flex)
- 내비게이션 (position: fixed로 배치)

### 이디야 음료(main)
- 음료 레이아웃을 위해 flex 사용
- 음료 아이템 크기를 지정 40% (flex: 1 0 40%)
- 음료 아이템을 position: relative로 지정 (상세정보 기준)
- 음료 버튼(a)을 display: block으로 지정
- 가운데 정렬 (text-align: center)
- 상세정보 (position: absolute로 배치)
- 음료 성분 정보의 경우 multi column으로 2단 배치
    - column-count: 2 (2단으로 구분)
    - column-gap: 20px (단 사이의 여백)
    - column-rule: 1px solid #999 (구분선 디자인)

```css
.ediya-menu__item--multi-column {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    /* column-gap: 15px; */
    column-fill: auto;
    column-rule: 1px solid #999;
    padding: 1em 1.5em;
    background: #f8f8f8;
  }
  .ediya-menu__item--multi-column.is-2 {
    column-count: 2;
 }
 ```
