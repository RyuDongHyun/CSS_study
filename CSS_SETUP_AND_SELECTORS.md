# CSS SETUP AND SELECTORS

### Intro to CSS

: 웹페이지의 뼈대가 html이라면 옷이 바로 CSS



### Inline Styles

: html 파일 안에 태그에 바로 style주는 방식

```html 
<p style="color: red;">I'm learning to code!</p>
```



### The `<style>` Tag

: html파일 head 부분에 style을 따로 모아서 쓰는 방식

```html
<head>
  <style>
    p {
      color: red;
      font-size: 20px;
    }
  </style>
</head>
```



### .css file

: html 파일에 다른 코드들을 쓰면 보기 불편, 수정 불편, 프로 불편러가 됨.

: .css파일을 따로 만들고 링크로 불러오는 방식 선호



### Linking the CSS File

: css파일을 따로 만들고나서 html파일과 연결을 안해주면 무용지물

: `<link>`  태그 사용

- `href` : 파일의 위치에 따라 다름. url이 될수도 있고 파일이 있는 폴더로 경로지정할 수도 있음.
- `type` : `text/css` 로 지정
- `rel` `stylesheet` 로 지정

ex)

```html
<link href="style.css" type="text/css" rel="stylesheet">
```

보통 예시와 같이 씀. .css파일을 폴더에 넣고 경로지정해서 불러오는 방식



### Tag Name

: tag 단위로 style주기.

```css
p {
  font-family: Arial;
}
```



### Class Name

: class로 만들어 사용

: 여러 태그에 동일한 style을 주고 싶을 때 따로 만들어 저장 후 사용

```html
<p class="brand">Sole Shoe Company</p>
```

```css
.brand {
	font-family: Arial;
}
/* class를 만들 때는 . 으로  */
```

=> Sole Shoe Company의 폰트가 Arial로 나옴.



### Multiple Class

: 한 태그에 여러개의 style을 줄 수도 있음.

- 다음과 같이 클래스를 만들고

```css
.green {
  color: green;
}

.bold {
  font-weight: bold;
}
```

- 아래와 같이 띄어쓰기로 여러개 추가할 수 있음.

```html
<h1 class="green bold"> ... </h1>
```



### ID Name

:특정 태그에 style을 주고 싶을 때 사용

- 해당 태그에 id를 주고

```html
<h1 id="large-title"> ... </h1>
```

- .css 파일에서 해당 id에 대한 style을 만든다.

```css
#large-title {
	/* id는 #을 사용!!*/
}
```



### Specificity

: html파일이 css파일을 바탕으로 style을 줄 때 우선순위가 있음

: 태그 < 클래스 < id

```html
<h1 class="headline">Breaking News</h1>
```

```css
h1 {
  color: red;
}

.headline {
  color: blue;
}
```

=> 태그보다 클래스의 우선순위가 더 높기 때문에 Breaking News는 파란색으로 보인다.



### Chaining Selectors

: 특정 태그안에 클래스를 주고 싶을 때 사용

```html
h1.special {

}
```

=> .special이라는 클래스는 h1태그만 사용할 수 있는 클래스



### Nested Elements

: 중첩해서 style을 주고 싶을 때 사용

- main-list라고 하는 style을 `<li></li>` 태그에 모두 주고 싶을 때

```html
<ul class='main-list'> <!--상위 태그에 style을 주고-->
  <li> ... </li>
  <li> ... </li>
  <li> ... </li>
</ul>
```

```css
.main-list li {

}
/* 다음과 같이 작성해준다.*/
```



### Chaining and Specificity

: 특정 태그에 클래스를 주었을 때

```css
p {
  color: blue;
}


.main p {
  color: red;
}
```

=> .main 클래스 안에 있는 p태그만 빨간색, 그 외의 p태그에는 파란색으로 보인다.



### Important

: 잘 사용하지 않는 기능. 해당 style을 최우선순위로 설정.

```css
p {
  color: blue !important;
}

.main p {
  color: red;
}
```

=> style 우선순위로 보면 .main안에 있는 태그는 빨간색이여야 하나

파란색으로 최우선순위 style이 정해져 있기 때문에 모든 p태그가 파란색으로 고정



### Multiple Selectors

: , 로 중복된 코드를 한번에 쓸수 있음.

```css
h1 {
  font-family: Georgia;
}

.menu {
  font-family: Georgia;
}
```

위 코드에서 `font-family: Georgia;`  가 두번 반복되는데

```css
h1, 
.menu {
  font-family: Georgia;
}
/* ,로 한번에 쓸수 있음.*/
```







