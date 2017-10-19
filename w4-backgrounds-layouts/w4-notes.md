notes
-a menu » multiple pages » psuedo classes
-background images
-flexbox
-hosting

## Warm Up
- position the button in the bottom right corner

## Objectives
- I can build a menu of links to access different pages
- I can use the CSS background properties to insert images and backgrounds.

## Mini-Lesson 1, build a menu
-build the menu in the index.html
```html
<ul class="menu">
<li><a href="index.html">home</a></li>
<li><a href="about.html">about</a></li>
<li><a href="contact.html">contact</a></li>
</ul>
```
-style it
```css
/* remove bullets, remove default space */
.menu {
  list-style-type: none;
margin: 0;
padding: 0;
}

/* make the list items look more like buttons */

.menu li {
border: 1px solid black;
width: 100px;
       text-align: center;
display: inline-block;

margin: 0;
}

/* style the the visited links */
a {
  text-decoration: none;
color: black;

display: block;
width: 100%;
}

/* make a hover effect... */
a:hover{
color:green;
      background-color: lightgrey;
  }
```

## Mini-Lesson 2, CSS background property
[resource](https://css-tricks.com/almanac/properties/b/background-image/)
When and Where
- Logo, common to use a CSS background
- background images or textures, show a pattern background
- show a 'parallax' like example

### Example
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

- Hero image example
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
- Target the body tag
1. Set background image to bart.png in the images folder
2. Turn of the repeat
3. position the background in the top right corner
4. set the margin to 0
5. set the background-attachment so the image doesn't move
- Target the logo id
1. set the display to block
2. Size the box to 500px;
3. use the margins to center in the middle of the page.
4. Set the background to krusty.gif
5. Position the image in the background
6. turn off the repeat.
- Target the hello class
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
  height: 500px
  background-image: url('./images/krusty.gif
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

## Mini-Lesson 3: flexbox
- There is html in a starter file
```css
h1{
	text-align: center;
	font-family: helvetica;
}
.wrapper{
	width: 900px;
	margin: 0 Auto;
	background-color: #BADA55;

	display: flex;
  align-items: center;
	/* flex-wrap: wrap; */
} 
.box{
	background-color: orange;
	width: 100px;
	height: 100px;
	margin: 10px;

	/* flex-grow: 1; */
}
.fig{
  height: 300px;
	flex-grow: 3;
}
```
 
Play, 5 minutes or so
- Go to this website, http://codepen.io/enxaneta/full/adLPwv/
- Mess around with the flexbox features.

### Position Exercise
- build a flex box menu, use menu-flex.html and menu-flex.html
- follow the comments.
- Solution
```
* {
  box-sizing: border-box;
  font-family: 'Chewy', cursive; 
}
body {
  background-color: #AEECEF; 
}

#wrapper {
  width: 900px;
  margin: 0 auto;
}

.header {
  padding: 20px;
  background-color: #fff; 
}

.menu {
  padding: 0;
  margin: 0;
  list-style: none;

  /* make this a flex container */
  display: flex;
   
  /* play with the spacing */ 
  justify-content: flex-start; 
   
  /* play with alignment */
  align-items: center;
}

.menu a {
  display: block;
  width: 100%;
  padding: 15px;
  text-align: center;
   
  font-size: 40px;
  text-decoration: none;
  color: #F991CC;
   
}

.menu a:hover {
  background-color: #F991CC;
  color: #FFF; 
}
 
/* another psuedo class */
/* this one only effects the first li in main */
/* here it is applying flxe grow to just the first li */
/* turn it on and off to see what it does */
.menu li:first-child {
  /* flex-grow: 1; */
}
 
.menu .logo{
  background-image: url("https://media.giphy.com/media/ISjYZh2up6Pn2/giphy.gif");
  width: 150px;
  height: 150px;
  background-size: cover;
  margin-right: auto; 
}

h2 {
  font-size: 40px;
  color: #2A1E5C;
}
```

> move to later, do a whole day on web animations?
> ## Transitions
> - show how to apply a size transtion on one of the boxes
> - show how to activate on hover
> - [exercise](https://www.w3schools.com/css/exercise.asp?filename=exercise_css3_transitions1)

