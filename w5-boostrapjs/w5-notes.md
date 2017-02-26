# Week 5, Boostrap JS

## Objectives
- I can use the Bootstrap card and nav components.
- I can incporate Javascript into a Bootstrap page.

## Cards
```
<!-- this is a simple card block -->
<div class="card">
  <img class="card-img-top" src="">
  <div class="card-block">
    <h4 class="card-title">title</h4>
    <p class="card-text">Some card text</p>
  </div>
</div>
<!-- end card block -->
```
-show how to put an image in the top, use /img/barnard.jpg
- whoa! way to big, add the `w-25` to the card class, this makes the card take 25% of its parent.
- whoa! scrunched, add img-fluid to the image class

Final Code
```
<!-- this is a simple card block -->
<div class="card w-25">
  <img class="card-img-top img-fluid" src="./img/barnard.jpg" alt="Card image cap">
  <div class="card-block">
    <h4 class="card-title">Barnard</h4>
    <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
  </div>
</div>
<!-- end card block -->
```
- cards can be used with the grid structure
- take movies.html and convert to a grid
- wrap cards in a row
- wrap each card in a responsive div, start with `col-md-4`
- play with the screen size, doesn't look great at medium size.
- change to `col-md-6 col-lg-4` 4 columns at lg, 6 at md
- now show how the row breaks, spacing not great, add `mt-4` to give some top margin.

## Navs
### Basic Nav
- common pattern to use a ul as a nav menu,
- pattern, ul gets `nav` class, li gets `nav-item`, the a link gets `nav-link`
- build basic nav

```
<ul class="nav">
<li class="nav-item">
<a class="nav-link active" href="#">Home</a>
</li>
<li class="nav-item">
<a class="nav-link" href="#">About</a>
</li>
<li class="nav-item">
<a class="nav-link" href="#">Resume</a>
</li>
</ul>
```
- Show how to turn to pills

### nav bar
- change previous example to a navbar
- pattern, make a `nav` tag with class of `nav-bar`, ul gets `navbar-nav` class.
- add a brand
- add a div for the content, this is mostly for later to get js toggle

```
  <nav class="navbar navbar-toggleable-md navbar-light bg-faded">

    <a class="navbar-brand" href="#">Adam Driggers</a>
  
  <!-- Div do hold the content of the navbar-->
    <div>
      <ul class="navbar-nav">
        <li class="nav-item">
          <a href="#" class="nav-link active">Home</a>
        </li>

        <li class="nav-item">
          <a href="#" class="nav-link">About</a>
        </li>

        <li class="nav-item">
          <a href="#" class="nav-link">Resume</a>
        </li>
      </ul>
    </div>
  </nav>
```

  - show some other style stuff, `navbar-inverse bg-inverse`
  - show mixed top

### Exercise
  - students build, see slide

  - solution:

```
   <nav class="navbar navbar-toggleable-md navbar-light bg-faded">
      <a class="navbar-brand" href="#">Cheese</a>
      <!-- Div do hold the content of the navbar-->
      <div> 
        <ul class="navbar-nav">
            <li class='nav-item'><a class="nav-link" href='#'>Manchego</a></li>
            <li class='nav-item'><a class="nav-link" href='#'>Brie</a></li>
            <li class='nav-item'><a class="nav-link" href='#'>Gouda</a></li>
            <li class='nav-item'><a class="nav-link" href='#'>Cheddar</a></li>
            <li class='nav-item'><a class="nav-link" href='#'>Gloucester</a></li>
            <li class='nav-item'><a class="nav-link" href='#'>Camembert</a></li>
            <li class='nav-item'><a class="nav-link" href='#'>Parmesan</a></li>
            <li class='nav-item'><a class="nav-link" href='#'>Asiago</a></li>
            <li class='nav-item'><a class="nav-link" href='#'>Chevre</a></li>
        </ul>
      </div>
    </nav>
```

## Using the JS libraries
- Why JS?
- Setup, you have to include js scripts in the bottom of the page.

### Show with menus
- Hamburger Menu
- pattern: add button group. Must have two attributes, `data-toggle` and `data-target`
  + `data-toggle` is an action
  + `data-target` is the id of the element being effected

```<!--  button for hamburger    -->
      <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#hamburger-ex">
        <span class="navbar-toggler-icon"></span>
      </button>
```
- Add an id to the div surrounding the ul, include the following classes
```
 <div class="collapse navbar-collapse" id="hamburger-ex"> 
```

- Complete code...

```
<!-- your navbar goes here -->
    <nav class="navbar navbar-toggleable-md navbar-light bg-faded">
      
<!--  button for hamburger    -->
      <button class="navbar-toggler navbar-toggler-right" type="button" data-toggle="collapse" data-target="#hamburger-ex">
        <span class="navbar-toggler-icon"></span>
      </button>   
      <a class="navbar-brand" href="#">Big Mac</a>
      <!-- Div do hold the content of the navbar-->
      <div class="collapse navbar-collapse" id="hamburger-ex"> 
        <ul class="navbar-nav">
          <li class='nav-item'><a class="nav-link" href='#'>All Beef Patty</a></li>
          <li class='nav-item'><a class="nav-link" href='#'>All Beef Patty</a></li>
          <li class='nav-item'><a class="nav-link" href='#'>Special Sauce</a></li>
          <li class='nav-item'><a class="nav-link" href='#'>Lettuce</a></li>
          <li class='nav-item'><a class="nav-link" href='#'>Cheese</a></li>
          <li class='nav-item'><a class="nav-link" href='#'>Pickles</a></li>
          <li class='nav-item'><a class="nav-link" href='#'>Onion</a></li>
          <li class='nav-item'><a class="nav-link" href='#'>Sesame Seed Bun</a></li>
        </ul>
      </div>
    </nav>
```

### Javascript Jigsaw
- Make a group of 4 people.
- You each get a different piece of the puzzle
    + modal 
    + carosel 
    + tab menu 
    + drop-down
- Spend 15 minutes reading through your puzzle piece
- Make a cool demo in a new thimble project
- Next, take turns sharing your demos, feel free to share files with thimble by publishing.

## Home Work
- Choose a website to redesign with a bad design or one that is not responsive. In canvas post the url and why you choose this website.
- Hint: many of the older gov websites are good candidates, not the sites that Lenny works on ;)
- Wireframe a mobile and desktop layout for your redesign. Bring to class next week.



