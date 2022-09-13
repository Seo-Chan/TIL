# Text

## line-height

    글자 라인의 높이를 지정해 텍스트 라인과 라인 사이의 간격을 조정할 때 사용.

    참고로 line-height를 주면 마치 padding값이 들어간 것 처럼 화면에 출력이 되는데 실제로는 padding값이 아니라 line-height 값임.

### line-height의 단위

    1. normal: 기본단위

    2. number: 숫자로 값을 설정하며, 폰트 사이즈를 기준으로 달라짐
    ex ) number가 2라면 font-size의 두배가 됨.

    3. px: 고정된 값을 적용하며 폰트의 사이즈가 변하면 대비하지 못하기 때문에 잘 사용하지 않음

    4. em: 부모 요소의 font-size에 비례한 값을 적용함. px과 마찬가지로 요소의 폰트사이즈가 변하면 대비 불가

    5. %: 요소 자신의 폰트 사이즈를 기준으로 값을 설정함

## letter-spacing

    글자 사이의 간격을 조절

## text-decoration

    텍스트에 붙는 라인을 꾸며주는 속성, 주로 a태그 밑줄을 없앨때 활용
