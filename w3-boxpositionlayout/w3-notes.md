#Week 3
box model, positioning, simple layout

## Objective
- I understand how padding, margin, and width work together in the box model.
- I can create a simple "About Me" page using HTML and CSS.

## Agenda
- box model, padding, margin
- Work Time
- Push to GitHub

## Box Model      
EVERY element in web design is a rectangular box.

The amount of space that the box will occupy is calculated like this...
width + padding + border + margin = total width 
height + padding + border + margin = total height 

### Demo 1
- before doing CSS, open up the page, see what it looks like, note the <p> stretches the whole page.
- give the `#page-contain` a width. Now notice the <p> wraps to the parent element
- give the box a width, border, margin and padding
- now open up the Inspector and see how much space each element has. Note the content box will be less than whatever the box width was set to.

### Demo 2
- before doing anything, look over code with class, open in browser and note two boxes side by side.
- add border and padding to left box. Refresh display.
- note the two boxes aren't side by side anymore.
- we could do math and resize the box based off the added padding and border, but that would be annoying
- use `box-sizing: border-box` to show how this will recalculate the size to include the padding and border in the overall total.
- margin will still mess everything up, there are some better ways of doing this kind of thing.

Show slide with the `content-box` and `border-box` criteria side by side.

### Exercise
- Go to https://www.w3schools.com/css/exercise.asp?filename=exercise_boxmodel1
- Complete steps 1-4, should take under 5 minutes!

## About Me Page

Introduce mini-project with slides
- Show suggested workflow
- Show simple wireframe, then the "marked up" one.
- Get students started, have them move the two files from "starter" folder to their .github.io repo.

Have students work on page. Next week we will deploy.
