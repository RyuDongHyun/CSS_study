# CSS TYPOGRAPHY

### Font Family

: 폰트 모양

```css
h1 {
    font-family: Garamond;
}
/* h1태그의 폰트(글자)모양은 Garamond로 */
```

1.  폰트 파일이 컴퓨터에 설치되어있어야 함.
2. Default값 : Times New Roman
3. 웹페이지 상에는 2~3개의 폰트모양을 추천
4. 폰트 이름이 두글자 이상일 때는 양 끝에 `"font name"` 와 같이 쌍따옴표로 닫아준다.



### Font Weight

: 폰트(글자) 두께

1. 키워드로 설정(bold / normal)

```css
p {
    font-weight: bold;
}
/*폰트(글자)를 두껍게*/
/*보통 두께는 font-weight: normal;*/
```

2. 숫자로 설정(100~900 / 100단위로)

```css
p {
    font-weight: 800;
}
/* 400 == default(normal) */
/* 700 == bold */
/* 300 == light*/
```



### Font Style

: italic(기울여쓰기) / default(normal)

```css
h3 {
    font-style: italic;
}
/* h3태그는 글자 기울임 */
```



### Word Spacing

: 단어 간격, 가독성을 높일 수 있음.

```css
h1 {
    word-spacing: 0.3em;
}
/* 0.25em == default*/
```



### Letter Spacing

: 각각 글자의 간격(kerning)

```css
h1 {
    letter-spacing: 0.3em;
}
```



### Text Transformation

: 대문자로 또는 소문자로

```css
h1 {
    text-transform: uppercase;
}
/* h1태그를 모두 대문자로 */
```



### Text Alignment

: 글자 정렬

```css
h1 {
    text-align: right;
}
/* h1태그를 모두 오른쪽으로 정렬 */
/* left : 왼쪽 정렬 */
/* center : 중앙정렬 */
/* right : 오른쪽 정렬 */
```



### Line Height

: 줄 높이, 가독성을 높이기 위해 가끔 사용

```css
p {
    line-height: 1.4;
}
/* 숫자 : 줄 높이가 비율로 정해져 자동으로 바뀜*/
/* 픽셀 : 예를들어 12px로 정하면 화면이 작아져도 크기는 12px로 고정*/
```

- 숫자로 설정하는 것을 선호. 반응형(화면크기에 따라 상대적으로 변함)이기 때문.



### Fallback Fonts

: 이미 설치된(내장된) 폰트

```css
h1 {
    font-family: "Garamond", "Times", serif;
}
/* h1태그의 폰트는 Garamond로 */
/* Garamond가 없다면 Times로 */
/* Garamond, Times가 없다면 이미 설치된 폰트로 */
```

- `"Garamond"` 뒤에 있는 `"Times", serif`  가 fallback fonts들임.
- 사이트를 방문하는 많은 유저들에게 일관된 view를 보여주고 싶을 때 유용



### Linking Fonts

: 모든 폰트를 설치해서 사용하는 데 한계. 링크해서 사용하자.

: Google Fonts, 오픈소스 폰트 사용.

- 해당 폰트 검색 후 `+` 버튼 클릭

- 밑에 뜬 창 클릭, `link` 태그 복사

- .css 파일 `header` 태그 안에 붙여넣기

  ```html
  <head>
    <link href="https://fonts.googleapis.com/css?family=Droid+Serif:400,700,700i|Playfair+Display:400,700,900i" rel="stylesheet">
  </head>
  <!-- font-weight을 다음과 같이 줄 수 있음 -->
  ```

  

### Font-Face

: html에 link를 쓰지 않고 stylesheet 폴더 안에 폰트 파일을 넣어서 사용.

: `@font-face` 로 import시켜 사용.

```css
@font-face {
  font-family: "Roboto";
  src: url(fonts/Roboto.woff2) format('woff2'),
       url(fonts/Roboto.woff) format('woff'),
       url(fonts/Roboto.tff) format('truetype');
}
/* 규칙. src: url(파일의 경로) format('truetype' ( ==사용하고자 하는 폰트) */
```

