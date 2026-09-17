
# PHP

PHP (aka "HyperText Processor") was originally called "personal home page", and is a *very* [web-centric](cs-software-webdev.md) language. For this reason, the code sits neatly inside [files](cs-files.md), but express most commonly through [web browsers](cs-browser.md).

The language has a strange quality of "fixing" errors because it has fallback code in case things fail. This makes it *very* robust, but also more difficult to [debug](cs-software-redesign.md).

## Specific snippets

```php
/* FAVICON HEADER CODE */
add_action('wp_head', 'favicon');
function favicon(){
?>
<link rel="shortcut icon" href="/favicon.ico" type="image/x-icon">
<link rel="icon" href="/favicon.ico" type="image/x-icon">
<?php
};

/* WORDPRESS CHILD THEME */
1st: functions.php with...
<?php
add_action( 'wp_enqueue_scripts', 'enqueue_child_theme_styles', PHP_INT_MAX);
function enqueue_child_theme_styles() {
  wp_enqueue_style( 'parent-style', get_template_directory_uri().'/style.css' );
}
?>
2nd: style.css with...
/*
Theme Name: [THEME] Child
Template: [ORIGINAL THEME NAME]
*/
/* stick all the CSS here */
```
