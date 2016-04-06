## Objectives
- I can create interactive elements using Bootstap with javascript.

## Do Now
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

## Dropdown Menus
```html
<ul class="nav navbar-nav">
	<li class="dropdown">
		<a href="#" class="dropdown-toggle" data-toggle="dropdown">Houses <span class="caret"></span></a>
		<ul class="dropdown-menu">
			<li><a href="#gryffindor">Gryffindor</a></li>
			<li><a href="#hufflepuff">Hufflepuff</a></li>
			<li><a href="#ravenclaw">Ravenclaw</a></li>
			<li><a href="#slytherin">Slytherin</a></li>
		</ul>
	</li>
</ul>
```
### You Do
- Create a copy of cheese.html.
- Create a new cheese menu with 2 separate dropdowns
- Include one dropdown for soft cheese
	+ Add chevre, brie, and camembert to this section
- Include one dropdown for hard cheese
	+ Add parmesean, asiago, and gouda to this section


## Collapsable Containers
- Accordian style container

```html
<!-- collapse -->
	<div class="panel-group container" id="accordion" role="tablist" aria-multiselectable="true">
		<h2>Subjects</h2>
		<!-- panel -->
		<div class="panel panel-default">
			<div class="panel-heading" role="tab" id="headingOne">
				<h4 class="panel-title">
					<a role="button" data-toggle="collapse" data-parent="#accordion" href="#transfig">
						Transfiguration
					</a>
				</h4>
			</div>
			<div id="transfig" class="panel-collapse collapse" role="tabpanel">
				<div class="panel-body">
					<p>Transfiguration is the art of changing the form or appearance of an object, and hence this is what this class teaches. Transfiguration is a theory-based subject, including topics such as "Switching Spells" (altering only a part of some object, such as giving a human rabbit's ears); Vanishing Spells (causing an object to completely disappear); and Conjuring Spells (creating objects out of thin air). It is possible to change inanimate objects into animate ones and vice versa — Minerva McGonagall, the class's teacher, transfigures her desk into a pig. The teachers of the class have been Professor Albus Dumbledore (?-1957) and Professor Minerva McGonagall (1957-1998).</p>
				</div>
			</div>
		</div>

		<div class="panel panel-default">
			<div class="panel-heading" role="tab" id="headingTwo">
				<h4 class="panel-title">
					<a role="button" data-toggle="collapse" data-parent="#accordion" href="#dada">
						Defence Against the Dark Arts
					</a>
				</h4>
			</div>
			<div id="dada" class="panel-collapse collapse" role="tabpanel">
				<div class="panel-body">
					<p>Defence Against the Dark Arts, commonly shortened to D.A.D.A., is the class that teaches students defensive techniques to defend against the Dark Arts, and to be protected from Dark creatures.</p>

					<p>The subject has an extraordinarily high turnover of staff members — throughout Harry Potter's time at Hogwarts, no Defence Against the Dark Arts teacher has remained at Hogwarts for more than one school year. These included Quirinus Quirrell, Gilderoy Lockhart, Remus Lupin, Bartemius Crouch Jr impersonating Alastor "Mad-Eye" Moody, Dolores Umbridge, Severus Snape, and Amycus Carrow. Hagrid suggested that "They're startin' ter think the job's jinxed. No one's lasted long for a while now." Dumbledore suggested that Voldemort cursed the position because his application for it was rejected. The position had also been coveted by Snape, but he was denied the position as well. Snape was finally appointed D.A.D.A. professor in 1996. After the end of the Second Wizarding War, the jinx on the position was lifted. Harry Potter would occasionally come to the class to give lectures on the subject.</p>
				</div>
			</div>
		</div>

	</div><!-- end panel group -->
```
### You Do
- Add another panel for potions

## Carousel
- Bootstrap comes with a built in image carosel

```html
	<div class="container">
		<div id="slider" class="carousel slide" data-ride="carousel" data-interval="3000">
	  <!-- Indicators -->
	  <!-- 
	  <ol class="carousel-indicators">
	    <li data-target="#slider" data-slide-to="0" class="active"></li>
	    <li data-target="#slider" data-slide-to="1"></li>
	    <li data-target="#slider" data-slide-to="2"></li>
	  </ol>
 -->

  <!-- Wrapper for slides -->
  <div class="carousel-inner" role="listbox">
    
    <div class="item active">
      <img class="img-responsive" src="http://www.thestudyabroadportal.com/studyabroadblog/wp-content/uploads/2014/08/Hogwarts-castle-harry-potter-166431.jpg">
      <div class="carousel-caption">
        <h1>Welcome to Hogwarts!</h1>
      </div>
    </div>

    <div class="item">
      <img class="img-responsive" src="http://vignette2.wikia.nocookie.net/harrypotter/images/4/47/Hogwarts-dh2.jpg/revision/latest?cb=20110421152732">
      <div class="carousel-caption">
      </div>
    </div>
  </div>


  <!-- Controls -->
<!--   <a class="left carousel-control" href="#slider" role="button" data-slide="prev">
    <span class="glyphicon glyphicon-chevron-left"></span>
  </a>
  <a class="right carousel-control" href="#slider" role="button" data-slide="next">
    <span class="glyphicon glyphicon-chevron-right"></span>
  </a>
 -->
</div>
```

### You Do
- Add another image to the slider.
- Add caption and title to the images.
- Bonus! Look at the bootstrap docs. You can add fancy control buttons! 


