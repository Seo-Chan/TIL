# 텍스트 레벨 요소

## `<a>`태그
- 하이퍼 텍스트 즉, 링크를 만들 때 사용하는 태그
- 배(사용자)가 정박할 수 있도록 좌표(주소 혹은 URL)를 가리키는 닻(anchor)의 역할을 하는 태그

### `<a>`태그의 속성
>- href: 이동시켜 줄 페이지의 경로를 담는 속성<br>
>- title: 경로에 대한 설명을 작성하여 툴팁이 나오는 속성<br>
>- target: 이동시켜 줄 페이지가 뜨는 위치를 지정하는 속성
>>- _self: 현재 창에서 변경하는 속성<br>
>>- _blank: 새 창 혹은 새 탭에서 열리는 속성<br>
>>- _parent: 아이프레임 페이지에서 부모가 되는 창에서 변경<br>
>>- _name: 특정 아이프레임에서 연결<br>
>>- _top: 최상단 브라우저에 표시. 부모 창이 없는 경우 _self와 같은 동작

### `<a>`태그의 종류와 예시
```html
<a href="https://www.naver.com">click</a>
<a href="https://www.naver.com" target="_blank">click</a>
<a href="./index.html">click</a>
<a href="#three">click</a> <!-- 해쉬 링크. 페이지 내부에서 이동 -->
<a href="./index.html" download>click</a>
<br>
<a href="./hello.hwp">hwp click</a>
<br>
<a href="./hello.hwp" download="a.hwp">hwp download click</a>
<br>
<a href="./hello.pdf">pdf click</a>
<br>
<a href="./hello.pdf" download="a.pdf">pdf download click</a>
<a href="tel:+82020000000">(02)000-0000</a> /
<a href="mailto:hello@gmail.com">hello@gmail.com</a>
```
## 그 외의 태그
- `<br>`: 줄바꿈<br>
- `<wbr>`: 텍스트 박스에서 한 줄로 모두 표시가 안될 때에만 줄바꿈<br>
- `<strong>`: 굵은 글꼴에 중요도를 더해 강조할 때 사용<br>
- `<i>`: 기울임 글꼴. HTML5에서는 전문 용어, 문단에서 주 언어와 다른 언어로 표현된 부분(주 언어가 한글이지만 영어로 표기되었을 경우), 소설이라면 등장인물의 생각이 표기되어 있는 부분 등 어떤 이유로 주위와 구분해야 하는 부분을 표현하기 위해 사용<br>
- `<em>`: 같은 기울임 글꼴이지만 강조의 의미<br>
- `<dfn>`: 현재 문맥에서 정의하고 있는 용어. dfn의 가장 가까운 부모가 `<p>` 혹은 `<dt><dd>` 쌍, `<section>` 요소일 경우 그 컨텐츠를 dfn의 정의에 대한 설명으로 간주하며 문서에서 최초로 나타났을 때 사용
- `<abbr>`: 준말, 약자를 나타내고 싶을 때 사용
- `<sup>`: 윗첨자
- `<sub>`: 아랫첨자
- `<span>`: 별다른 의미 없이 보통 줄 바꿈 없이 영역을 묶는 용도로 사용<br>
  `<div>`와의 차이점은 줄바꿈이 되지 않는다는 것