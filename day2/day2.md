# Day 2 학습 내용
## HTML 기본
Hyper Text Markup Language 약자로 웹 문서를 제작할 때 사용하는 언어이다.
그리고 마크업은 구조를 설계하는 언어로 콘텐츠 관점에서 시맨틱 하게 작성하는 것이 필요하다.
HTML 언어를 학습할 때 알아야 할 기본 용어는 다음과 같다.
- 요소 : Element
- 시작 태그 : Open Tag
- 종료 태그 : Close Tag
- 속성 : attribute
- 값 : value

## 표준모드와 호환 모드
문서 유형 정의(Document Type Definition)를 말하며 브라우저의 렌더링 모드를 표준으로 작동하게 만들어 줍니다. DTD는 HTML 문서의 반드시 최상 위에 위치해야 합니다.

## 제목 및 단락 요소
사용자가 가장 먼저 읽는 콘텐츠는 제목(Heading Level 1-6)입니다. 제목은

## 피겨 및 이미지
HTML 문서에 연겨되어 화면에 표시되는 이미지 요소와 동영상, 차트, 표, 이미지 등을 캡션과 함께 묶어주는 요소가 피규어(fIqure) 입니다. 참고로 alt 속성을 잘 설정해두면, 시각 장앵ㄴ이 아니더라도 도움을 받을 수 있습니다. 이미지 링크가 깨질 경우, 화면에 alt 속성 값이 출력 디어 어떤 이미지 였는지 정보를 제공할 수 있습니다. alt 속성은 바로 이미지를 볼 수 없는 환경에서 이미지를 대체할 수 있는 정보이기 때문입니다.
- 이미지 삽입 예시  
![From A to Z Zucchini](./img/logo.gif)
- src 속성 : 이미지 파일
- alt 속성 : 대체 텍스트
- width/height 속성: 이미지의 가로 및 세로 크기

#목록과 하이퍼링크
HTML 문서 작성 시, 목록은 매우 빈번하게 사용 되는 요소들 입니다. 비순차 모록(Unordered List), 순차 목록(Ordered List)에 대해 정리해보는 시간을 가져봅시다.

HTML unordered list 요소 (ul) 는 리스트에서의 순서가 의미없는, 숫자 순서를 가지고 있지 않은, 정렬되지 않은 항목들의 리스트를 나타냅니다. 일반적으로, 정렬되지않은 리스트의 항목들은 굵은 점과 함께 표시됩니다.

HTML ol 요소는 정렬된 리스트의 항목들을 나타냅니다. 일반적으로, 정렬된 리스트의 항목들은 앞에 번호와 함께 표시되며, 이 번호는 순자,문자,로마 숫자,간단한 점과 같이 어떤 형태로든 나타날수 있습니다.

HTML List item 요소 (li) 는 리스트 항목을 나타낼때 사용됩니다. 이 요소는 자신이 리스트에서 하나의 개체를 나타내는 정렬된 리스트(ol), 정렬되지 않은 리스트(ul), 메뉴(menu) 에 포함되어야 합니다. 메뉴와 정렬되지 않은 리스트에서, 리스트 항목들은 일반적으로 글머리 기호와 함께 표시됩니다. 정렬된 리스트에서는,  숫자나 글자가 내림차순으로 왼쪽에 같이 표시됩니다.

HTML a 요소 (앵커 요소)는 다른 페이지, 파일, 같은 페이지의 어느 위치, 이메일 주소나 그 외 다른 URL로 연결할 수 있는 하이퍼링크를 만듭니다.

- ul 비순차 목록 요소 [MDN ul요소](https://developer.mozilla.org/ko/docs/Web/HTML/Element/ul)
- ol 순차 목록 요소  [MDN ol요소](https://developer.mozilla.org/ko/docs/Web/HTML/Element/ol)
- li 목록 항목 요소 [MDN li요소](https://developer.mozilla.org/ko/docs/Web/HTML/Element/li)
- a 하이퍼링크 요소 [MDN a요소](https://developer.mozilla.org/ko/docs/Web/HTML/Element/a)