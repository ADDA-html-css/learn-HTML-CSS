# Week 4
## Do Now
- Use positioning to put a button in the bottom right corner of a square that is 200 pixels in size.

```css
.box{
  position: relative;
  width: 200px;
  height: 200px;
  background-color: #BBAADD;
}

button{
  position: absolute;
  bottom: 10px;
  right: 10px;
}
```

## Objectives
- I can develop advanced layouts using simple grids and flexbox.
- I can use the float property to control object positioning.
- I can build simple interactions with pseudo classes.
- I can load fonts into my markup and use them in CSS rules.

## Housekeeping

## Stand Up
- Successes?
- Struggles?


## Mini-Lesson 1, Advanced Positioning

### Floats
- Float will move an element to the right or left
- Used for making multiply column layouts
- Will take the element out of the normal flow.

Floating Div
- HTML Starter file in advDispaly folder

```css
.container{
	width: 800px;
	background-color: #B2675E;
	margin:0 auto;
}

aside{
	background-color: #F55536;
	float: right;
	width: 500px;
	height: 500px;

}

.clearfix:after { 
   content: "."; 
   visibility: hidden; 
   display: block; 
   height: 0; 
   clear: both;
}
```

Two Column Layout
-html starter in folder

```css
.container{
	width: 800px;
	height: 20px;
	margin: 0 auto;
	
}
.header{
	height: 60px;
	background-color: #b2675E;
}

.sidebar{
	background-color: #F55536;
	float: left;
	width: 300px;
	height: 300px;
}

.main{
	float: right;
	width: 500px;
	background-color: blue;
	height: 200px;
}

.footer{
	clear:both;
}
```

### flexbox
- There is html in a starter file
```css
  h1{
  	text-align: center;
  	font-family: helvetica, sans-serif;
  }

  .wrapper{
  	display: flex;
  	flex-wrap: wrap;
  	width: 900px;
  	margin: 0 auto;
  	background: #BADA55;
  }

  .box{
	  border: 1px solid orange;
	  width: 428px;
	  height: 200px;
	  margin: 10px;
  }

  .elderberry{
  	flex-grow: 2;
  }
```

Play, 5 minutes or so
- Go to this website, http://codepen.io/enxaneta/full/adLPwv/
- Mess around with the flexbox features.

### Position Exercise
- Build a 2 row, 4 column grid of divs using floats for positioning.
- Build the same grid, using flexbox for positioning.

## Mini-Lesson 2, Pseudo Classes 
- A pseudo class is a keyword added to a selector that designates a special state.
- The styles in a pseudo class are applied only when a condition is true.
- Here are some pseudo classes
	+ a:visited - target a link that is visited
	+ element:hover - adds rules to an element only when the mouse is over it. 
	+ element:focus - adds focus when an element is in focus, think forms
[MDN Guide to Pseudo Classes](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

insert example
- hover
- focus
- visited
- first child
- last child 
- nth child

```css
.txt, .btn{
	width:300px;
	height: 30px;
	border: solid 2px #eee;
	font-size: 20px;
	font-family: helvetica, sans-serif;
	border-radius: 0;
}

.txt:focus, .btn:focus{
	border: solid 2px #91F5AD;
	outline: none;
}

.btn{
	background-color: white;
	border: solid 2px #91F5AD;
	color:#91F5AD;
}

.btn:hover{
	background-color: #91F5AD;
	color: #fff;
}

ul{
	font-size: 20px;
	font-family: helvetica, sans-serif;
  
  padding: 0;
  margin: 0;

  list-style: none;
}

li:first-child{
	color: #745296;
}

li:last-child{
	color: #D1626F;
}

li:nth-child(2){
	color: #C65CA3;
}

a, a:visited{
	color: #C65CA3;
	text-decoration: none;
}

a:hover{
	color: #D1626F;
	text-decoration: underline;
}

li:before{
  content: 'before';
}

li:after{
  content: 'after';
}
```

### Pseudo Exercise
- add style to grid that you made in the previous exercise.
- on hover, change the background color of the element that is under the mouse
- use the first-child to change the background color of the first box
- use the last-child to change th background color of the last box
- use nthchild to change the background color of another box.

## Mini-Lesson 3, using fonts
- show google fonts demo
```html
<link href='https://fonts.googleapis.com/css?family=Poiret+One|Open+Sans' rel='stylesheet' type='text/css'>
```

```css
body{
	font-family: 'Open Sans', sans-serif;
	background-image: url('concrete_wall_2.png');
}

#page-wrapper{
	width: 940px;
	margin: 0 auto;
	background: #fff;
	padding: 20px;
}

h1, h2, h3, h4, h5, h6{
	font-family: 'Poiret One', cursive;
}
```

