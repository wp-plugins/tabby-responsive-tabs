=== Tabby Responsive Tabs ===
Contributors: numeeja
Donate link: http://cubecolour.co.uk/wp
Tags: tabs, responsive,
Requires at least: 3.7
Tested up to: 3.7.1
Stable tag: 1.0.1
License: GPLv2 / MIT

Tabby enables you to create responsive tabs inside your posts, pages or custom post types by adding simple shortcodes inside the post editor. The tabs transform into an accordion on a viewport 767px wide or less.

== Description ==

* Adds a Horizontal Tabbed interface which changes to Accordion when the viewport width is 767px or less
* Tabs and accordion are created with jQuery
* Supports multiple sets of tabs on same page
* Uses Semantic header and Content markup
* Aria attributes and roles aid screen reader accessibility
* Tabs and content are accessible via keyboard

= Usage: =

There are two shortcodes which should both be used `[tabby]` and `[tabbyending]`

`[tabby title="tabname"]`

replace tabname with the name of your tab.

Add the content of the tab after the `[tabby]` shortcode.

`[tabbyending]`
After the content of the last tab in a tabgroup use a `[tabbyending]` shortcode
		
= Example =
`
[tabby title="First Tab"]
Tabby ipsum dolor sit amet, kitty sunbathe dolor mauris a tristique, feed me nullam stuck in a tree ac faucibus bibendum libero. Jump on the table accumsan et vestibulum fluffy fur pussy libero.

[tabby title="Second Tab"]
Lay down in your way catnip stuck in a tree iaculis, sunbathe orci turpis kittens scratched dolor quis nunc. Vestibulum cras nec attack sniff eat, tempus enim ut adipiscing scratched orci turpis give me fish.

[tabby title="Third Tab"]
Jump sleep in the sink vestibulum climb the curtains attack, sleep on your face sniff attack your ankles etiam give me fish judging you. Sagittis run zzz jump elit nibh, sunbathe enim rip the couch vulputate accumsan.

[tabbyending]
`
You can see the tabs on the [demo page](http://cubecolour.co.uk/tabby-responsive-tabs/ "Tabby Responsive Tabs demo").

If you want to change the style of the tabs / accordion, copy the contents of the plugin's stylesheet into your child theme, or custom styles plugin and make the changes. This will also enable you to change the dimension used as the responsive breakpoint.

If you are using your own custom version of the css, you can prevent the built-in styles from loading by adding the following line to your child theme's functions.php or a custom functionality plugin:

`<?php remove_action('wp_print_styles', 'cc_tabby_css', 30); ?>`


== Installation ==

1. Upload the plugin folder to your '/wp-content/plugins/' directory
1. Activate the plugin through the 'Plugins' menu in WordPress

== Frequently Asked Questions ==

= Where is the plugin's admin page? =

There isn't one. This is a lightweight plugin with no options, so there is no need for an admin page.

= Is it responsive? =

Yes - it should work with responsive themes. It defaults to 100% of the width of the enclosing element.

= How can I change the colours? =

You can copy the css rules from the plugin's stylesheet into your child theme's stylesheet and then customise the colours or use a plugin to add in the css. The css rules should be straighforward to work out.

= OK I've done that, now how do I stop the default styles from loading? =

You can prevent the built-in styles from loading by adding the following line to your child theme's functions.php or a custom functionality plugin:

`<?php remove_action('wp_print_styles', 'cc_tabby_css', 30); ?>`

= Can I display multiple tab groups on a single page? =

Yes you can. As many as you like.

= My Tabs are too high or low =

This is due to differences in the metrics of different fonts and css that is inherited from your theme. You sould be able to overide this with a little additional css in your child theme stylesheet or addded via a custom css plugin.

You can increase specificity to ensure that additional css rules are applied.

The value to look at here are

1. **margin-bottom** for the **.responsive-tabs__list class**
1. **padding-bottom** for the **responsive-tabs__list__item class**

eg:
`
.responsive-tabs-wrapper .responsive-tabs .responsive-tabs__list {
	margin-bottom: 5px;


}

.responsive-tabs-wrapper .responsive-tabs__list__item {
	padding-bottom: 3px;

}
`

Changing these values individually will show you how they interact.

= Can you create a customised stylesheet for me to fit in with the colours of my website? =

I'd love to, but my time is limited and this is beyond of the scope of the free support that I can give on the forums, I can offer this as a paid service. Please send me details of your requirements via the [cubecolour contact form](http://cubecolour.co.uk/contact/ "cubecolour contact form").

= Why do you spell the word 'colour' incorrectly? =

I don't, I'm from England.

= I am using the plugin and love it, how can I show my appreciation? =

You can donate via [my donation page](http://cubecolour.co.uk/wp/ "cubecolour donation page")

If you find the plugin useful I would also appreciate a review on the [plugin review page](http://wordpress.org/support/view/plugin-reviews/tabby-reponsive-tabs/ "Tabby Responsive Tabs plugin reviews")

If it isn't working for you, please read the documentation carefully. If it doesn't address your issue, post a question on the [plugin support forum](http://wordpress.org/support/plugin/tabby-responsive-tabs" Tabby Responsive Tabs plugin support forum") so we can at least have an opportunity to try to get it working before you leave a review.

== Other Notes ==

The plugin is licenced under [GNU GPLv2](http://opensource.org/licenses/GPL-2.0 "GNU GPLv2"), however as the original responsive tabs script was hosted at codepen as a public pen, [hosted at codepen as a public pen](http://blog.codepen.io/legal/licensing/ "hosted at codepen as a public pen")the GPL compatible [MIT license](http://opensource.org/licenses/MIT "MIT license") applies to that component.

== Screenshots ==

1. On a desktop browser the content is displayed within tabs.
1. When the browser width is below the size set in the media query, the tabs are replaced by an accordion.

== Changelog ==

= 1.0.1 =

* Updated js & css

= 1.0.0 =

* Initial Version

== Upgrade Notice ==

= 1.0.1 =

* Updated js & css

= 1.0.0 =

* Initial Version