# flex란?
컨텐츠를 정렬하거나 공간을 나눌 수 있는 CSS 속성의 집합
display 속성으로, 내부 자식 박스들의 배치에 영향을 미치는 내부 디스플레이 타입 중 하나

## flex-container에 사용하는 속성

### 주축과 정렬 방향
flex-container는 기본적으로 주축(axis)를 가지며 기본 방향은 왼쪽에서 오른쪽을 향한다.
주축이 시작하는 시작점을 flex-start, 중간을 center, 끝나는 곳을 flex-end라고 부른다.

### flex-direction
flex-container가 사용할 주축과 정렬 방향을 결정
- **row** : 주축을 행 방향으로 한다.
- **row-reverse** : 주축을 행 방향으로 하되 축의 시작점을 역전한다. 즉, flex-direction : row 였을때의 flex-start가 flex-end로 변경된다.
- **column** : 주축을 열 방향으로 한다.
- **column-reverse** : 주축을 열 방향으로 하되 축의 시작점을 역전한다. 즉, flex-direction : column 이었을때의 flex-start가 flex-end로 변경된다.

### justify-content
주축(Axis)을 기준으로 배열의 위치를 조종하거나 아이템 간의 간격을 설정할 수 있다.

### Axis와 Cross-Axis
axis가 row 상태라면 cross-axis는 column 이고, axis 가 column 이면 cross-axis는 row 인 상태이다.

### align-items, align-content
- align-items : **cross-axis를 기준으로 이동**
- align-content : flex-container의 cross-axis 축의 아이템들이 **여러 줄**일 때 사용 가능. 따라서 **두 줄의 flex-wrap:wrap인 상태에서 사용**해야 한다.

### flex-wrap
flex-container는 flex-item 넓이의 합이 컨테이너보다 클 때 강제로 flex-item의 넓이를 조절하지 않는다. **flex-wrap**은 자식요소를 감싸서 부모의 넓이에 따라 자식들을 줄바꿈하도록 해주는 기능.

### flex-flow
flex-direction과 flex-wrap은 같이 사용하는 일이 많기 때문에 flex-flow 속성을 통해 단축하여 사용할 수 있다.

## flex-item에 사용하는 속성

### flex-basis
- flex-item의 크기를 지정한다.
- width, height와 다른점은 axis 방향에 따라 달라진다는 것 그리고 내부의 컨텐츠에 따른 유연한 크기이다. 만약 flex-basis 값이 적용되어 있다면 width, height 값은 무시된다.
- 본적으로 px이나 em 등의 단위값을 사용하며, 0외에 다른 상수값을 사용할 수 없다.

### flex-grow
flex-basis의 값에서 더 늘어나도 되는지 지정하는 값으로, 할당된 값에 따라 flex-container의 남은 여백을 할당하도록 한다.
    flex-grow  : 1 → 자식 요소들이 모두 동일한 크기의 공간을 할당받는다.

    flex-grow  : 2 →  특정한 하나의 자식에게만 줄 경우 다른 자식요소보다 두배의 **여백 공간**을 할당받는다. 만약 자식요소들의 컨텐츠 크기가 존재한다면 그 컨텐츠의 넓이에 따라 할당받는 값이 달라진다.

### flex-shrink
flex-grow에 반대되는 개념으로 컨테이너의 공간이 줄어들때 flex-basis의 값에서 더 줄어들어도 되는지 지정하는 값. 크기를 고정하거나 줄이는 역할을 한다.
