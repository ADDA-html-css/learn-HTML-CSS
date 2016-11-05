## Objectives
- I can use Bootstrap to rapidly develop responsive pages with grid systems.
- I can use Bootstrap to create simple navigation

## Do Now

## Stand Up
- Successes
- Struggles
- Show and Tell

## Intro to Bootstrap
- Bootstrap is a HTML/CSS framework for rapid development of responsive, mobile first websites.
- You can think of Bootstrap as a library of components that you can add to your page as needed.
- Bootstrap is very popular, used on a wide variety of sites.
- Show a quick gallery of pages
- Use CDN to include Bootstrap.
`<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" integrity="sha384-1q8mTJOASx8j1Au+a5WDVnPi2lkFfwwEAa8hDDdjZlpLegxhjVME1fgjWPGmkzs7" crossorigin="anonymous">`

## Basic Page
- Show .container and .container-fluid
  ```html
  <div class='container-fluid'></div>
  <section class='container'></section>
  ```
- Create a main and sidebar section, grid system must = 12
  ```
  <div class='col-md-8'></div>
  <div class='col-md-3 col-md-offset-1 well>'
  ```
- add some more styling to the title
- `<div class="container-fluid well text-center'>`

### You Do - A 4 x 3 Grid
  - use characters.html to create a 3 column grid for a medium screen.
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
  - Make it so the grid is 2 columns on extra small screens, hint xs
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
  - use a home link `<a href="index.html" class='navbar-brand'>`

  ```html
  <nav class="navbar">
  <div class="container">
  <div class="navbar-header">
  <a href="#">
    bttf
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

## Override Styles
  - Create and link CSS file to override the default CSS behaviors of Bootstrap
  ```
  /*html *{
    border: 1px solid red;
    }*/
  body{
    padding-top: 10px;
  }
.box{
height: 100px;
}
.nav-pills li.active a, .nav-pills li.active a:focus{
  background-color: #BADA55;
}
.nav-pills>li.active>a:hover{
  background-color: #5B9279;
}
a{
color: #7b4b94;
}
```

## Your Turn
- Use bootstrap to make a nav bar include the following links.
	+ Manchego
	+ Brie
	+ Gouda
	+ Cheddar
	+ Gloucester
	+ Camembert
	+ Parmesan
	+ Asiago
	+ Chevre

```html
<html>
<head>
	<title>Cheese</title>

	<!-- must include this link to use bootstrap -->
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" integrity="sha384-1q8mTJOASx8j1Au+a5WDVnPi2lkFfwwEAa8hDDdjZlpLegxhjVME1fgjWPGmkzs7" crossorigin="anonymous">
</head>
<body>

	<nav class="navbar navbar-default">
		<div class="container">
			<div class="navbar-header">
				<a href="#">
					<span class='navbar-brand glyphicon glyphicon-cutlery'></span>
				</a>
			</div><!-- end navbar header -->

		<ul class="nav navbar-nav">
			
			<li class='nav-item'>
				<a href="#" class='nav-link'>Manchego</a>
			</li>

			<li class='nav-item'>
				<a href="#" class='nav-link'>Brie</a>
			</li>

			<li class='nav-item'>
				<a href="#" class='nav-link'>Gouda</a>
			</li>

			<li class='nav-item'>
				<a href="#" class='nav-link'>Cheddar</a>
			</li>

			<li class='nav-item'>
				<a href="#" class='nav-link'>Gloucester</a>
			</li>

			<li class='nav-item'>
				<a href="#" class='nav-link'>Camembert</a>
			</li>

			<li class='nav-item'>
				<a href="#" class='nav-link'>Parmesan</a>
			</li>

			<li class='nav-item'>
				<a href="#" class='nav-link'>Asiago</a>
			</li>

			<li class='nav-item'>
				<a href="#" class='nav-link'>Chevre</a>
			</li>
		</ul>
		</div><!-- end container -->
	</nav>

	<!-- jquery -->
	<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>

	<!-- bootstrap js library -->
	<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js" integrity="sha384-0mSbJDEHialfmuBBQP6A4Qrprq5OVfW37PRR3j5ELqxss1yVqOtnepnHVP9aJ7xS" crossorigin="anonymous"></script>
</body>
</html>
```

## Collapseable Menu 
- Hamburger Menu, for Mobile
- Starter Menu from do now
- Wrap menu in a div
```html
	<div class="collapse navbar-collapse" id="watch">
		...
	</div>
```
- Create the 'hamburger' using spans
- Notice the id matches the data-toggle
```html
<!-- hamburger button -->
	<button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#watch">
		<span class="icon-bar"></span>
		<span class="icon-bar"></span>
		<span class="icon-bar"></span>
	</button>
```

### Your Turn
- Debug the code below
```html
<nav class="navbar navbar-default">
  <div class="container-fluid">
  
    <div class="navbar-header">
      <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#menu">
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
    </div

    <div class="collapse navbar-collapse" id="collapse-menu">
      <ul class="nav navbar-nav">
        <li><a href="#">Top Bun</a></li>
        <li><a href="#">Special Sauce</a></li>
        <li><a href="#">Lettuce</a></li>
        <li><a href="#">Cheese</a></li>
        <li><a href="#">All Beef Patty</a></li>
        <li><a href="#">Bottom Bun</a></li>
      </ul>
    </section>
</nav>
```

