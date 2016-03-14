# Week 6 Notes

## Objectives
- I can celebrate the sucess of creating my first website.
- I can design responsive, mobile first pages using media queries.
- I can use responsive image best practices to increase page performance.

## Mini-lesson 1, Responsive desgin.
### Responsive Design
Responsive Web Design is intended to make your web page look beautiful on all devices (desktops, tablets, and phones).

The idea being that the page should respond ot the users environement based on screen size, platform, and orientation.

Responsive Web Design is about using CSS and HTML to resize, hide, shrink, enlarge, or move the content to make it look good on any screen

### Mobile first
As suggested, design for mobile first. Why?
- Simplest, your mobile site should be the most simple to navigate and read. It should only present the content that is necessary for the user.
- You create more structure as you go, don't have to overwrite css rules.

Your small screen styles are in your regular screen CSS and then as the screen gets larger you override what you need to. So, min-width media queries in general.

How do we achieve this? 
- Media Queries
- Responsive units

### Media Queries

Demo Media Queries
```css
html { background: red; }

@media (min-width: 500px){
  html { background: green; }
}

@media (min-width: 900px) {
  html { background: blue; }
}
```

Your Turn: Create a new media, when the screen is larger than 1100px, make the background color purple.

*Breakpoints*
- Breakpoints are the sizes where a page design "breaks," and we need to css rules to fix it. 
- Choose breakpoints based on your design and not specific devices. This is best practice. Devices change all the time.
- You can inspect how your page will look on different devices. (show chrome dev tools for different devices)

### Responsive Units
We want to get away from a reliance on using pixels as are only unit.
- % Defines the width in percent of the containing block
- rems, Relative to font-size of the root element
- ems, Relative to the font-size of the element (2em means 2 times the size of the current font)

```
/* Document level adjustments */
html { 
	background: red;
	text-align: center;
	font-size: 14px 
}

h1 {
  font-size: 3rem;
}
h2 {
  font-size: 2.5rem;
}
h3 {
  font-size: 2rem;
}

p{
	font-size:1.25rem;
}

@media (min-width: 500px){
  html { 
  	background: green;
  	font-size: 15px;
  }
}

@media (min-width: 900px) {
  html { 
  	background: blue; 
  	font-size: 17px;
  }
}
```

###You Do
- Don't Touch html!
- Write CSS, in mobile, the two divs should sit on top of each other.
- when the window size is greater than 600, the two divs should site side by side.
- Style the fonts using rems, make sure they look good at each breakpoint.
- Bonus, with the size is greater than 1100, make the the element with the class of sidebar appear.

```CSS
*{
	box-sizing: border-box;
}

.three{
	display: none;
}

html{
	background-color: #eee;
	padding: 0;
	font-family: helvetica;
	font-size: 17px;

}

.wrapper{
	margin: 0 auto;
	width:90%;
	background-color: #fff;
	padding: 2%;
	border-radius: 10px;
}

.box{
	border-radius: 10px;
	padding: 1rem;
	margin-bottom:1rem; 
}
.one{
	background-color: #ADF7B6;
}

.two{
	background-color: #FCDE9C;
}

.three{
	background-color: #9CAFB7;
}

footer{
	text-align: center;
	clear: both;
	margin-top: 2%;
}

@media (min-width: 600px){
	.box{
		float: left;
		display: inline-block;
		width: 49%;
	}

	.two{
		margin-left: 2%;
	}
}

@media (min-width: 1100px){
	.three{
		display: inline-block;
		margin-left: 1%;
		width: 100%;
		margin: 0;
	}

}
```

Homework
[make these](https://s-media-cache-ak0.pinimg.com/564x/dd/08/ec/dd08ec883409c4502e2da0def73679d7.jpg)
-Start with mobile layout
-Make the page responsive, at 