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
