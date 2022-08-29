# Chapter 01

## Structure of Wordpress core files

- There are 2 parts to a Wordpress site: the files and the database (critical to functioning of your site). And the Wordpress files are splited to 2 groups: the core files and the content files.
- Wordpress core files are the "foundational" files that are required for Wordpress to work.
  - index.php: The index file basically loads and initializes all your WordPress files when a page is requested by a user.
  - wp-config.php: This file tells WordPress how to connect to your database. It also sets some global settings for your WordPress site.
  - .htaccess: A server configuration file, WordPress uses it to manage permalinks and redirects.

## Connect to database

- Wordpress uses MySQL as a database management system, and PHP to store and retrieve data from the database
- When you first install WordPress, you are asked to provide a database name, host, username, and password. This information is stored in the configuration file called wp-config.php
- If using phpMyAdmin:
  - Choose a name for database in Create database field
  - Create user in Users tab

## Loop in Wordpress

- is PHP code that displays Wordpress posts
- is used in Wordpress themes to display posts in a webpage
- will display a specified amount of info in a list on a page like blog previews, about pages, ... Inside the loop there are some functions that are run by default to display posts and developers can format the output by using template tags to customize how each post inside the loop is displayed.

## Structure of template - neccessary files

- A WordPress template is a single file found within a WordPress theme. It determines the layout of a single page or group of pages within a theme.
- Templates are files containing HTML and CSS code that defines how content is displayed on WordPress posts and pages, as well as other areas of your WordPress website. They are designed to work within a certain WordPress theme.
- Some neccessary files:
  - index.php: displays main page of a website
  - header.php: displays the header section
  - footer.php: displays the footer section
  - sidebar.php: generates HTML output for the sidebar

## the_title(), get_the_title()

- **the_title()**:
  - fetches the post title without echoing function
  - is recommended to use the_title() in the loop
- **get_the_title()**:
  - requires echoing to display the title of the post (echo get_the_title())
  - is useful outside the loop to retrieve a single post

## get_stylesheet_directory_uri(), get_stylesheet_directory()

- **get_stylesheet_directory_uri()**:
  - Retrieves stylesheet directory URI for the active theme
  - returns a properly-formed URI; in other words, it will be a web-address (starting with http:// or https:// for SSL)
- **get_stylesheet_directory()**:
  - Retrieves stylesheet directory path for the active theme
  - An example output of get_stylesheet_directory() is /home/user/public_html/wp-content/themes/my_theme
  - In the event a child theme is being used, that is the directory that will be returned, not the parent theme directory
