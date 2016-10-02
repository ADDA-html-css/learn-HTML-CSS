# Week 2 Instructor Notes

## Objectives
- I can investigate and build layouts using the CSS "Box Model" 
- I can use nested targets.

## Housekeeping 
- Using github desktop
- go to homework [repo](https://github.com/ADDA-html-css/F_2016_HTMLCSS_HW)
- create a fork
- clone that fork in desktop
- Go to that location, make a folder with your name
- Copy the folder with starter into your folder, 
- do all your work in this location
- When you are finished, sync, then do a pull request

## Do Now
Find the error!
```html
<body>
	<h2>My Weekend Plans
		<ul>
			<li>sleep</li>
			<li>watch tv</li>
			<li>eat good food
		<ol>
</body>
```

## Stand-up
- Successes?
- Struggles?
- Show and Tell!

## Mini-Lesson 1, classes
```html
<html>
<head>
	<title>Class V. ID</title>
	<link rel="stylesheet" type="text/css" href="idAndClass.css">
</head>
<body>
	<div id="titleDiv">
		<h1>Class v. IDs</p>
	</div>

	<div class="red">
		<p>red text<p>
			<p class="blue">red text?</p>
	</div>

	<h2 class="red">A red header</h2>
	<a href="http://www.facebook.com" class="red">A red link</a>

</body>
</html>

```

```css
	#titleDiv{
		color: green;
	}

	.red{
		color: red;
	}

	.blue{
	background-color: blue;
	}
```

- An ID should be unique to a single html element
- Many elements can share a class
- Analogy: You have an ID, there is no one else should share your ID. You are in this class, but many people can share this class.

### Excercise 1
- Make index.html
- Make three paragraphs, use a text generator
- Make style.css
- Make the first paragraph green
- Make the second paragraph black text (normal) with a silver background
- Make the third paragraph green text and a silver background

Introduce DRY!

## Mini-Lesson 2, Box Model
Show a basic slide of the box model.
[link](http://www.w3schools.com/css/css_boxmodel.asp)

### Exercise 2
** investigate a simple box model and how it effects the layout**
Have two divs that are next to each other, have students open up the inspector on this page
- Make the border larger. What happens? Return to normal.
- Make the padding larger. What happens? Return to normal.
- Make the margin larger. What happens? Return to normal.
- Formulate a theory of what is happening.

Bonus: add a css property, `box-sizing: border-box;` to one of the elements, now change the padding and margin. What happens now?

Have a discussion. Show a computed [example](http://www.sitepoint.com/web-foundations/css-box-model/)

**Cool Trick**
```css
* {
   border: 1px solid red !important;
}
```

## HW
[week 2 HW](https://github.com/ADDA-html-css/F_2016_HTMLCSS_HW/tree/master/week2)

