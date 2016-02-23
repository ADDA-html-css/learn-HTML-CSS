# Week 3

## Objectives
- I can employ semantic HTML to optimize my markup.
- I can use the CSS background properties in all of their glory.
- I can develop advanced layouts using simple grids and flexbox.
- I can use the float property to control object positioning.

## Housekeeping
- Do a git pull, you should have a folder now called week3.

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
<article>	Defines an article
<aside>		Defines content aside from the page content
<details>	Defines additional details that the user can view or hide
<figcaption>	Defines a caption for a <figure> element
<figure>	Specifies self-contained content, like illustrations, diagrams, photos, code listings, etc.
<footer>	Defines a footer for a document or section
<header>	Specifies a header for a document or section
<main>		Specifies the main content of a document
<mark>		Defines marked/highlighted text
<nav>		Defines navigation links
<section>	Defines a section in a document
<summary>	Defines a visible heading for a <details> element
<time>		Defines a date/time
<address>   Defines the contact information for the author/owner of a document or an article
<code>		Defines a code block
<em>		Adds emphasis
<mark>		highlight!
<strong>	Bold, with added semantic importance.
```
- build this ![example](http://www.w3schools.com/html/img_sem_elements.gif)

```html
<!-- inside body -->
<header>
	<h1>Page Title</h1>
	<nav>Page navigation</nav>
</header>
<main>
	<section>
		<header>
			<h2>Section</h2>
			<time>10:00</time>
		</header>
		<p>Something cool to read about</p>
	</section>
	<article>
		<header>
			<h2>Articles</h2>
		</header>
		<p>Cool Article</p>
	</article>
	<aside>
		<p>Sweet Aside</p>
	</aside>
</main>

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
3. Still inside MainCreate a fake article. inside the article include the following.
	+ A header, with heading title and a date
	+ A paragraph with some filler content
	+ A footer, with the authors name
4. Create an aside, use an address tag to put the address of your sweet blog
5. Create a page footer, include a link to something cool.
6. Copy and paste your code into this [validator](http://validator.w3.org/#validate_by_input)

Finished Early? Add some *style*

## Mini-Lesson 2, CSS background property
[resource](https://css-tricks.com/almanac/properties/b/background-image/)
When and Where
- Logo, common to use a CSS background
- background images or textures, show a pattern background
- show a 'parallax' like example

### Example 2
- Make starter code, drop in a logo. Apply a background image, repeat.

## Mini-Lesson 3, Grids
https://css-tricks.com/snippets/css/complete-guide-grid/
https://css-tricks.com/dont-overthink-it-grids/

## Mini-Lesson 4, flexbox

## Floats
http://alistapart.com/article/css-floats-101


## Homework
- Rebuild Tattly
- Simple Responsive layouts, see your pinterest board.