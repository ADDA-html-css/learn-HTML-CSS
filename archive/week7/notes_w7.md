# Week 6 Notes

## Objectives
- I can celebrate the success of creating my first website.
- I can design responsive, mobile first pages using media queries.
- I can use responsive image best practices to increase page performance.
- I can employ semantic HTML to optimize my markup.

- [Hongkiat](http://www.hongkiat.com/blog/html-5-semantics/)
- [Treehosue Example](http://blog.teamtreehouse.com/use-html5-sectioning-elements)

## Stand Up
- Successes?
- Struggles?
- Show and tell, design inspiration.

## Mini-Lesson, semantic html
- Semantics, n. the branch of linguistics and logic concerned with meaning.
- Semantics add meaning to our html
- "The Semantic Web provides a common framework that allows data to be shared and reused across application, enterprise, and community boundaries." w3 consortium
- Why? Improve machine and human readibility of markup.
- Human: easier to debug, easier to understand.
- Machine: using semantic html makes it easier for search engine index our page information. This helps Search Engine Optimization.
-Common Semantic tags
```html
<article> Defines an article
<aside>   Defines content aside from the page content
<details> Defines additional details that the user can view or hide
<figcaption>  Defines a caption for a <figure> element
<figure>  Specifies self-contained content, like illustrations, diagrams, photos, code listings, etc.
<footer>  Defines a footer for a document or section
<header>  Specifies a header for a document or section
<main>    Specifies the main content of a document
<mark>    Defines marked/highlighted text
<nav>   Defines navigation links
<section> Defines a section in a document
<summary> Defines a visible heading for a <details> element
<time>    Defines a date/time
<address>   Defines the contact information for the author/owner of a document or an article
<code>    Defines a code block
<em>    Adds emphasis
<mark>    highlight!
<strong>  Bold, with added semantic importance.
```
- build this ![example](http://www.w3schools.com/html/img_sem_elements.gif)

```html
<!-- inside body -->
	<header>
		<h1>Header</h1>
		<nav>navigation</nav>
	</header>
	<section>
		<header>section header</header>
		<time>10:00</time>
		this is a section
		<footer><author>adam</author></footer>
	</section>
	<article>this is an article</article>
	<aside>this is the aside</aside>
	<footer><nav>This is the footer</nav></footer>

```

### Exercise, build a sample blog page
- Create a simple "blog" style page.
- Don't worry about any styling right now.

Create the following elements using semantic html
1. Create a header for the page. Inside the header, put the following elements,
  + a div with the id of logo
  + a nav element
  2. Create a main, inside main put in the following elements
  + A page heading
  + A paragraph with a description of your sweet blog.
  3. Still inside Main Create a fake article. inside the article include the following.
  + A header, with heading title and a date
  + A paragraph with some filler content
  + A footer, with the authors name
  4. Create an aside, use an address tag to put the address of your sweet blog
  5. Create a page footer, include a link to something cool.
  6. Copy and paste your code into this [validator](http://validator.w3.org/#validate_by_input)

Finished Early? Add some *style*

```html
    <header> 
        <div id='logo'> </div> 
            <nav> Navigation </nav> 
        
    </header> 


<main> 
    <header> <h1> Newspaper </h1> </header> 
    <p> Read all about the news here on my blog! </p> 
    <article> 
        <header> <h2> Apple Asks Court to Vacate Order to Unlock iPhone </h1> </header>
        <title> New York Times </title>
        <date> 2/25/16 </date> 
        <p> 
        SAN FRANCISCO — Apple on Thursday filed its formal opposition to the federal court order requiring it to help law enforcement officials break into an iPhone, setting the stage for more legal wrangling in a case that has pitted the world's most valuable company against the United States government.</p>
<p>
In its brief, filed in federal court in California, Apple said that the court should drop an order issued last week that essentially asked the company to create a tool that law enforcement agents can use to break into an iPhone.
</p>
<p>
"Apple strongly supports, and will continue to support, the efforts of law enforcement in pursuing justice against terrorists and other criminals — just as it has in this case and many others," the company said in its motion. "But the unprecedented order requested by the government finds no support in the law and would violate the Constitution."
</p>
        <footer> 
            <author> KATIE BENNER  </author> 
        </footer> 
    </article> 
</main>
        
```

## Mini-lesson 2, Responsive design.
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

Homework
[Responsive Patterns](https://github.com/ADDA-html-css/F_2016_HTMLCSS_HW/tree/master/w7-responsive)
