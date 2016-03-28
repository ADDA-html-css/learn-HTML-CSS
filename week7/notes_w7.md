## Objectives
- I can use Bootstrap to rapidly develop responsive pages with grid systems.
- I can use Bootstrap to create simple navigation 

## Do Now

## Stand Up
- Successes
- Struggles
- Show and Tell

## Intro to Bootstrap
- Bootstrap is a HTML/CSS framework	for rapid development of responsive, mobile first websites.
- You can think of Bootstrap as a library of components that you can add to your page as needed.
- Bootstrap is very popular, used on a wide variety of sites.
- Show a quick gallery of pages
- Use CDN to include Bootstrap.
`<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" integrity="sha384-1q8mTJOASx8j1Au+a5WDVnPi2lkFfwwEAa8hDDdjZlpLegxhjVME1fgjWPGmkzs7" crossorigin="anonymous">`

## Basic Page
- Show .container and .container-fluid
- Show how to use .well to set the the section apart.
- Create a main and sidebar section,
```
<div class='container-fluid'></div>
<section class='container'></section>
<div class='col-md-8'></div>
<div class='col-md-8 col-md-offset-1'
```

### You Do - A 4 x 3 Grid
- use characters.html to create a 4 x 3 grid for a medium screen. 
- don't worry about offsets
- solution

```html
<div class='container-fluid well text-center'>
		<h1>Back to the Future Trilogy</h1>
		<h2>Character List</h2>
	</div>
	<section class='container text-center'>
		<div class='col-md-4'>
			<h3>Marty McFly</h3>
		</div>
		<div class='col-md-4'>
			<h3>Emmett "Doc" Brown</h3>
		</div>
		<div class='col-md-4'>
			<h3>Biff Tannen</h3>
		</div>
		<div class='col-md-4'>
			<h3>George McFly</h3>
		</div>
		<div class='col-md-4'>
			<h3>Lorraine Baines-McFly</h3>
		</div>
		<div class='col-md-4'>
			<h3>Jennifer Parker</h3>
		</div>
		<div class='col-md-4'>
			<h3>Marty (Jr.)</h3>
		</div>
		<div class='col-md-4'>
			<h3>Douglas J. Needles</h3>
		</div>
		<div class='col-md-4'>
			<h3>Goldie Wilson</h3>
		</div>
		<div class='col-md-4'>
			<h3>Buford "Mad Dog" Tannen</h3>
		</div>
		<div class='col-md-4'>
			<h3>Griff</h3>
		</div>
		<div class='col-md-4'>
			<h3>Gerald Strickland</h3>
		</div>
	</section>
```

## Making the Grid Responsive
- Goal: Make the grid be 4x3 at md and lg, 3x4 on sm, and 1x12 on xs
- Show how to use row class, wrap row around something that makes up a 12 col row.

```html
	<div class='container-fluid well text-center'>
		<h1>Back to the Future Trilogy</h1>
		<h2>Character List</h2>
	</div>
	<section class='container text-center'>
		<div class='row'>
			<div class='col-md-4 col-sm-3'>
				<h3>Marty McFly</h3>
			</div>
			<div class='col-md-4 col-sm-3'>
				<h3>Emmett "Doc" Brown</h3>
			</div>
			<div class='col-md-4 col-sm-3'>
				<h3>Biff Tannen</h3>
			</div>
		</div>
		
		<div class='row'>
			<div class='col-md-4 col-sm-3'>
				<h3>George McFly</h3>
			</div>
			<div class='col-md-4 col-sm-3'>
				<h3>Lorraine Baines-McFly</h3>
			</div>
			<div class='col-md-4 col-sm-3'>
				<h3>Jennifer Parker</h3>
			</div>
		</div>
		
		<div class='row'>
			<div class='col-md-4 col-sm-3'>
				<h3>Marty (Jr.)</h3>
			</div>
			<div class='col-md-4 col-sm-3'>
				<h3>Douglas J. Needles</h3>
			</div>
			<div class='col-md-4 col-sm-3'>
				<h3>Goldie Wilson</h3>
			</div>
		</div>

		<div class='row'>
			<div class='col-md-4 col-sm-3'>
				<h3>Buford "Mad Dog" Tannen</h3>
			</div>
			<div class='col-md-4 col-sm-3'>
				<h3>Griff</h3>
			</div>
			<div class='col-md-4 col-sm-3'>
				<h3>Gerald Strickland</h3>
			</div>
		</div>
```

### You Do
- Make it so the grid is 2x6 on extra small screens, hint xs
- Answer: Add `col-xs-6`

## Adding a Nav
- as many as you want
- Basic Nav
```
<ul class='nav navbar-nav nav-pills'>
		<li class='nav-item'>
			<a class="nav-link" href="bttf1.html">1</a>
		</li>
		<li class='nav-item'>
			<a class="nav-link">2</a>
		</li>
		<li class='nav-item'>
			<a class="nav-link">3</a>
		</li>
	</ul>
```
- introduce navbars
- add container
- add brand and navbar header `<div class="navbar-header">`
- use a home link <a href="index.html" class='navbar-brand'>
```html
<nav class="navbar">
	<div class="container">
		<div class="navbar-header">
			<a href="#">
				<span class="glyphicon glyphicon-film navbar-brand"></span>
				
			</a>
		</div>

	<ul class='nav navbar-nav nav-pills'>
		<li class='nav-item'>
			<a class="nav-link" href="bttf1.html">1</a>
		</li>
		<li class='nav-item'>
			<a class="nav-link">2</a>
		</li>
		<li class='nav-item'>
			<a class="nav-link">3</a>
		</li>
		<li class-'nav-item'>
			<a class="nave-link" href="characters.html">Characters</a>
		</li>
	</ul>
</div>

</nav>

```

## Glyphs
- introduce glphicons `<span class="glyphicon glyphicon-film navbar-brand"></span>`
```html
<a href="#">
	<span class="glyphicon glyphicon-film navbar-brand"></span>				
</a>
```

## HW
- [Accept Invite](https://classroom.github.com/assignment-invitations/50017d425b192b1dc649c87bbf036cfc)