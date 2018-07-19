---
layout: post
title:  "생활코딩 CSS 강의"
date:   2018-07-19 00:09:11 +0900
categories: css
---

## 선택자

li{
color:red;
text-decoration:underline;
}

css game
http://flukeout.github.io/

https://userstyles.org/

http://brackets.io/

## 기타

### border - shorthand property

border-width
border-style (required)
border-color

## 레이아웃

### 인라인 VS 블럭레벨

```
h1,a{border:1px solid red;}
h1{display: inline;}
a{display:block;}
```

### 박스모델

### box-sizing

width 와 height 는 엘리먼트의 컨텐츠의 크기를 지정 (마진 부분 제외)
box-sizing:border-box;

### 마진겹침현상

마진겹침(margin-collapsing) 현상은 상하 마진값이 어떤 상황에서 사라지는 현상

1.  이웃 엘리먼트
    더 큰 마진이 두 엘리먼트 사이의 마진이 된다.
2.  부모 자식 엘리먼트
    부모엘리먼트가 시각적으로 아무런 스타일이나 내용이 없을 때 마진겹침 발생. 부모 자식 마진 중 큰 마진이 두 엘리먼트의 마진이 된다.

```
 #parent{
            border:1px solid tomato;
            margin-top:100px;
        }
        #child{
            background-color: powderblue;
            margin-top:50px;
        }
```

3.  이웃 엘리먼트에서 한 엘리먼트가 시각적으로 아무런 스타일이나 내용이 없을 때 마진겹침 발생

```
#empty{
            margin-top:50px;
            margin-bottom: 100px;
            border:1px solid tomato;
        }
        #normal{
            background-color: powderblue;
            margin-top:100px;
        }
```

### 포지션

static
relative
absolute
fixed

### flex

```
<container>
    <item></item>
    <item></item>
</container>
```

container 와 item 에 주는 attribute 가 구분되어 있음

#### flex 의 기본

flex 를 사용하기 위해서는 컨테이너 태그에 display:flex 속성을 부여해야 합니다.
flex-direction 을 이용해서 정렬방향을 바꿀 수 있습니다

#### grow & shrink

flex-basis: 150px - 기본 크기 지정
flex-grow:1 - 여백 n 빵
flex-shrink:0 - 창이 작아졌을 때, flex-basis 로 준 사이즈가 작아지지 않음. flex-shrink:1 이면 작아짐.

#### Holy Grail layout

align-items:center;

#### flex 의 여러 속성들

http://codepen.io/enxaneta/pen/adLPwv

- Properties for the flex container

* display
* flex-direction
* flex-wrap
* flex-flow
* justify-content
* align-items
* align-content

- Properties for the flex items

* order
* flex-grow
* flex-shrink
* flex-basis
* flex
* align-self

## media query

min-width: 480px 최소 480px 이상일 때 적용
max-width: 480px 최대 480px 이하일 때 적용
캐스캐이팅
같은 조건들이 있으면 나중에 나오는 조건에 나오는 스타일이 우선순위가 높음

## 질문

- flex 쓸 때, wrap 하면서 part 의

## Frequently used style attributes

```
font-size
color
margin-top
margin-left
width
margin-bottom
margin-right
padding-left
padding-top
height
padding-bottom
padding-right
font-family
text-decoration
display
font-weight
border-bottom-width
text-align
border-bottom-style
border-top-width
background-color
border-left-width
border-top-style
border-right-width
background-image
position
border-left-style
border-right-style
float
line-height
top
left
background-position-y
background-position-x
clear
z-index
border-bottom-color
list-style-type
border-top-color
cursor
vertical-align
border-right-color
right
border-left-color
visibility
font-style
border-bottom-left-radius
border-bottom-right-radius
border-top-right-radius
bottom
border-top-left-radius
opacity
min-height
content
box-shadow
max-width
text-transform
overflow-y
overflow-x
font-variant
outline-width
white-space
background-repeat
text-indent
background-repeat-x
background-repeat-y
font-stretch
text-shadow
box-sizing
overflow
transition-duration
min-width
outline-style
transition-property
letter-spacing
transition-timing-function
```
