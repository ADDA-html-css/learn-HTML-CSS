# Week 6

## Objective
-Build something from start to finish

## Mini-Lesson: Starting from Scratch
- Start with the HTML
- Show wireframes
- Use Semantic HTML for the wireframes
- Start styling
- mobile first, start with footer
  + hide the copyright
  + style the logo, background image
  + style the menu
- style the page wrap div
- style the main title
- start the media queries
  + size and center the page wrapper 
  + make the title bigger
  + float the sidebar left
  + float the main left
  + style the footer
  + change the size of the logo
  + put the nav to the right
  + display the copyright
  + add the page wrap to the footer
  + resize the page wrap

## Final HTML
```
/* blue #0F3589 */
/* grey #CECECE */
/* red #FF5E5B */

body {
  font-family: "Ovo", times;
  margin-bottom: 200px;
}

.main-title {
  font-size: 50px;
  text-align: center;
  color: #0F3589;
}

.page-wrap {
  padding: 0 15px;
}

.page-wrap h3 {
  margin: 0;
  color: #FF5E5B;
}

aside h3 {
  font-size: 30px;
}

article {
  line-height: 1.25;
  font-size: 20px;
}

/* style all the footer stuff*/
footer {
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  background-color: #0F3589;
}

.logo {
  width: 100px;
  height: 100px;
  display: block;
  margin: 0 auto;
  background-color: green;
  margin-top: 15px;
  background-image: url('./images/belle.jpg');
  background-size: cover;
  background-position: center;
  border-radius: 50%;
}

nav {
  display: inline-block;
}

footer h3 {
  text-align: center;
  display: none;
}

footer nav {
  width: 100%;
}

footer nav ul {
  padding: 0;
  margin: 15px 0;
  height: 40px;
  list-style-type: none;
}

footer nav ul li {
  display: inline-block;
  width: 49%;
}

footer nav ul li a {
  width: 100%;
  text-align: center;
  display: block;
  font-size: 20px;
  text-decoration: none;
  color: #CECECE;
  padding: 10px;
  box-sizing: border-box;
  transition: font-size 0.5s ease-out, margin-top 0.5s;
}

footer nav ul li a:hover {
  color: #FF5E5B;
  font-size: 30px;
  margin-top: -10px;
}

@media (min-width: 650px) {
  .page-wrap {
    max-width: 900px;
    margin: 0 auto;
  }
  .main-title {
    font-size: 100px;
    margin-bottom: 0px;
  }
  aside {
    float: left;
    width: 20%;
    margin-right: 5%;
  }
  main {
    width: 75%;
    float: left;
  }
  footer .page-wrap {
    width: 600px;
  }
  footer nav {
    width: 300px;
    float: right;
    margin-top: 45px;
  }
  .logo {
    width: 125px;
    height: 125px;
    float: left;
    margin-left: 50px;
  }
  footer .page-wrap h3 {
    display: block;
    clear: both;
    margin-bottom: 15px;
    color: #CECECE;
    width: 300px;
    float: right;
    font-size: 15px;
  }
}
```

## Final HTMl
```
<html>

<head>
  <title>Belle's Book Reviews</title>
  <link href="https://fonts.googleapis.com/css?family=Ovo" rel="stylesheet">
  <link rel="stylesheet" type="text/css" href="style.css">
</head>

<body>
  <header>
    <h1 class="main-title">Belle's Books</h1>
  </header>

  <div class="page-wrap">
    <aside>
      <h3>Hello.</h3>
    </aside>

    <main>
      <article>
        <p>Blandit. Mollis curae; mus conubia potenti etiam id eu ligula adipiscing. Conubia sociis blandit congue nam molestie bibendum commodo nostra. Ridiculus euismod et mauris pede sagittis posuere mus ridiculus scelerisque adipiscing iaculis consequat. Cum. Arcu nam inceptos interdum natoque congue. Elementum facilisis tellus ornare nunc tempus nisl.</p>

        <p>Fusce magna duis inceptos suscipit molestie aenean. Suspendisse Dictumst, donec nec cras fringilla urna nec. Est placerat dictumst suscipit magnis sit malesuada luctus donec dui. Vulputate. Tristique.</p>

        <p>Neque facilisis. Hendrerit nisi cursus aenean euismod habitasse sociis gravida dignissim odio accumsan lacinia orci. Netus vivamus laoreet. Primis ligula facilisis pulvinar interdum. Augue praesent fusce.</p>
      </article>
    </main>

    <footer>
      <div class="page-wrap">
        <div class="logo"></div>
        <nav class="main-menu">
          <ul>
            <li><a href="#">about</a></li>
            <li><a href="#">reviews</a></li>
          </ul>
        </nav>

        <h3>built with &#9829 2017</h3>
      </div>
    </footer>

</body>

</html>
```
