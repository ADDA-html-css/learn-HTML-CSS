# Week 2 Instructor Notes

## Objectives
- I can investigate and build layouts using the CSS "Box Model" 
- I can investigate how the display property effects an element
- I can explain and use the different CSS positioning styles
- I can use nested targets.

## Housekeeping 
- Using github desktop
- go to homework [repo](https://github.com/ADDA-html-css/F_2016_HTMLCSS_HW)
- create a fork
- clone that fork in desktop
- Go to that location, make a folder with your name
- Copy the folder with starter into your folder, 
- do all your work in this location
- When you are finished, sync, then do a pull request

## Do Now
Find the error!
```html
<body>
	<h2>My Weekend Plans
		<ul>
			<li>sleep</li>
			<li>watch tv</li>
			<li>eat good food
		<ol>
</body>
```

## Stand-up
- Successes?
- Struggles?
- Show and Tell!

## Mini-Lesson 1, classes
```html
<html>
<head>
	<title>Class V. ID</title>
	<link rel="stylesheet" type="text/css" href="idAndClass.css">
</head>
<body>
	<div id="titleDiv">
		<h1>Class v. IDs</p>
	</div>

	<div class="red">
		<p>red text<p>
			<p class="blue">red text?</p>
	</div>

	<h2 class="red">A red header</h2>
	<a href="http://www.facebook.com" class="red">A red link</a>

</body>
</html>

```

```css
	#titleDiv{
		color: green;
	}

	.red{
		color: red;
	}

	.blue{
	background-color: blue;
	}
```

- An ID should be unique to a single html element
- Many elements can share a class
- Analogy: You have an ID, there is no one else should share your ID. You are in this class, but many people can share this class.

### Excercise 1
- Make index.html
- Make three paragraphs, use a text generator
- Make style.css
- Make the first paragraph green
- Make the second paragraph black text (normal) with a silver background
- Make the third paragraph green text and a silver background

Introduce DRY!

## Mini-Lesson 2, Box Model
Show a basic slide of the box model.
[link](http://www.w3schools.com/css/css_boxmodel.asp)

### Exercise 2
** investigate a simple box model and how it effects the layout**
Have two divs that are next to each other, have students open up the inspector on this page
- Make the border larger. What happens? Return to normal.
- Make the padding larger. What happens? Return to normal.
- Make the margin larger. What happens? Return to normal.
- Formulate a theory of what is happening.

Bonus: add a css property, `box-sizing: border-box;` to one of the elements, now change the padding and margin. What happens now?

Have a discussion. Show a computed [example](http://www.sitepoint.com/web-foundations/css-box-model/)

**Cool Trick**
```css
* {
   border: 1px solid red !important;
}
```
## Mini-Lesson 3, display
- inline
- block
- inline-block
- display none;
- visibility: none;

### Exercise 3

Starter Code
```html
<html>
<head>
	<title>Display Exercise</title>
	<link rel="stylesheet" type="text/css" href="display.css">
</head>
<body>
	<div id ='one' class='box'>
		one
	</div>

	<div id ='two' class='box'>
		two
	</div>

	<div id ='three' class='box'>
		three
	</div>

	<div id ='four' class='box'>
		four
	</div>

	<div id ='five' class='box'>
		five
	</div>

	<ul>
			<li>pizza</li>
			<li>calzone</li>
			<li>pasta</li>
	</ul>
</body>
</html>
```

Part 1
1. Style the box class 
	- width and height of 200px
	- a backgound color
	- add a border
2. Open in browser, what do you see?
3. Add a `display: inline;` to the box class. What do you see?
4. Change to `display: inline-block;` What do you see now?
5. Target an individual box, change the display to the different options, what's happening?
6. Target an individual box, change to `display: none;` what happened?
7. Remove the `display: none;` add `visibility: hidden` what happened?

Part 2
1. Target the list items `li`
	- add a background color
	- add a width and a height
2. load in browser, what do you see?
3. Change the display to the different options, what happens?

Possible Responses
1. boxes stacked on top of each other
2. boxes are small, only take up the width of the text
3. now boxes are spread across the screen
4. When a single element is changed to block, it breaks the flow of the other boxes

## Mini-Lesson 4, CSS Positioning
- static, default
- Relative, relative to the surrounding elements
- Absolute, takes out of flow,
- Fixed, doesn't move, fixed inside the window

```
#container{
	width: 100%;
	max-width: 800px;
	display: block;
	margin: 0 auto;
	
}

.demo{
	background-color: #BADA55;
	width: 200px;
	height: 200px;
	opacity: 0.5;
	right: 500px;

	border-radius: 10;
}

.demo button{
	position: absolute;
	top: 10px;
	right:10px;

	display: block;
	width:100px;
}


.footer{
	background: #BADA55;
	width: 100%;
	height: 120px;
	text-align: center;
	bottom: 0;
	opacity: 0.5;
}

body{
	margin-bottom: 120px;
}
```
change demo button to be absolute
```
.demo button{
	position: absolute;
	bottom: 0;
	right: 0;
}
```

fix the footer
```css
	.footer{
		background: #BADA55;
		width: 100%;
		height: 120px;
		text-align: center;
		position: fixed;
		bottom: 0;
	}
```

Add a margin to the bottom of the body, otherwise text will be covered up.
```css
body{
	margin-bottom: 120px;
}
```

### Exercise 4
ipod challenge

```html
	<html>
  <head>
    <title>Cool CSS</title>
    <link rel="stylesheet" href="style.css" ></script>
  </head>
  <body>
  
  <div id="ipod_body">
    <div id="screen">
      <div id="top_bar">
        <h6>Now Playing</h6>
        <div id="battery">
        </div>
      </div>
      <ul id="selection_list">
        <li>Music</li>
        <li>Video</li>
        <li>Photos</li>
        <li>Podcasts</li>
        <li>Extras</li>
        <li>Settings</li>
        <li>Shuffle Songs</li>
        <li>Now Playing</li>
      </ul>
    </div>
    <div id="wheel">
      <div id="menu"><h4>Menu</h4></div>
      <div id="forward"><h4>|>></h4></div>
      <div id="back"><h4><<|</h4></div>
      <div id="inner_wheel">
    </div>
      <div id="play">
        <h4>>||</h4>
      </div>
    </div>
  </div>  
  
  </body>
</html>
```

## HW

### Continue working on your personal site.
- Create a inline menu from list items.
- Add a footer that sticks to the bottom of you page

### Practice CSS Positiokning
![Example Layout](http://designshack.net/wp-content/uploads/layoutideas-1-1.jpg)
Build this layout from scratch.

Bonus! Add content. Make one of the images a circle.

### Review CSS Positioning! 
Watch this [video](https://css-tricks.com/video-screencasts/110-quick-overview-of-css-position-values/)

## Extra Resources
+ Watch [Don't Fear the Browser - Developer Tools & Vanilla Ice Cream](http://www.dontfeartheinternet.com/html/html) (3:35)
+ Read [Building Your First Web Page](http://learn.shayhowe.com/html-css/building-your-first-web-page/)
+ Watch [Don't Fear Starting from Scratch Part 1: HTML](http://www.dontfeartheinternet.com/html/don%E2%80%99t-fear-starting-from-scratch)
+ Watch [Don't Fear Starting from Scratch Part 2: CSS](http://www.dontfeartheinternet.com/css/don%E2%80%99t-fear-starting-from-scratch-2)




