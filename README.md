# CSS Layout Master

display: block

- 한 줄 차지
- width는 기본 값으로 100%를 가짐

display: flex

- 자식이 사용하는 프로퍼티: align-self, order, flex-grow, flex-shrink, flex-basis
- order default 0, 이 값 순서대로 나열됨
- flex box는 아이템을 한 줄로 유지함, 너비값을 바꿔서라도
- flex-wrap의 nowrap은 너비 유지안함, wrap은 너비 유지함
- flex-wrap 사용 시 단일 행에서 여러 행으로 바뀐 경우, align-content로 위치 수정
- flex-grow default 0, flex-shrink default 1, flex-basis default 200px
- flex-basis는 flex-grow와 flex-shrink가 동작하기 위한 기준이 되는 놈으로 row일 땐 기준너비가 되고, column일 땐 기준높이가 된다.
- flex-grow는 여백이 생기면 그 여백을 얼마만큼씩 분배할 것인지를 의미함
- flex-shrink는 기준너비보다 작아질 때 누구를 더 줄일지를 결정함

display: grid

- grid-template-columns, grid-template-rows, repeat()
- grid-template-areas, grid-area
- grid-template-areas는 grid-area로 명명된 이름으로 영역을 지정할 수 있음
- grid-template-areas로 영역 지정 시에는 사각형 모양이어야함(?)
- grid-column-start, grid-colum-end
- grid-row-start, grid-row-end
- shortcut grid-row, grid-column
- grid-row: 1 / 4, grid-row: 1 / -1, grid-row: 1 / span 3, grid-row: span 2
  1 2 3 | -3 -2 -1
  2     | -2
  1     | -1
- row-gap, column-gap, gap
