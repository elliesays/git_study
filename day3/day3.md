# Day 3 학습 내용
## [CSS란?](https://developer.mozilla.org/ko/docs/Glossary/CSS)

CSS(Cascading Style Sheets, 종속형 스타일 시트)는 브라우저에서 웹페이지의 외형을 결정하는 선언형 언어입니다. 브라우저는 선택한 요소에 CSS 스타일 선언을 적용해 화면에 적절히 표현합니다. 하나의 스타일 선언은 속성과 그 값으로 이루어져 있습니다.

CSS는 HTML, JavaScript와 함께 웹의 3대 핵심 기술을 이룹니다. 보통 HTML 요소의 스타일을 결정하지만, SVG와 XML 등 다른 마크업 언어에도 사용할 수 있습니다. 하나의 CSS 규칙은 선택자에 연결된 속성 세트로 구성됩니다.

## [CSS 선택자(Selector)](https://developer.mozilla.org/ko/docs/Glossary/CSS_Selector)

- 전체 선택자(Universal selectors)
- 태그, 요소 선택자(Type selectors)
- 클래스 선택자(Class selectors)
- 아이디 선택자(ID selectors)
- 속성 선택자(Attribute selectors)
- 상태 선택자(State selectors)

## [상속(Inherit)](https://developer.mozilla.org/ko/docs/Web/CSS/inherit)

inherit CSS 값은 요소가 부모 요소로부터 속성(property)의 계산값(computed value)을 갖도록 지정되게 합니다. 모든 CSS 속성에 허용됩니다.

상속되는 속성(inherited properties)의 경우, 이는 기본 동작(behavior)을 강화하고 오직 다른 규칙을 재정의(override)해야 합니다. 상속되지 않는 속성(non-inherited properties)은, 이는 보통 비교적 거의 의미가 없는 동작을 지정하고 당신은 대신 initial 혹은 all 속성에 unset 사용을 고려할 지도 모릅니다.

상속(Inheritance)은 심지어 부모 요소가 포함(containing) 블록이 아니더라도, 항상 문서 트리 내 부모 요소로부터입니다.

## [겹침(Cascade)](https://developer.mozilla.org/ko/docs/Web/CSS/Cascade)
종속(Cascade)이란 서로 다른 원점에서 가져온 속성 여럿을 조합해 최종 결과를 도출하는 알고리즘입니다. Cascading Style Sheets라는 이름에서도 알 수 있듯 종속은 CSS의 중심입니다. 이 글은 종속이 무엇인지, 선언한 CSS 정의가 어떤 순서로 종속되는지, 그리고 여러분, 즉 웹 개발자에게 어떤 영향을 주는지 설명합니다.

| 예시      | Inline Style | ID | Class | Element |
|:---------:|:--------:|:--------:|:--------:|:--------:|
| p        | 0 | 0 |0 |1|
| .note    | 0 | 0 |0 |1|
| p.note   | 0 | 0 |0 |1|
| #outer a | 0 | 0 |0 |1|

## [박스모델(Box Model)](https://developer.mozilla.org/ko/docs/Web/CSS/CSS_Box_Model)

CSS Basic Box Model은 각 요소에 대해 시각적 서식 모델에 따라 생성하고 배치하는 사각형 박스(안팎 여백 포함)를 위한 CSS 모듈입니다.

- [display](https://developer.mozilla.org/ko/docs/Web/CSS/display)
- [box-sizing](https://developer.mozilla.org/ko/docs/Web/CSS/box-sizing)
- [width](https://developer.mozilla.org/ko/docs/Web/CSS/width)
- [height](https://developer.mozilla.org/ko/docs/Web/CSS/height)
- [margin](https://developer.mozilla.org/ko/docs/Web/CSS/margin)
- [border](https://developer.mozilla.org/ko/docs/Web/CSS/border)
- [padding](https://developer.mozilla.org/ko/docs/Web/CSS/padding)