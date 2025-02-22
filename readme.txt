=== Custom Post Links ===
Contributors:grosbouff
Donate link:http://bit.ly/gbreant
Tags: links,quick links,related links,custom links, post links
Requires at least: 3.5
Tested up to: 4.6.1
Stable tag: trunk
License: GPLv2 or later

Adds a new metabox to the editor, allowing you to attach a set of related links to any post.


== Description ==

This plugin has *moved* to [https://wordpress.org/plugins/post-bookmarks](https://wordpress.org/plugins/post-bookmarks).  Please upgrade !

== Installation ==

1. Upload the plugin to your blog and Activate it.

== Frequently Asked Questions ==

= How can I style a link based on its domain, using CSS ? =

Use the *data-cp-link-domain* attribute, for example : 

`li.cp-links[data-cp-link-domain='wikipedia.org'] .cp-links-favicon {
    background-image: url('https://wikipedia.org/static/favicon/wikipedia.ico');
}`

= How can I change the way links are displayed ? =

Use the filter *cp_links_output_single_link* (located in the **cp_links_output_single_link** function), for example : 

`<?php

function custom_output_single_link($output,$link){
    return $output;
}

add_filter('cp_links_output_single_link','custom_output_single_link',10,2);

?>`

== Screenshots ==

1. Custom Post Links metabox in the backend editor
2. Settings page
3. Links displayed under a post

== Changelog ==

= 2.0.7 =
* cleaner code for blank row link + links tabe actions

= 2.0.6 =
* try to guess the link name from remote page title or domain (ajaxed)
* URL as first column
* better way to load JS

= 2.0.5 =
* Better output styling
* Favicons : Option to automatically load URL pictures from Google API
* New filter ‘cp_links_get_for_post_pre’
* New function ::get_blank_link()

= 2.0.4 =
* minor

= 2.0.3 =
* ignore targets (eg. ’_blank’) if a link is a local link
* backend : use ‘_blank’ target for URLs in the links table
* implemented links targets

= 2.0.2 =
* Importer and admin notice for links from the original [Custom Post Links](https://github.com/daggerhart/custom-post-links) plugin (metas '_custom_post_links').
* new function CP_Links::insert_link()
* Improved function 'cp_links_get_existing_link_id'
* new function ‘cp_links_get_metas’

= 2.0.1 =
* Do not use the same post meta key than than the original [Custom Post Links](https://github.com/daggerhart/custom-post-links) plugin.

= 2.0 =
* custom sorting
* options page
* set the link domain as class in the link output
* display entries in metabox using class CP_Links_List_Table (extends WP_List_Table)
* store / read entries from the Link Manager plugin (Worpress core) instead of metas
* wrapped in a class, better code structure
* use fontAwesome css, deleted drag_handle.png
* various other improvements

= 1.0 =
* Forked from [Custom Post Links](https://github.com/daggerhart/custom-post-links) by Jonathan Daggerhart.

== Upgrade Notice ==

== Localization ==