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
|:--------|:-----:|:-----:|:-----:|:-----:|
| p        | 0 | 0 | 0 | 1 |
| .note    | 0 | 0 | 1 | 0 |
| p.note   | 0 | 0 | 1 | 1 |
| #outer a | 0 | 1 | 0 | 1 |

## [박스모델(Box Model)](https://developer.mozilla.org/ko/docs/Web/CSS/CSS_Box_Model)

CSS Basic Box Model은 각 요소에 대해 시각적 서식 모델에 따라 생성하고 배치하는 사각형 박스(안팎 여백 포함)를 위한 CSS 모듈입니다.

- [display](https://developer.mozilla.org/ko/docs/Web/CSS/display)
- [box-sizing](https://developer.mozilla.org/ko/docs/Web/CSS/box-sizing)
- [width](https://developer.mozilla.org/ko/docs/Web/CSS/width)
- [height](https://developer.mozilla.org/ko/docs/Web/CSS/height)
- [margin](https://developer.mozilla.org/ko/docs/Web/CSS/margin)
- [border](https://developer.mozilla.org/ko/docs/Web/CSS/border)
- [padding](https://developer.mozilla.org/ko/docs/Web/CSS/padding)

## [플렉스 레이아웃](https://developer.mozilla.org/en-US/docs/Glossary/Flex)

flex는 CSS display속성에 새롭게 추가 된 값입니다. inline-flex동시에 사용하는 것으로, Element (요소)에 Flex 컨테이너 가 적용됩니다. 또한 그 Element (요소)의 자식 Element (요소) 각각은 Flex 항목 이 적용됩니다. flex 항목이 적용 된 Element (요소)는 flex layout을 구성하고 CSS Flexible Box Layout Module에 정의되어있는 속성의 모든이 적용되는 것입니다.

flex속성은 flexbox 속성을 줄여서 나타낸 속성입니다. flex-grow나 flex-shrink, flex-basis 등이 있습니다.

참고 사이트 [Flex CSS Tricks](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

<!-- <div style="overflow: hidden">
  <div style="width: 50%; float: left;"><img src="./img/01-container.svg" alt=""></div>
  <div style="width: 50%; float: left"><img src="./img/02-items.svg" alt=""></div> 
</div> -->
<img src="./img/01-container.svg" alt="" width="450">
<img src="./img/02-items.svg" alt="" width="450">

## [포지션 레이아웃(Position)](https://developer.mozilla.org/ko/docs/Web/CSS/position)

position CSS 속성은 문서 상에 요소를 배치하는 방법을 지정합니다. top, right, bottom,  left 속성이 요소를 배치할 최종 위치를 결정합니다.

### 배치 유형
배치 요소는 position의 계산값이 relative, absolute, fixed, sticky 중 하나인 요소입니다. 즉 static이 아닌 요소입니다.

상대적 배치 요소는 position의 계산값이 relative인 요소입니다. top과 bottom은 원래 위치에서의 세로축 거리를, left와 right은 원래 위치에서의 가로축 거리를 지정합니다.

절대적 배치 요소는 position의 계산값이 absolute 또는 fixed인 요소입니다. top, right, bottom, left는 요소 컨테이닝 블록 모서리로부터의 거리를 지정합니다. 요소가 바깥 여백을 가진다면 거리에 더합니다.

끈끈한 배치 요소는 position의 계산값이 sticky인 요소입니다. 상대적 배치 요소로 동작하다가 컨테이닝 블록이 플로우 루트flow root(또는 스크롤 중인 컨테이너)의 임계값을 넘으면, 컨테이닝 블록의 반대편 모서리를 만날 때까지 "부착"됩니다.

- position: static  
기본값입니다. static이 지정된 요소는 document의 일반적인 흐름(normal flow)을 따라 배치됩니다. top, right, bottom, left, z-index 속성들이 static에서는 아무런 효과도 주지 못합니다. 

- position: relative    
relative가 지정된 요소 역시 document의 일반적인 흐름(normal flow)을 따라 배치됩니다. 그리고 요소 자신에 대한 상대적인 top, right, bottom, left 속성에 의한 좌표로 배치됩니다. (relative는 별도의 거리 속성을 주지 않으면 static과 동일하게 동작합니다.)이때 요소의 좌표는 다른 요소들의 위치에 영향을 주지 않습니다. 따라서, 페이지 레이아웃에서 요소에게 지정된 공간은 static일 때와 동일합니다. relative는 z-index의 값이 auto가 아닐 경우에 새로운 stacking context를 만듭니다. table-*-group, table-row, table-column, table-cell, table-caption 요소에 relative가 주는 효과는 정의되지 않았습니다.

- position: absolute   
요소가 일반적인 문서(document) 흐름에서 제거됩니다. 페이지 레이아웃에서 요소에 대한 공간이 생성되지 않습니다. 대신, 가장 가까운 위치에있는 조상에 대해 상대적 위치로 배치됩니다. 그렇지 않으면 초기 컨테이닝 블록을 기준으로 배치됩니다. 최종 위치는 top, right, bottom, left 값에 의해 결정됩니다. 이 값은 z-index가 auto가 아닌 경우에 새로운 stacking context를 생성합니다. 절대적으로 배치된(positioned) 박스(box)들은 마진을 가질 수 있으며 다른 마진에 의해 망가지지 않습니다.  

- position: fixed    
요소가 일반적인 문서(document) 흐름에서 제거됩니다. 페이지 레이아웃에서 요소에 대한 공간이 생성되지 않습니다. 대신, 스크린의 '뷰포트(viewport)를 기준으로 한 위치'에 배치됩니다. 따라서 스크롤되어도 움직이지 않는 고정된 자리를 갖게 됩니다. top, right, bottom, left 값에 의해 최종 위치가 결정됩니다. 이 값은 항상 새로운 stacking context를 생성합니다. 조상의 transform 속성이 none이 아닌 다른 것으로 설정되면, 그 조상은 뷰포트 대신에 컨테이너로 사용됩니다(CSS Transforms Spec). 인쇄된 문서(document)의 경우, 모든 페이지에서 요소가 동일한 위치에 배치됩니다.  

- position: sticky   
요소가 일반적인 문서(document) 흐름에 따라 배치됩니다. 그런 다음 top, right, bottom, left 값을 기준으로 플로우 루트(flow root) 및 해당 요소를 포함하는 블록(containing block)에 대한 상대적(relative) 위치에 자리하게 됩니다. 이 오프셋은 다른 요소들에 영향을 주지 않습니다. 이 값은 항상 새로운  stacking context를 생성합니다. 테이블과 관련된 요소들에 미치는 sticky의 효과는 relative와 동일합니다. 브라우저 사양에 따라 overflow : hidden 또는 auto 요소 내에서 작동하지 않을 수 있습니다.