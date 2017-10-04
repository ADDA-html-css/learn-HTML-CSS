## Theme Development
  - Slide, wtf is php
  - Slide, Theme development starters
  - Download [naked theme](http://naked-wordpress.bckmn.com/)
  - Upload the theme using the themes admin panel
  - Your Turn: Catch up, install and activate the naked theme. Preview [anatomy of a wp page](https://cdn-images.yoast.com/uploads/2011/01/anatomy-wordpress-yoast.png)
  - Slide, WP page anatomy
  - Slide, the WP loop
  - Add a background to the header
```
   background: linear-gradient(141deg, #0fb8ad 0%, #1fc8db 51%, #2cb5e8 75%);
```
- Walk through using the inspector to change a style. Change the font size of the body
- Show were to add custom CSS to your page.

## Styling the Header
- add a logo to header.php
- style the logo to be 200px wide
- fix the menu bar to the top of the page, might need to add a class to it.
- Show how the inspector to find where a rule is being applied, i.e change the color of the menu items

## Changing the Content
- Show how to remove the site description from the header

### Your Turn
- Change the color of all links on the page, for example the categories in the sidebar.
- Change the footer text to be something else.

## Review templating
- look at home-page.php, what is making the sidebar appear on this page?
- Show how to add the sidebar to page.php

### Your Turn
- add the sidebar to single.php
- Test to make sure it works

## Custom Post Types and Custom Fields
- walk through installing the custom post types plugin
- walk through adding a custom post type for recipes
- walk through adding advanced custom fields plugin
- add an ingredients, directions, and image custom field to the recipe post type
- add a custom tax for the recipe post called type, to hold the type of pizz i.e. sicilian, chicago etc.
- content won't display! so make a single-recipe.php template.
- use `<?php the_field("ingredients"); ?>` to get the ingredients list

### Your Turn
- add the remaining custom fields for the recipe post type
- add some custom style to the page

