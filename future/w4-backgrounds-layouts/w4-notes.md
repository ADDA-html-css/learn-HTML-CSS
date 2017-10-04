- I can use the CSS background properties to insert images and backgrounds.
- I can apply zindex, transition, and box shadows to my css.

## Mini-Lesson 1, CSS background property
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

## Z-index
- Think cartesian coordinates, what would z represent?
- This is the stacking order of elements on the page.
- load example, what do you notice?
- positive numbers will make the element move up
- negative numbers will make it move down
- nothing can go behind the body!

### You Do
- Open zindex/ex folder
- No need to edit the html!
- use zindex to move your least favorite simpsons character behind the orange div
- use zindex to put your favorite characters on top of all the others
- can you make the image that the mouse is over come to the front?
- BONUS, use "hover" to change the size when you hover over an image, can you make this happen smoothly?

Exercise Solution
```
.wrapper{
	width: 900px;
	height: 400px;
	margin: 0 auto;
	padding-top: 50px;
	padding-left: 200px;
	background-color: orange;
}

img{
	position: relative;	/*zindex only works with postioned elements*/
	height: 300px;
	margin-left: -100px;

	transition: height 1s;
}


/*character I don't like*/
.nelson, .burns, .maggie{
	z-index: -100;
}

img:hover{
	z-index: 100;

	height: 600px;
}
```

## Box shadow
- so hot right now
- google cards
- add this to zindex code

```css
box-shadow:10px 10px 10px #aaa;
```
- change the zindex, looks bad!
```css
box-shadow:10px 10px 10px rgba(0,0,0,0.1);
```
-better, describe rbga colors

## Transitions
- show how to apply a size transtion on one of the boxes
- show how to activate on hover
- [exercise](https://www.w3schools.com/css/exercise.asp?filename=exercise_css3_transitions1)

# Boostrap

## Making a Responsive Grid
- explain how the grid works
- 12 columns
- show auto-sized columns using '.col' class
  ```html
  <div class="container wrapper">
    <div class="row">
      <div class="col colStyle">
        4 columns 
      </div>
      <div class="col colStyle">
        4 columns  
      </div>
      <div class="col colStyle">
        4 column
      </div>
    </div>
  </div>
  ```

- show how to do a 9-2-1 grid, show what happens when the row exceeds 12 columns
  ```html
  <div class="container wrapper">
    <div class="row">
      <div class="col-md-9 colStyle">
        9 columns 
      </div>
      <div class="col-md-2 colStyle">
        2 columns  
      </div>
      <div class="col-md-1 colStyle">
        1 column
      </div>
    </div>
  </div>
  ```
- show how to do an offset
  ```html
  <div class="container wrapper">
    <div class="row">
      <div class="col-md-8 colStyle">
        9 columns 
      </div>
      <div class="col-md-3 offset-md-1 colStyle">
        2 columns  
      </div>
    </div>
  </div>
  ```

- show a nested grid
  ```html
      <div class="col colStyle">
        <div class="row">
          <div class="col">
           nested 1
          </div>
          <div class="col">
           nested 2 
          </div>
          <div class="col">
           nested 3
          </div>
        </div>
      </div>
  ```
- show how to do responsive grids
```html

  <div class="container wrapper">
    <div class="row">
      <div class="col-md-4 colStyle">
        4 columns  
      </div>
      <div class="col-md-4 colStyle">
        4 columns  
      </div>
      <div class="col-md-4 colStyle">
        4 column
      </div>
    </div>
  </div>
```

- show how to hide use '.hidden-lg-down'
```html
  <aside class="jumbotron container hidden-lg-down">
    hidden content
  </aside>
```

### Your Turn
- Build a responsive page using bootstrap, see slide
