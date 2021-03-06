=== Menu Icons ===
Contributors: kucrut
Donate Link: http://kucrut.org/#coffee
Tags: menu, nav-menu, icons, navigation
Requires at least: 3.8
Tested up to: 3.8.1
Stable tag: 0.1.5
License: GPLv2
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Easily add icons to your nav menu items.


== Description ==
This plugin gives you the ability to add icons to your menu items, similar to the look of the latest dashboard menu.

= Usage =
1. After the plugin is activated, go to *Appearance* > *Menus* to edit your menus
1. Each menu item will now have new *Icon Type* selection field with their corresponding sub-fields
1. Select the desired icon type
1. Select the icon from the second drop-down
1. Save the menu

= Currently supported icon types =
- Dashicons (WordPress core icon fonts)
- [Genericons](http://genericons.com/) by [Automattic](http://automattic.com/)

= Planned supported icon types =
- [Font awesome](http://fortawesome.github.io/Font-Awesome/)
- Image (attachment file & URL)

= Planned features =
1. Provide modal popup that displays the icons for selection

Development of this plugin is done on [GitHub](https://github.com/kucrut/wp-menu-icons). **Pull requests welcome**. Please see [issues reported](https://github.com/kucrut/wp-menu-icons/issues) there before going to the plugin forum.


== Screenshots ==
1. Icon selection
2. Twenty Fourteen with Dashicons
3. Twenty Fourteen with Genericons
4. Twenty Thirteen with Dashicons
5. Twenty Thirteen with Genericons


== Installation ==

1. Upload `menu-icons` to the `/wp-content/plugins/` directory
1. Activate the plugin through the *Plugins* menu in WordPress


== Frequently Asked Questions ==

= The icons are not showing! =
Make sure that your active theme is using the default walker for displaying the nav menu. If it's using its own custom walker, make sure that the menu item titles are filterable (please consult your theme author about this).

= The icon positions don't look right =
If you're comfortable with editing your theme stylesheet, then you can override the styles from there.
Otherwise, I recommend you to use the [Simple Custom CSS plugin](http://wordpress.org/plugins/simple-custom-css/)

= Is this plugin extendable? =
**Certainly!** Here's how you can remove an icon type from your plugin/theme:
`
function myplugin_remove_menu_icons_type( $types ) {
	unset( $types['genericon'] );
	return $types;
}
add_filter( 'menu_icons_types', 'myplugin_remove_menu_icons_type' );
`

To add a new icon type, take a look at the `type-*.php` files inside the `includes` directory of this plugin.

= Can you please add X icon font? =
Let me know via [GitHub issues](https://github.com/kucrut/wp-menu-icons/issues) and I'll see what I can do.

= Can I disable the extra stylesheet loaded by this plugin? =
**YES!** Simply add the following to your plugin/theme:
`
add_filter( 'menu_icons_load_extra_style', '__return_false' );
`


== Changelog ==
= 0.1.5 =
* Invisible, but important fixes and improvements

= 0.1.4 =
* Fix menu saving

= 0.1.3 =
* Provide icon selection fields on newly added menu items

= 0.1.2 =
* Improve extra stylesheet

= 0.1.1 =
* Improve icon selection UX

= 0.1.0 =
* Initial public release
