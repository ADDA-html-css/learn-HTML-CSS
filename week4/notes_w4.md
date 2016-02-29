# Week 4
## Do Now
We are moving to building a personal website and interactive resume. Each of our needs for a personal website are a little different. Spend a few minutes writing about what you want out of a psersonal website. What information is most important, what do you want a visitor to get out of your website? What do you want it to say about yourself.

## Objectives
- I can develop advanced layouts using simple grids and flexbox.
- I can use the float property to control object positioning.
- I can build simple interactions with pseudo classes.
- I can load fonts into my markup and use them in CSS rules.
- I can create an amazing personal website working from wireframe to final code. 

## Resources
- [Google Drawing Wireframe Templates](https://drive.google.com/templates?q=%23wfkit&ddrp=1#)
- 
## Housekeeping
- Do a git sync, you should have a folder now called week3.

## Stand Up
- Successes?
- Struggles?
- Show and tell, design inspiration.

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
```html
<!-- inside body -->
<div class="wrapper">
	<header class="b-bl m-t-1"><h1>Two Column Layout</h1></header>
	<div class="main b-bl m-t-1">main</div>
	<div class="sidebar b-bl m-t-1"></div>
	<footer class="b-bl m-t-1">Foot</footer>
</div>
```

```css
.wrapper{
	width: 900px;
}

.b-bl{
	border: 1px solid black;
}
.main{
	float: left;
	width: 66%;
	height: 500px;
}

.sidebar{
	float: right;
	width: 33%;
	height: 300px;
}

footer{
	clear:both;
}

```

### flexbox
```html

```

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

## Mini-Lesson 4, Wireframes and Prototypes
**Purpose of wireframes** 
- layout of a page
- No style just visual structure
- The whole point is to have a quick way of playing with a sites design
- size the page to the device you are playing for

**Wireframe Options**
- Can be drawn by hand (this is usually where I start)
- Using google drawings and sheets, with stencils
- Using sketch, adobe illustrator or photoshop (obviously you will need a foundation in these programs)

**From wireframe to prototype**
- a prototype is a quick mockup of a website.
- allows us to test the site without writing any code.
- Usually a prototype has a buttons as links to a few different pages
- allows you as a designer to test some of the navigation and layout elements. 
- Prototypes can be tested with users, 
	+ ask a user to perform a specific task, 
	+ watch them as they interact with your prototype.

**Prototype Options**
- Protoyping on Paper, website and app
- Using Google Drawings and Sheets
- Using InVision, you will need to upload images or design files (psd, ai, pdf, sketch)

### Your Task
- Create a wireframe for the desktop version of your personal site.
- Create a simple prototype from your wireframe, 1-3 pages, some buttons, some links
- Test your prototype different people. Ask them to do a specific task, i.e. "where would you go to find my resume", pay attention to there movements.

## Homework
- Build your personal website from your prototype.
- Create a new repository in github to hold your files.
- Rebuild Tattly