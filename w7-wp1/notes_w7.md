# Week 10

## Objectives
  - I can deploy a Wordpress site using Cloud 9.
  - I can administer a Wordpress site.
  - I can build a custom wordpress theme.

## Do Now
  - Skim the following links...
  - https://wordpress.org/about/
  - https://optimizerwp.com/what-is-wordpress/
  - Turn and Talk: Why use wordpress?

## Cloud 9 + Wordpress 
  - Slide, What is cloud 9?
  - Slide, What is wordpress?
  - Slide, Why use cloud 9 with wordpress?
  - Walk Through Setup

## Wordpress Dashboard: Content
  - Slide, Content and Admin links
  - Slide, posts vs pages
  - Walk through adding a post using http://www.wpfill.me/
  - Walk through adding a page
  - WISIWG vs visual
  - Show deleting posts and pages
  - Slide, Your Turn: Add a simple post and a contact page, create a blog page, leave it empty for now
  
## Wordpress Dashboard: Admin
  - Slide, Jargon: Widgets, Plugins, Themes, Navigations
  - Walk through Adding and removing a Widget
    - Add some simple text
  - Walk through adding a custom menu
    - Add the custom menu to the sidebar widget
  - Walk through adding a plugin, show using Akismet
  - Walk through changing the theme, change to another WP starter theme
  - Walk through setting up a static front page and a blog page
  - Your Turn: add the "Contact Form 7" plugin to your site. Add some other widget to the sidebar.
  - Slide, shortcodes
  - Walk through connect contact form 7 to the wp build a form.

## Advanced Plugins
  - Tags and categories
  - Custom Post Types
  - Custom Taxonomies
  
### Walkthrough
  - setting up CPTUI and ACF
  - Create a custom post type for reviews
  - Create a custom field group for reviews
    + Title, Author, Stars, Review
  - assign the field to the post type
  - copy the single.php and archive.php page.
  - create single-review.php and archive-review.php
    + make sure you put in the field php... `<?php the_field('rating'); ?>` 
  - create a custom taxonomy for reviews
    + i.e. nonfiction
  - create an example of review. Test.

# Move to Week 8!!!! 
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

## Final Project
  - Slide, introducing the project
  - Slide, submission details
