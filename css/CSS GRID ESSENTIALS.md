# CSS GRID ESSENTIALS

### Creating a Grid

: grid(격자) 생성을 위한 grid container(parent), grid items(children) 설정

- grid container의 display 속성을 grid로 설정해야 함.



### Creating Columns

```css
.grid {
  display: grid;
  width: 100px;
  grid-template-columns: 20px 40% 60px;
}
/* column이 3개, 1번째: 20px, 2번째: 40%, 3번재 60px */
```



### Creating Rows

```css
.grid {
  display: grid;
  width: 1000px;
  height: 500px;
  grid-template-columns: 100px 200px;
  grid-template-rows: 10% 20% 600px;
}
/* row설정, 1번째row: 10%, 2번째row: 20%, 3번째row: 600px*/
```



### Grid Template

: column과 row를 한줄로

```css
.grid {
  display: grid;
  width: 1000px;
  height: 500px;
  grid-template: 200px 300px / 20% 10% 70%;
}

/* / 앞부분 row, / 뒷부분 column */
```



### Fraction

: `fr` , CSS Grid에서 사용하는 단위

```css
.grid {
  display: grid;
  width: 1000px;
  height: 400px;
  grid-template: 2fr 1fr 1fr / 1fr 3fr 1fr;
}
/* 높이와 너비의 픽셀을 정하고 쪼개서 나눠가지는 형태 */
```



### Repeat

: column과 row의 속성을 정하는 함수중 하나

: `repeat()`

```css
.grid {
  display: grid;
  width: 300px;
  grid-template-columns: repeat(3, 100px);
}
/* column 3개를 100px width로 */
```



### minmax

: 화면에 크기가 커지거나 작아졌을때의 min값과 max값 설정

```css
.grid {
  display: grid;
  grid-template-columns: 100px minmax(100px, 500px) 100px;
}
/* width항목을 지우고 설정 */
```



### Grid Gap

: 각 item 사이의 거리 설정

```css
.grid {
  display: grid;
  width: 320px;
  grid-template-columns: repeat(3, 1fr);
  grid-column-gap: 10px;
}
/* column 사이의 gap을 10px로 */
/* grid-row-gap: 5px; (row 사이의 거리를 5px로 )*/
/* 두 줄을 한 번에*/
/* grid-gap: 10px 5px; */
```





### Multiple Row Items

: `grid-row-start`, `grid-row-end` 사용

: grid row 나 column의 끝을 지정할 때는 항상 그 자리값보다 1 크게 설정

```css
.item {
  grid-row-start: 4;
  grid-row-end: 6;
}

/* Refactoring */
.item {
  grid-row: 4 / 6;
}
```



: `span` 키워드를 사용하면 시작위치나 끝 위치 중 하나를 설정하고 얼마나 차지할지 설정 가능

```css
.item {
  grid-column-start: 4;
  grid-column-end: span 2;
}
```



### Grid Area

: row와 column을 한 줄에

```css
.item {
  grid-area: 2 / 3 / 4 / span 5;
}
/* 2 : grid-row-start */
/* 3 : grid-column-start */
/* 4 : grid-row-end */
/* span 5 : grid-column-end */
```

