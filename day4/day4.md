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
  - 저작권 정모 (small.copyright) : \&copy;
