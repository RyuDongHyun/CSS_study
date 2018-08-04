### ADVANCED CSS GRID

### Grid Template Areas

: 키워드로 각 위치를 지정할 수 있다.

```css
.container {
  display: grid;
  max-width: 900px;
  position: relative;
  margin: auto;
  
  /*4줄 2칸을 만들어 총 8개의 칸이 있는 격자를 만들고 */
  grid-template-rows: 300px 120px 800px 120px;
  grid-template-columns: 1fr 3fr; 
  
 /* 각각의 위치를 키워드로 지정함 */   
  grid-template-areas: "head head"
                       "nav nav" 
                       "info services"
                       "footer footer";
}

/* keword로 grid-area설정 */
header {
  grid-area: head;
} 

nav {
  grid-area: nav;
} 

.info {
  grid-area: info;
} 

.services {
  grid-area: services;
}

footer {
  grid-area: footer;
}


```



### Overlapping Elements

: 각 요소들이 겹쳤을 때 어떤 항목을 위로 올릴지 결정

```css
img {
  grid-area: 2 / 3 / 5 / 5;
  z-index: 5;
  /* z-index 항목을 추가해서 우선순위를 정할수 있다. */
}
```

 

### Justify Items

: 각 grid 안에 들어있는 Item들을 가로로 정렬하기

- `justify-items: (keyword)` 

  

### Justify Content

: gird 자체를 가로로 정렬하기

- `justify-content: (keyword)`



### Align Items

: 각 grid 안에 들어있는 Item들을 가로로 정렬하기 

- `align-items: (keyword)`



### Align Content

: gird 자체를 세로로 정렬하기

- `align-content: (keyword)`



예를들어 hwp(한글문서)에서 표를 만들면

표 안에 있는 내용들 => item, 표 => content라고 하면

가로 정렬시에는 justify, 세로 정렬시에는 align을 한다고 생각하면 됨.



### Justify Self and Align Self

: 위에 내용이 셀 전체 선택이라고 한다면 이건 셀 한개 선택후 설정

- `justify-self: (keyword)`
- `align-self: (keyword)` 



### Implicit vs. Explicit Grid



### Grid Auto Rows and Grid Auto Columns



### Grid Auto Flow





