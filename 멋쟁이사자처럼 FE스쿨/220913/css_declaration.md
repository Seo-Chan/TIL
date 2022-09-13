## 절대 길이 단위란?

    사용자가 선언한 고정된 크기 그대로를 화면에 그리기 때문에 직관적으로 사용 가능
     ex) cm, mm, px 등이 있지만 cm,mm은 거의 쓰지 않음.
```
  📝h1과 p 의 기본단위

    h1의 기본px: 32px
    
    p의 기본px: 16px
```

## 상대 길이 단위란?

    배수 단위, 부모 요소의 글자크기 등 특정한 대상을 기준삼아 상대적으로 font-size가 결정 됨.
     ex) em, %, rem, vw, vh 등

### em
    상대 길이 단위로 배수를 나타내는 단위이며, 부모의 font-size에 따라 기준점을 세움.

```html
        <style>
            /* 128이라는 숫자는 어떻게? */
            div {
                font-size: 2em;
            }
        </style>
    </head>
    <body>
        <!-- 16px -->
        16px입니다.
        <div>
            <!-- 부모 body의 크기인 16px에 div의 크기인 2를 곱한다. -->
            32px입니다.
            <div>
                <!-- 부모 body의 크기인 32px에 div의 크기인 2를 곱한다. -->
                64px입니다.
                <div>
                    <!-- 부모 body의 크기인 64px에 div의 크기인 2를 곱한다. -->
                    128px입니다.
                </div>
            </div>
        </div>
    </body>
```

### rem

    rem의 r은 root(최상위)를 의미
    최상위 태그에 지정한것을 기준으로 삼으며, 보통 최상위 태그는 html

```html
        <style>
            /* 64px 이라는 숫자는 어떻게? */
            /* rem은 html의 폰트사이즈를 기준으로 정해짐. */
            html {
                font-size: 32px;
            }
            div {
                font-size: 2rem;
            }
        </style>
    </head>
    <body>
        <div>
            <div>
                <div>
                    <!-- 최상위 태그 html의 크기인 32px에 div의 크기인 2를 곱한다. -->
                    64px입니다.
                </div>
            </div>
        </div>
    </body>
```

`기본적으로 rem을 많이 쓰고 ex) 버튼(large, medium, small) 등에 텍스트의 비율에 따라 달라져야 할 경우 em을 사용`

### vmin & vmax

    v는 view port를 의미
    화면의 짧은 쪽을 100으로 나눈것이 vmin, 긴 쪽을 100으로 나눈것이 vmax

## overflow

    overflow 속성은 요소의 콘텐츠가 너무 커다랄 경우 요소를 어떻게 처리할지 지정함.
    Overflow-x Overflow-y 의 축 별로 값을 설정할 수 있음.

### overflow의 주요 속성

    1. visible: overflow 속성의 기본 값 (콘텐츠를 자르지 않음.)

    2. hidden: 콘텐츠를 요소의 크기만큼 잘라냄(흘러 넘치는 것을 자름), 스크롤바를 제공하지 않음

    3. scroll: 콘첸츠를 요소의 크기만큼 맞추기 위해 잘라내는데 스크롤바를 제공


## background-image

    background-image 는 width와 height값이 없으면 출력되지 않음 그러나 body의 경우 background-image에 width 와 height값을 주지 않아도 배경이미지가 출력 됨.

```
    📝cover와 contain의 차이

    contain: 이미지가 잘리거나 찌그러지지 않는 한도 내에서 제일 크게 만듦

    cover: 이미지가 찌그러지지 않는 한도 내에서 제일 크게 만듦 (잘릴수도 있음)
```

### 그외의 속성

    repeat : 반복

    repeat-x : x축만 반복

    repeat-y : y축만 반복

    no-repeat : 반복하지 않음

    round : 이미지가 짤리지 않게, 이미지 크기 변화를 줘서 간격 없이 반복

    space : 이미지가 짤리지 않게, 이미지크기는 유지한채로 간격을 줘서 반복

## font

    text-transform: 텍스트를 대문자나 소문자로 표현할 수 있음
    uppercase는 대문자, lowercase는 소문자, capitalize는 각 단어의 첫 글자를 대문자로 지정

    font-style: 텍스트를 기울기 글꼴로 표현할 수 있음.
    normal은 일반 스타일, italic은 필기체, oblique는 기울임체

    text-align: 텍스트의 정렬을 표현.
    left는 왼쪽, right는 오른쪽, center는 가운데, justify는 마지막 줄을 제외하고 양쪽으로 정렬

    text-decoration: 텍스트의 장식을 설정할 수 있다. none은 효과제거, underline은 밑줄추가

## opacity
    요소의 투명도 지정
    투명도가 들어간 요소의 내용물도 함께 투명해짐
    0.0 과 1 사이의 숫자 지정할 수 있다.