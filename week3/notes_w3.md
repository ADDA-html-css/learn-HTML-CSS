# Week 3

## Do Now

## Objectives
- I can investigate how the display property effects an element
- I can explain and use the different CSS positioning styles
- I can use the CSS background properties in all of their glory.

## Housekeeping
- Do a update in github desktop, you should have a folder now called week3.

## Stand-up
- Successes?
- Struggles?
- Show and Tell!

## Mini-Lesson 1, display
- inline
- block
- inline-block
- display none;
- visibility: none;

### Exercise 1 

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

## Mini-Lesson 2, CSS Positioning
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

### Exercise 2 
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

## Mini-Lesson 3, CSS background property
[resource](https://css-tricks.com/almanac/properties/b/background-image/)
When and Where
- Logo, common to use a CSS background
- background images or textures, show a pattern background
- show a 'parallax' like example

### Example 3
- Make starter code, drop in a logo. Apply a background image, repeat.

```css
body{
	background-image: url('./images/textured_paper.png')
}

#logo{
	display: block;
	/*background-color: white;*/
	width: 500px;
	height: 500px;
	margin: 0 auto;

	background-size: 100px;
	
	background-position: center;
	
	background-repeat: no-repeat;
	
	/*background-repeat: repeat-x;
	background-repeat: repeat-y;*/
	
	background-image: url('http://pre07.deviantart.net/08b2/th/pre/f/2012/050/0/b/planet_express_logo_by_chupacabrathing-d4qbo3v.png');
}
```

example
```css
body{
	margin: 0;
	font-family: "Helvetica Neue"
}
div{
	padding: 100px;
	background-color: cornFlowerBlue;
}
.bg-image{
	display: block;
	height:600px;
	background-image: url('https://wallpaperscraft.com/image/futurama_doctor_zoidberg_69273_1920x1080.jpg');
	background-size: cover;
	background-attachment: fixed;
	background-position: 50% 50%;
}
```
#### Exercise, don't touch html!
- [ ] Target the body tag
	1. Set background image to bart.png in the images folder
	2. Turn of the repeat
	3. position the background in the top right corner
	4. set the margin to 0
	5. set the background-attachment so the image doesn't move
- [ ] Target the logo id
	1. set the display to block
	2. Size the box to 500px;
	3. use the margins to center in the middle of the page.
	4. Set the background to krusty.gif
	5. Position the image in the background
	6. turn off the repeat.
- [ ] Target the hello class
	1. set width to 100%;
	2. set the height to 200px;
	3. repeat along the x-axis but not the y
	4. set a background color of orange

Solution
```css 
body{
	background-image: url('./images/bart.png');
	background-position: right top;
	background-repeat: no-repeat;
	margin: 0;
	background-attachment: fixed;
}

#logo{
	display: block;
	margin: 0 auto;
	width: 500px;
	height: 500px;
	background-image: url('./images/krusty.gif');
	background-position: center;
	background-repeat: no-repeat;
}

.hello{
	width: 100%;
	height: 500px;
	background-image: url('./images/hello.gif');
	background-size: 200px;
	margin-top: 100px
}
```

## Homework
- Rebuild Instagram
