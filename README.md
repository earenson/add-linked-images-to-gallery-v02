add-linked-images-to-gallery-v02
================================

A fork of BBQ Iguana's Wordpress plugin to import and re-attach externally linked images in posts.

I needed a way to import images from content imported from a ColdFusion-powered site, 
where image source URLs didn't include the file extension. Most URLs looked something like:

http://site.com/index?id=92281

and this caused the plugin to remove completely the SRC attribute from the image tag.

I edited the script to use file_get_contents() to grab the file so necessary information
could be extracted from the headers,downloaded, and properly copied to the 'uploads'
directory in wp-content.

Hopefully this helps someone in the future.