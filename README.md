# CSS Layout Master
## display: block
- 한 줄 차지
- width | (default) auto
- height | (default) auto
- width는 뷰포트 너비를 기준으로 잡지만, height는 끝이 없다(?)
## display: flex
- flex box는 아이템을 한 줄로 유지함, 너비값을 바꿔서라도
### flex 부모 속성
- flex-direction
- flex-wrap
  - flex-wrap의 nowrap은 너비 유지안함, wrap은 너비 유지하면서 다음 줄로 넘김
- justify-content
  - 열 단위 이동
- align-content
  - 행 단위 이동
  - 높이가 존재해야함
  - flex-wrap default 값이 nowrap이기 때문에 강제로 한줄로 유지되는 형태라 align-content로 변경 안됨
  - flex-wrap 사용 시 단일 행에서 여러 행으로 바뀐 경우, align-content로 위치 수정
- align-items
  - 아이템들의 위치 수정
### flex 자식 속성
- align-self
  - 단일 아이템의 위치 수정
- flex-grow
  - (default) 0
  - flex-grow는 여백이 생기면 그 여백을 얼마만큼씩 분배할 것인지를 의미함
- flex-shrink
  - (default) 1
  - flex-shrink는 기준너비보다 작아질 때 누구를 더 줄일지를 결정함
- flex-basis
  - (default) 200px
  - flex-basis는 flex-grow와 flex-shrink가 동작하기 위한 기준이 되는 놈으로 row일 땐 기준너비가 되고, column일 땐 기준높이가 됨
- flex
  - (shortcut) flex-grow | flex-shrink | flex-basis
- order
  - (default) 0, 이 값 순서대로 나열됨

![image](https://user-images.githubusercontent.com/75672249/139773858-a564217a-5fda-47b8-b558-be600151692d.png)

## display: grid
### grid 부모 속성
- grid-template-columns
- grid-template-rows
- grid-template-areas
  - grid-area로 명명된 이름으로 영역을 지정할 수 있음
  - 영역 지정 시에는 사각형 모양이어야함(?)
- grid-template:  
    'header header header header' 1fr  
    'content content content nav' 2fr  
    'footer footer footer footer' 1fr / 1fr 1fr 1fr 1fr ;
  - grid-template에는 repeat() 적용 안됨
  - (shortcut) grid-template-rows / grid-template-columns
- justify-content
- align-content
- place-content
  - (shortcut) justify-content | align-content  
- justify-items
- align-items
- place-items
  - (shortcut) justify-items | align-items 
- row-gap
- column-gap
- gap
  - (shortcut) row-gap | column-gap
- grid-auto-rows
  - 개수를 정해둔 행보다 더 많을 경우 자동으로 추가되는 행의 크기
- grid-auto-columns
  - 개수를 정해둔 열보다 더 많을 경우 자동으로 추가되는 열의 크기
- grid-auto-flow
  - (defalut) row
  - 개수를 정해둔 열과 행보다 더 많은 열과 행이 필요할 때 row일 경우 행을 추가하고, column일 경우 열을 추가함 
### grid 자식 속성
- grid-row-start
- grid-row-end
- grid-row
  - (shortcut) grid-row-start / grid-row-end
- grid-column-start
- grid-colum-end
- grid-column
  - (shortcut) grid-column-start / grid-column-end
- grid-area
  - (shortcut) grid-row-start / grid-column-start / grid-row-end / grid-column-end
- order
  
|1|2|3|4|
|:---:|:---:|:---:|:---:|
|2||||
|3|||
|4|||

|-4|-3|-2|-1|
|:---:|:---:|:---:|:---:|
|-3||||
|-2|||
|-1|||

- justify-self
- align-self
- place-self
  - (shortcut) justify-self / align-self
### etc
- fr = fraction(분수), 사용 가능한 공간, 1fr
- 내용물이 글자뿐이면 글자의 width, height을 가짐
- repeat()
  - auto-fill 여백의 빈 공간을 남겨둠
  - auto-fit 여백을 다 채움
- minmax()
- max-content, min-content
