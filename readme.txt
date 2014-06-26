=== Tabby Responsive Tabs ===
Contributors: numeeja
Donate link: http://cubecolour.co.uk/wp
Tags: tabs, responsive, shortcode, tab
Requires at least: 3.7
Tested up to: 3.9.1
Stable tag: 1.1.1
License: GPLv2 / MIT

Enables you to create responsive tabs inside your posts, pages or custom post types by adding simple shortcodes inside the post editor.

== Description ==

* Adds a set of horizontal tabs which changes to an accordion on narrow viewports
* Tabs and accordion are created with jQuery
* Supports multiple sets of tabs on same page
* Uses Semantic header and Content markup
* Aria attributes and roles aid screen reader accessibility
* Tabs and content are accessible via keyboard

= Tabby Responsive Tabs Customiser Add-on Plugin =
If you need a simple way to customise the display of your tabs, you can now purchase the optional [Tabby Responsive Tabs Customiser](http://cubecolour.co.uk/tabby-responsive-tabs-customiser/ "Tabby Responsive Tabs Customiser") add-on plugin which adds a comprehensive settings panel for Tabby Responsive Tabs fpr creating your unique style without editing any code. It also provides several one-click style presets and adds in the files to enable icons to be included in the your titles.

= Usage: =

There are two shortcodes which should both be used `[tabby]` and `[tabbyending]`

`[tabby title="tabname"]`

*replace tabname with the name of your tab.*

Add the tab content after that. It is recommended to leave a blank line before and after each tabby short code.

Add a `[tabbyending]` shortcode after the content of the last tab in a tabgroup.
		
= Example =
`
[tabby title="First Tab"]

Tabby ipsum dolor sit amet, kitty sunbathe dolor, feed me.

[tabby title="Second Tab"]

Lay down in your way catnip stuck in a tree, sunbathe kittens.

[tabby title="Third Tab"]

sleep in the sink climb the curtains attack, give me fish.
[tabbyending]
`
You can see the tabs on the [demo page](http://cubecolour.co.uk/tabby-responsive-tabs/ "Tabby Responsive Tabs demo").

If you want to change how the tabs and accordion display on your site, you have two options:

1. Use the [Tabby Responsive Tabs Customiser](http://cubecolour.co.uk/tabby-responsive-tabs-customiser/ "Tabby Responsive Tabs Customiser") plugin which provides a very easy way to customise the display of your tabs without needing to edit any code.

2. Copy the contents of the plugin's stylesheet into your child theme or custom styles plugin and make the changes. You also need to prevent the built-in styles from loading by adding the following line to your child theme's functions.php or a custom functionality plugin: `<?php remove_action('wp_print_styles', 'cc_tabby_css', 30); ?>`

= Additional Shortcode attributes =

**Open**
The first (leftmost) tab panel will be open by default in 'tab view' and in 'accordion view'.

If you want a specific tab other than the first to be open by default when the page first loads, you can add the attribute **open="yes"** to the shortcode for that tab:

`
[tabby title="My Tab" open="yes"]
`
**Icon**
You can add the markup required to show an icon alongside a tab title by using the **'icon'** attribute. You will need to use a theme or plugin to add the icon files:
`
[tabby title="My Tab" icon="cog"]
`
This adds a pseudo element before the tab table with the classes "fa" and "fa-cog". Other icon font sets can be used if you ensure the CSS rules target the classes added by the plugin. 

The [Tabby Responsive Tabs Customiser](http://cubecolour.co.uk/tabby-responsive-tabs-customiser/ "Tabby Responsive Tabs Customiser") plugin can be used to add the required Font Awesome files for you.


= Controlling which tab is open depending on the link =
You can use a 'target' URL parameter to set which tab will be open. The value of this parameter is based on tab title specified in the tabby shortcode with punctuation & special characters removed and with spaces replaced by dashes.

If you want to link to a 'contacts' page with a tab titled 'Phone Numbers' open, the url you use in link to this page would look like:
`
yoursite.com/contact/?target=phone-numbers
`
and if you want a tab with the title 'email addresses' to be open, the url would look like:
`
yoursite.com/contact/?target=email-addresses
`

== Installation ==

1. Upload the plugin folder to your '/wp-content/plugins/' directory
1. Activate the plugin through the 'Plugins' menu in WordPress

== Frequently Asked Questions ==

= Why doesn't it work? =

There are a few factors that may cause the plugin not to work.

**Incorrectly formed shortcodes**
If you copied &amp; pasted in the shortcodes from a web page rather than having typed them directly, it is possible that there may be artefacts such as invisible characters in the version copied. Correct this by deleting the shortcodes and try typing them directly instead.

**Plugin or theme conflicts**
To troubleshoot whether you have a plugin or theme conflicting with he plugin, switch to a default theme such as Twenty-Thirteen. If the plugin starts working correctly at that point, you know that the theme is at fault.

If changing the theme makes no difference, deactivate all other plugins. If Tabby Responsive Tabs starts working correctly at that point, discover which plugin caused the issue by reactivating the plugins one by one until tabby responsive tabs stops working again.

*If the plugin isn't working for you*, please read the documentation to check whether your issue is covered. Then review the topics in the [plugin support forum](http://wordpress.org/support/plugin/tabby-responsive-tabs/ "Tabby Responsive Tabs plugin support forum"). You may find an appropriate solution outlined in a resolved topic. If you do not find an answer that enables you to solve your issue, please post a new topic on the forum so we have an opportunity to get it working before you consider leaving a review.

= Where is the plugin's admin page? =

There isn't one. This is a lightweight plugin with no options. If you want to be able to configure your tabs using an admin page, the [Tabby Responsive Tabs Customiser plugin](http://cubecolour.co.uk/tabby-responsive-tabs-customiser/ "Tabby Responsive Tabs Customiser plugin") is available.

= Does it work with responsive Themes? =

Yes - it should work with any well coded responsive theme.

= Does it work with non-responsive Themes? =

The plugin should also work with non-responsive Themes, however this is not recommended and if you are using a non-responsive theme the tabs will not switch to an accordion display on a mobile device.

= How can I change the colours? =

The recommended way is to  copy the css rules from the plugin's stylesheet into your child theme's stylesheet (or a custom CSS plugin) and then customise the colours or use a plugin to add in the css. The css rules should be straighforward to work out.

If you are using a customised version of the plugin's styles, you should also prevent the built-in styles from loading by adding the following line to your child theme's functions.php or a custom functionality plugin:
`<?php remove_action('wp_print_styles', 'cc_tabby_css', 30); ?>`

If you prefer to use a settings page in your WordPress admin to set a custom tab style, you can use the [Tabby Responsive Tabs Customiser plugin](http://cubecolour.co.uk/tabby-responsive-tabs-customiser/ "Tabby Responsive Tabs Customiser plugin") which contains several tab style presets which can be further customised with a comprehensive set of easy to set options.

= Can I change the responsive breakpoint from the default 767px? =

Yes, you'll find where that is set in the css. Refer to the answer above about using custom css.

This value can also be set using the Tabby Responsive Tabs Customiser plugin's admin panel. 

= Why Doesn't my slider work in any tab except the first one? =

Some carousels/sliders plugins render their content with zero height & width if the tab containing the content is not visible on page load. If you need to place a slider in a tab, I would suggest trying Meteor Slides as it seems to work reliably in my tests.

= Why Doesn't my Google Map work in any tab except the first one? =

Some google maps plugins also render their content with zero height & width if the tab containing the content is not visible on page load. I would welcome any suggestions for a workaround that might help with this.

= Can I display multiple tab groups on a single page? =

Yes you can have as many as you like.

= Can I specify which tab is open when the page initially loads? =

Yes, see the documentation for the 'open' shortcode parameter for details.

= Can I specify which tab is open from a link pointing to the page =

Yes, see the documentation for the usage of a 'target' URL parameter in the link.

= I've just updated the plugin and the tabs are now displaying differently =

The default CSS has changed in version 1.0.2 and version 1.1.0. If your tabs now appear 'broken' after an update, this may be due to your site using customised tab styles added to your theme instead of following the recommended method of replacing the default CSS with a complete customised version. To fix this remove the CSS rules you added to your theme to target the tabs and add the custom styles using the method outlined in the documentation.

= Can you create a customised stylesheet for me to fit in with the colours of my website? =

Unfortunately this is beyond of the scope of the free support I can provide. You should be able to style your tabs to integrate closely with your theme using the optional [Tabby Responsive Tabs Customiser](http://cubecolour.co.uk/tabby-responsive-tabs-customiser/ "Tabby Responsive Tabs Customiser") add-on plugin.

Plugin support for Tabby Responsive Tabs is provided at the [plugin's support forum](http://wordpress.org/support/plugin/tabby-responsive-tabs/ "Tabby Responsive Tabs plugin support forum") on WordPress.org.

= Why do you spell the word 'color' incorrectly? =

I don't, I'm from England and 'colour' is the correct spelling.

= I am using the plugin and love it, how can I show my appreciation? =

You can donate any amount via [my donation page](http://cubecolour.co.uk/wp/ "cubecolour donation page") or you could purchase a copy of the [Tabby Responsive Tabs Customiser plugin](http://cubecolour.co.uk/tabby-responsive-tabs-customiser/ "Tabby Responsive Tabs Customiser plugin").

If you find Tabby Responsive Tabs useful, I would also appreciate a review on the [plugin review page](http://wordpress.org/support/view/plugin-reviews/tabby-responsive-tabs/ "Tabby Responsive Tabs plugin reviews")

= Is the Tabby Responsive Tabs Customiser a Premium or Pro Version of Tabby Responsive Tabs? =

No, Tabby Responsive Tabs works great on its own and is ideal for anyone comfortable with editing a child theme. The Tabby Responsive Tabs Customiser plugin is an add-on which is designed to be useful for anyone who wants an easy way to customise how their tabs display without touching any code.

= Why is the Tabby Responsive Tabs Customiser an add-on plugin rather than part of Tabby Responsive Tabs? =

The free Tabby Responsive Tabs plugin was designed as a lightweight plugin for a WordPress developer to add responsive tabs to their WordPress site. The functionality provided by the optional add-on customiser plugin was never intended to be included as part of Tabby Responsive Tabs and is designed to be particularly useful for non-coders.

= How much does the Tabby Responsive Tabs Customiser plugin cost? =

The [Tabby Responsive Tabs Customiser plugin](http://cubecolour.co.uk/tabby-responsive-tabs-customiser/ "Tabby Responsive Tabs Customiser plugin") costs just 15GBP. If you purchase before the end of June 2014, a launch discount of 20% is available with the discount code: TWINKLE20.

== Other Notes ==

The plugin is licenced under [GNU GPLv2](http://opensource.org/licenses/GPL-2.0 "GNU GPLv2"), however as the original responsive tabs script was [hosted at codepen as a public pen](http://blog.codepen.io/legal/licensing/ "hosted at codepen as a public pen"), the GPL compatible [MIT license](http://opensource.org/licenses/MIT "MIT license") applies to that component.

== Screenshots ==

1. On a desktop browser the content is displayed within tabs.
2. When the browser width is below the size set in the media query, the tabs are replaced by an accordion.

== Changelog ==

= 1.1.1 =

* Improvements to default CSS
* Addition of 'open' shortcode attribute to allow tabs other than the first to be open when the page loads
* First tab now is open by default when displayed as accordion 
* Changed links in plugin table
* Get Plugin Version function
* Prevent tabs overlapping if there are too many
* Remove hard coded paragraph tags in tab content & improve
* Added icon font support (Font Awesome needs to be loaded by your theme or another plugin)
* Added functionality to allow target url parameter to control which tab is open on page load.

= 1.0.3 =

* improved theme compatibility with default css

= 1.0.2 =

* enqueue plugin js only when needed
* css for improved specificity

= 1.0.1 =

* Updated js & css

= 1.0.0 =

* Initial Version

== Upgrade Notice ==

= 1.1.1 =

* Added Support for Tabby Responsive Tabs Customiser add-on
* Further improved theme compatibility with default css
* Control which tab is open on page load using short code parameter or url parameter
* Font Awesome icon support in tabs

= 1.0.3 =

* improved theme compatibility with default css

= 1.0.2 =

* improved efficiency - enqueue plugin only when needed
* improved theme compatibility with default css

= 1.0.1 =

* Updated js & css

= 1.0.0 =

* Initial Version