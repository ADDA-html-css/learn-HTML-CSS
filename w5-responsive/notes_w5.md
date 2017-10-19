## Objectives
- I can create a grid using flex-box
- I can apply zindex, transition, and box shadows to my css
- I can use github pages to host my personal website.
- I can create an amazing personal website working from wireframe to final code. 

## Do Now
- Take the code for a simple grid in the DoNow folder. Don't touch the html!
- Use flex to make a 4 x 3 grid
- make the first grid element a perfect circle without touching the html!
- when you hover over the elements, make them change color.

```css
.wrapper{
	width: 850px;
	padding:12.5px 0 0 12.5px;
	background-color: #eee;
	
	display: flex;
	flex-wrap: wrap;
}

.gi{
	margin-right: 12.5px;
	margin-bottom: 10px;
	width: 200px;
	height: 200px;
	background-color: #8822FF;
	
	
}

.gi:hover{
	background-color: #22FF22;	
}

.gi:first-child{
	border-radius: 50%;
}

.gi:hover{
	background-color: #22FF22;
}
```

Introduce Transitions
-add to gi
```css
	transition: background-color 2s ease-out;
	transition: border-radius 2s;
	/*transition: background-color 2s;*/

```

## Clearfix
-Show a better clearfix problem/solution
-float the logo left or right
-What happens?
```
.clearfix:after { 
   content: "."; 
   visibility: hidden; 
   display: block; 
   height: 0; 
   clear: both;
}
```

## Github Page For Hosting!
- Create a new repo, named username.github.io
- initialize with a readme
- You html page must be called index.html
- Add your index.html and css files to the repo
- Go to `http://username.github.io/` should work


