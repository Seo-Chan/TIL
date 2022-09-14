# Text

## line-height
글자 라인의 높이를 지정해 텍스트 라인과 라인 사이의 간격을 조정할 때 사용.

line-height를 주면 마치 padding값이 들어간 것 처럼 화면에 출력이 되는데 실제로는 padding값이 아니라 line-height 값임.

### line-height의 단위

    1. normal: 기본단위. 폰트종류에 따라 line-height가 달라진다

    2. number: 숫자로 값을 설정하며, 폰트 사이즈를 기준으로 달라진다
    ex ) number가 1이라면 leading area가 사라짐. font-size 그 자체가 된다.
         number가 2라면 font-size의 두배가 됨.

    3. px: 고정된 값을 적용하며 폰트의 사이즈가 변하면 대비하지 못하기 때문에 잘 사용하지 않음

    4. em: 부모 요소의 font-size에 비례한 값을 적용함. px과 마찬가지로 요소의 폰트사이즈가 변하면 대비 불가

    5. %: 요소 자신의 폰트 사이즈를 기준으로 값을 설정함

` 📝leading area->> lead: 납 이라는뜻`

## letter-spacing
글자 사이의 간격을 조절

## text-decoration
텍스트에 붙는 라인을 꾸며주는 속성, 주로 a태그 밑줄을 없앨때 활용

## text-align
블록레벨안의 인라인요소들을 정리할 때 사용

한줄짜리 문장을 수직 정렬하고 싶을 때 line-height를 설정할 수도 있다 (height값이랑 동일하게 설정) <br>
but 폰트의 여백범위에 따라서 수직 정렬처럼 안보일 수도 있다 (그럴 땐 margin값 사용해서 조절)

```
📝버튼은 수직정렬 굳이 해줄 필요 없음. 높이값만 줘도 자동으로 수직정렬된다.
  버튼에 `width`랑 `height`값을 준 것과 `padding` 값을 준 것의 차이: 컨텐츠박스가 늘어나는가, 컨텐츠박스 외의 패딩이 늘어나는가
  패딩값을 주면 컨텐츠 크기만큼 가로로 길게 늘어나고 width값을 지정하면 밑으로 내려감
```

## vertical-align
**인라인 요소**의 수직 정렬을 맞추기 위해 사용하는 속성
    
    1. baseline : 베이스라인을 부모의 베이스 라인에 맞추어 정렬

    2. sub: 베이스라인을 부모의 subscript(아래첨자)-baseline 에 맞추어 정렬

    3. super : 베이스라인을 부모의 superscript(윗첨자)-baseline에 맞추어 정렬

    4. top: 상단의 위치를 라인(인라인 박스를 감싸고 있는 공간)의 상단으로 정렬 

    5. text-top: 상단의 위치를 부모 엘리먼트 폰트의 상단으로 정렬

    6. bottom: 하단의 위치를 전체 라인의 하단으로 정렬

    7. text-bottom: 하단의 위치를 부모 엘리먼트 폰트의 하단으로 정렬

    8. middle : 폰트의 중간 위치를 부모의 baseline + x-height의 절반에 해당하는 위치로 정렬. 즉, 수직의 정가운데가 아님..

## text-indent
들여쓰기 공간 설정

## text-overflow
부모 컨테이너를 넘어간 컨텐츠가 어떻게 보여질지 결정하는 속성
- clip : 기본값. 컨테이너의 끝에서 텍스트를 자른다.
- ellipsis : 잘린 텍스트를 `말줄임` 표시로 나타낸다.
 
### 말줄임
text-overflow:ellipsis;
화면 크기 줄일때 말줄임 설정