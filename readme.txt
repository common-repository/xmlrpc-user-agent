=== Plugin Name ===
Contributors: koke
Tags: xmlrpc, mobile
Requires at least: 2.7
Tested up to: 3.1
Stable tag: trunk

Store the user agent when posting from XMLRPC and provide functions to themes to make it visible

== Description ==

Store the user agent when posting from XMLRPC and provide functions to themes to make it visible

== Installation ==

1. Upload the `xmlrpc-user-agent` directory to the `/wp-content/plugins/` directory.
2. Activate the plugin through the 'Plugins' menu in WordPress.
3. There is no step 3

== Theme support ==

If you want to use this in your theme, it's really simple:

	<?php if ( function_exists( 'xua_the_agent_link' ) ) : ?>
	    <span class="user-agent">
	        <?php xua_the_agent_link( __( 'Posted via ' ) ) ?>
	    </span>
		<span class="meta-sep">|</span>
	<?php endif; ?>

Available functions with the iOS app as an example:

* `xua_get_the_agent($post_ID)` returns `"WordPress for iOS"`
* `xua_get_the_agent_url($post_ID)` returns `"http://ios.wordpress.org/"`
* `xua_get_the_agent_link($post_ID)` returns `"<a rel='nofollow' href='http://ios.wordpress.org/'>WordPress for iOS</a>"`
* `xua_the_agent()` prints `"WordPress for iOS"`
* `xua_the_agent_link($before = '', $after = '')` prints `"<a rel='nofollow' href='http://ios.wordpress.org/'>WordPress for iOS</a>"`
