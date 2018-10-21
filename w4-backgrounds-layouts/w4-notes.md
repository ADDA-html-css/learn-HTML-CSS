notes
- a menu » multiple pages » psuedo classes
- background images
- flexbox
- hosting

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

  */
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

Now change the demo box to be position absolute, reload.

Change demo button to be absolute
```
     .demo button{
     position: absolute;
     bottom: 0;
     right: 0;
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
