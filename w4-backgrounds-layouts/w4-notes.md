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

## 1 Positioning
- static, default
- Relative, relative to the surrounding elements, still takes up the same space.
- Absolute, takes out of flow,
- Fixed, doesn't move, fixed inside the window

Change the demo box to be relative, reload.
```
  /* add to demo class
     position: absolute;
     left: 500px;
```

Now change the demo box to be position absolute, reload.

Change demo button to be absolute
```
     .demo button{
     position: absolute;
     bottom: 0;
     right: 0;
     }
```

Fix the footer
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

## Mini-Lesson 2, layout with foats

### Live Code
- starter code is `layout.html` and `layout.css`
- HTML is done
- Add to the CSS

```css
#container{
width: 800px;
margin: 0 auto;
height: 30px;
}

header{
height: 60px;
background-color: #33A1FD;
}

sidebar{
background-color: #F55536;
float: left;
width: 300px;
height: 400px;
}

main{
float: right;
width: 500px;
height: 200px;
background-color: #F79824;
}

footer{
height: 200px;
background-color: blue;
  clear: both;
  }
```

## Mini-Lesson 2, build a menu
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
