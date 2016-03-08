## Objectives
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
	
	transition: width 1s, height 1s, background-color 1s, border-radius 1s
}

.gi:hover{
	background-color: #22FF22;	
}

.gi:first-child:hover{
	border-radius: 100%;
}
```


## Mini-Lesson 1, z-index
- Think cartesian coordinates, what would z represent?
- This is the stacking ordr of elements on the page.
- load example, what do you notice?
- positive numbers will make the element move up
- negative numbers will make it move down
- nothing can go behind the body!

ex simpsons

## Mini-lesson 2, box shadow
- This is so hot right now
- google cards
- add this too code

```css
box-shadow:10px 10px 10px #aaa;
```
- change the zindex, looks bad!
```css
box-shadow:10px 10px 10px rgba(0,0,0,0.1);
```
-better, describe rbga colors


## Mini-Lesson 3, Wireframes and Prototypes
**Purpose of wireframes** 
- layout of a page
- No style just visual structure
- The whole point is to have a quick way of playing with a sites design
- size the page to the device you are playing for

**Wireframe Options**
- Can be drawn by hand (this is usually where I start)
- Using google drawings and sheets, with stencils
- Using sketch, adobe illustrator or photoshop (obviously you will need a foundation in these programs)

**From wireframe to prototype**
- a prototype is a quick mockup of a website.
- allows us to test the site without writing any code.
- Usually a prototype has a buttons as links to a few different pages
- allows you as a designer to test some of the navigation and layout elements. 
- Prototypes can be tested with users, 
	+ ask a user to perform a specific task, 
	+ watch them as they interact with your prototype.

**Prototype Options**
- Protoyping on Paper, website and app
- Using Google Drawings and Sheets
- Using InVision, you will need to upload images or design files (psd, ai, pdf, sketch)

### Your Task
- Create a wireframe for the desktop version of your personal site.
- Create a simple prototype from your wireframe, 1-3 pages, some buttons, some links
- Test your prototype different people. Ask them to do a specific task, i.e. "where would you go to find my resume", pay attention to there movements.