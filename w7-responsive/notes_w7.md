# Week 7 - Final Project and Responsive Design

## Warm-up
- Read through final project prompt


## Mini-lesson, Responsive design. - 30 min

### Responsive Design
Responsive Web Design is intended to make your web page look beautiful on all devices (desktops, tablets, and phones).

The idea being that the page should respond to the users environment based on screen size, platform, and orientation.

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
```
/* Extra small devices (phones) */
/* Small devices (tablets) */
@media (min-width: 768px) { ... }
/* Medium devices (desktops) */
@media (min-width: 992px) { ... }
/* Large devices (large desktops) */
@media (min-width: 1200px) { ... }
``` 
 
### Responsive Units
We want to get away from a reliance on using pixels as our only unit.
- % Defines the size in percent of the containing block
- ems, defines the size based on the parents size, scaled by the number given. 
  + ex: parent's font-size is 14px, child font-size is 1.5ems, this is equivalent to 21px;
- rems, literally "root ems", size is based off the size of the root (html tag) and scaled by the number
  + ex: root size is 10px, child size is 3rems, this is equivalent to 30px; 
- demo the percent and the rems by adding onto sample code...
 
-final code
```css
/*overriding the rules for different screen sizes*/
@media (min-width: 800px) {
  .logo {
    float: left;
    position: absolute;
    top: -1rem;
  }
  nav {
    float: right;
    width: 60%;
  }
  main {
    margin-top: 8rem;
  }
  .characters {
    display: flex;
    flex-wrap: wrap;
  }
  .card {
    flex-basis: 30%;
    margin: 1%;
  }
}
@media (min-width: 1100px) {
  .wrapper {
    width: 1000px;
    margin: 0 auto;
    padding: 1rem 0;
  }
  header {
    width: 25%;
    float: left;
  }
  .logo {
    position: relative;
    width: 100%;
    top: -15rem;
    background-size: contain;
  }
  .main-menu {
    margin-top: 10rem;
    width: 100%;
  }
  .main-menu ul {
    flex-direction: column;

  }
  main {
    width: 70%;
    float: right;
    margin-top: 0rem;
  }
}
```
 
###You Do
- Don't Touch html!
- Write CSS, in mobile, the two divs should sit on top of each other.
- when the window size is greater than 600, the two divs should site side by side.
- Style the fonts using rems, make sure they look good at each breakpoint.
- Bonus, with the size is greater than 1100, make the element with the class of sidebar appear.

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
# Wordpress Info

## Setting Up MAMP/XAMP
  - slides for why
  - help students run through setup

## Wordpress Dashboard: Content
  - Slide, Content and Admin links
  - Slide, posts vs pages
  - Walk through adding a post using http://www.wpfill.me/
  - Walk through adding a page
  - WISIWG vs visual
  - Show deleting posts and pages
  - Slide, Your Turn: Add a simple post and a contact page, create a blog page, leave it empty for now
  
## Wordpress Dashboard: Admin
  - Slide, Jargon: Widgets, Plugins, Themes, Navigations
  - Walk through Adding and removing a Widget
    - Add some simple text
  - Walk through adding a custom menu
    - Add the custom menu to the sidebar widget
  - Walk through adding a plugin, show using Akismet
  - Walk through changing the theme, change to another WP starter theme
  - Walk through setting up a static front page and a blog page
  - Your Turn: add the "Contact Form 7" plugin to your site. Add some other widget to the sidebar.
  - Slide, shortcodes
  - Walk through connect contact form 7 to the wp build a form.

