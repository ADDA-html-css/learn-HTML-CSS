#Week 3
box model, positioning, simple layout

## Objective

## Agenda
- box model
- positioning exercise
- floats!

## 1 Float vs IDs

- An ID should be unique to a single html element
- Many elements can share a class
- Analogy: You have an ID, there is no one else should share your ID. You are in this class, but many people can share this class.

Demo with class.html and class.css
-add the class happy and sad to the titles
`<h1 class="happy">I'm a Happy Title</h1>`

-show that an element can have more than one class applied
`<button class="circle happy">click for happy</button>`

-show that the id current will override the sad text
`h1 id="current" class="sad">I'm a Sad Title</h1>`

Final thought: you will use classes a lot more than ids. 
 
## 2 Box Model      
EVERY element in web design is a rectangular box

The amount of space that the box will occupy is calculated like this...
width + padding + border + margin = total width 
height + padding + border + margin = total height 
 
Why should I care? Show `demo/box.html` and `demo/box.css`
- padding and a border to `left`, what happens?

One fix! use box sizing...
`box-sizing: border-box;`

- this rule says "when calculating the box size include the border and padding in that calculation." 
- margin will still mess everything up, there are some better ways of doing this kind of thing.

### Exercise
- Go to https://www.w3schools.com/css/exercise.asp?filename=exercise_boxmodel1
- Complete steps 1-4, should take under 5 minutes!

## 3 Positioning
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

## Layout with Floats
 
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

## Work Time
- convert wireframe to code
- start with identifying structure in html
- code up html
- start working on css

## Out of Class
- Continue working on your page.

## Resources
- [Positioning](http://www.barelyfitz.com/screencast/html-training/css/positioning/)
- [Floats](https://css-tricks.com/all-about-floats/)
- [More Floats](https://alistapart.com/article/css-floats-101)
