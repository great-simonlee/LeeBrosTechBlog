---
layout: post
title: Wordpress Lecture (2) - Theme, Post/Page, Header/Footer
categories: wordpress lecture
author: Simon Lee
permalink: /:categories/:title
---

<strong>[WORDPRESS DEVELOPER UDEMY COURSE][wp-udemy]</strong>  
<strong>[WORDPRESS OFFICIAL SUPPORT DOCUMENTATION][wp-support]</strong>

## 4. Theme

- Path to the theme folder in local: /Users/seunghoonlee/Local Sites/fictional-university/app/public/wp-content/themes/

`screenshot.png` <- Make this file thumbnail with this specific fileName.
![image]({{ site.baseurl }}/assets/img/wp-theme-thumbnail.png)
![image]({{ site.baseurl }}/assets/img/wp-theme-index.png)
![image]({{ site.baseurl }}/assets/img/wp-theme-css.png)
![image]({{ site.baseurl }}/assets/img/wp-theme-site.png)

<br>

## 5. Post / Page

`index.php` // <- Main landing page
{% highlight php %}

<?php 
    while(have_posts()) {
        the_post(); ?>

        <h2><a href="<?php the_permalink(); ?>"><?php the_title(); ?></a></h2>
        <?php the_content(); ?>
        <hr />

<?php }
?>

{% endhighlight %}

`single.php` // <- Single post template
{% highlight php %}

<?php 
    while(have_posts()) {
        the_post(); ?>

        <h2><?php the_title(); ?></h2>
        <?php the_content(); ?>

<?php }
?>

{% endhighlight %}

`page.php` // <- Single page template
{% highlight php %}

<?php 
    while(have_posts()) {
        the_post(); ?>

        <h1>This is a page, not a post.</h1>
        <h2><?php the_title(); ?></h2>
        <?php the_content(); ?>

<?php }
?>

{% endhighlight %}

<br>

## 6. Header / Footer

`header.php` below:
{% highlight php %}

<!DOCTYPE html>
<html lang="en">
    <head>
        <?php wp_head(); ?>
    </head>
    <body>
        <h1>Fictional University</h1>
    </body>
</html>

{% endhighlight %}

`index.php` below:
{% highlight php %}

<?php get_header(); 
    while(have_posts()) {
        the_post(); ?>

        <h2><a href="<?php the_permalink(); ?>"><?php the_title(); ?></a></h2>
        <?php the_content(); ?>
        <hr />

<?php }
get_footer(); ?>

{% endhighlight %}

`footer.php` below:
{% highlight php %}

<h1>This is a footer.</h1>

<?php wp_footer(); ?>
</body>
</html>

{% endhighlight %}

`functions.php` below:
{% highlight php %}

<?php 
    function university_files() {
        wp_enqueue_style('custom-google-font', '//fonts.googleapis.com/css?family=Roboto+Condensed:300,300i,400,400i,700,700i|Roboto:100,300,400,400i,700,700i');
        wp_enqueue_style('font-awesome', '//maxcdn.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css');
        wp_enqueue_style('university_main_styles', get_stylesheet_uri());
    };
    add_action('wp_enqueue_scripts', 'university_files');
?>

{% endhighlight %}

<br>
<br>
<br>

[wp-udemy]: https://www.udemy.com/course/become-a-wordpress-developer-php-javascript/learn/lecture/6896262?start=0#overview
[wp-support]: https://wordpress.org/support/
