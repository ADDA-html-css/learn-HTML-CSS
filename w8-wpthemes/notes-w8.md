# Week 8 - Wordpress Themes and Final Project

## Objectives
- I can understand how to create themes using wordpress child themes.
- I can start working on my final project.

## Warm-Up
Look over final project prompt. Discuss ideas with someone near you.

## WP Child Themes
Go over Slides for Child themes

Walking through creating a theme.
- In finder, make a new folder, ixion-child
- In atom, make a new file in this folder called style.css
- add the following code to this,
```css
/*
 Theme Name: Ixion Child Theme
  Template: ixion
*/

/* this rule is just for testing, delete once you know the style is being applied */
body {
  background-color: blue;
}
```
- explain this file
- next add the functions.php file
- explain how the functions file works.
- Pause here, let everyone get this working and get to a blue screen.

Add this to the child theme css to alter the theme
```css
a,
a:visited,
a:hover {
  color: #F26419
}

a:visited {
  color: #F26419
}

.widget {
	background: #eee;
}
```

## Going Further
You can edit more than just styles. You can edit the structure and content of the page.

Wordpress doesn't have any html files, instead you will see a bunch of php files. These files include html. What is happening is that php builds the html on the server, then sends it to the browser.

Themes often have a modular design, parts of the page live in different files, i.e. header, footer, sidebar.

To change the structure of the page, you will have to have a copy of that page to override the parent theme. This will be a little different for each theme.

Depending on time, show how to do this with ixion-child?
- find the footer.php page.
- create a copy of it and add to the ixion-child, follow the exact structure, components/footer/site-info
- edit it, reload to see changes.

## Introduce Final Projects
Slides
