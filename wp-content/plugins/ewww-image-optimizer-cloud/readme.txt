=== EWWW Image Optimizer Cloud ===
Contributors: nosilver4u
Tags: image, compress, optimize, optimization, lossless, photo, picture, seo, jpegmini, tinypng, tinyjpg, webp, wp-cli
Requires at least: 4.4
Tested up to: 4.7.2
Stable tag: 3.2.6
License: GPLv3

Reduce image sizes for images within WordPress including NextGEN, GRAND FlAGallery, FooGallery and more via EWWW IO API.

== Description ==

EWWW Image Optimizer Cloud is a WordPress plugin that will automatically optimize your images as you upload them to your blog. It can optimize the images that you have already uploaded, convert your images automatically to the file format that will produce the smallest image size, and even apply lossy reductions for PNG and JPG images for high compression while retaining image quality.

**Why use EWWW Image Optimizer Cloud?**

1. **Your pages WILL load faster.** Smaller image sizes means faster page loads. Faster page loads means more revenue, and who doesn't want that?
1. **Faster backups.** Smaller image sizes also means faster backups.
1. **Less bandwidth usage.** Optimizing your images can save you hundreds of KB per image, which means significantly less bandwidth usage.
1. **Better Privacy.** The cloud servers do not store any images after optimization is complete, and you retain all rights to any images processed via the cloud service.
1. **Root access not needed** No binaries needed on your local server, so it works on any hosting platform.
1. **Optimize everything** With the wp_image_editor class extension, and the ability to specify your own folders for scanning, any image in Wordpress can be optimized.

By default, EWWW Image Optimizer Cloud uses lossless optimization techniques, so your image quality will be exactly the same before and after the optimization. The only thing that will change is your file size. The one small exception to this is GIF animations. While the optimization is technically lossless, you will not be able to properly edit the animation again without performing an --unoptimize operation with gifsicle. The gif2png and jpg2png conversions are also lossless but the png2jpg process is not lossless. The lossy optimization for JPG and PNG files uses sophisticated algorithms to minimize perceptual quality loss, which is vastly different than setting a static quality/compression level.

Images are optimized via cloud servers that utilize the latest tools available in lossless or lossy mode. Your images can optionally be converted to the most suitable file format.

EWWW Image Optimizer Cloud offloads all optimization to designated servers which will allow the plugin to work on any hosting platform. The lossy compression options use special algorithms to gain maximum compression with minimal loss of quality. Using the EWWW I.O. Cloud can also be desirable if you cannot, or do not want to use the exec() function on your server, or prefer to offload the cpu demands of optimization for any reason. This is an ideal setup for web developers who can install this plugin for their clients with no risk due to the potentially insecure exec() function.

If you want to optimize images on your own server without using the API, see the [EWWW Image Optimizer](http://wordpress.org/plugins/ewww-image-optimizer/).

= Support =

If you need assistance using the plugin, please visit our [Support Page](https://ewww.io/contact-us/). The forums are community supported only.

= Bulk Optimize = 

Optimize all your images from a single page using the Bulk Scanner. This includes the Media Library, your theme, and a handful of pre-configured folders (see Optimize Everything Else below). Officially supported galleries (GRAND FlaGallery, NextCellent, and NextGEN) have their own Bulk Optimize pages.  

= Skips Previously Optimized Images = 

All optimized images are stored in the database so that the plugin does not attempt to re-optimize them unless they are modified. On the Bulk Optimize page you can view a list of already optimized images. You may also remove individual images from the list, or use the Force optimize option to override the default behavior. The re-optimize links on the Media Library page also force the plugin to ignore the previous optimization status of images. 

= WP Image Editor = 

All images created by the built-in WP_Image_Editor class will be automatically optimized. Current implementations are GD, Imagick, and Gmagick. Images optimized via this class include Animated GIF Resize, BuddyPress Activity Plus (thumbs), Easy Watermark, Hammy, Imsanity, MediaPress, Meta Slider, MyArcadePlugin, OTF Regenerate Thumbnails, Regenerate Thumbnails, Simple Image Sizes, WP Retina 2x, WP RSS Aggregator and probably countless others. If you are not sure if a plugin uses WP_Image_Editor, send an inquiry via the support page.

= Optimize Everything Else =

Site admins can specify any folder within their WordPress folder to be optimized. The Bulk Scan under Media->Bulk Optimize will optimize theme images, BuddyPress avatars, BuddyPress Activity Plus images, Meta Slider slides, WP Symposium images, GD bbPress attachments, Grand Media Galleries, and any user-specified folders. Additionally, this tool can run on an hourly basis via wp_cron to keep newly uploaded images optimized. Scheduled optimization should not be used for any plugin that uses the built-in Wordpress image functions.

= WebP Images =

Can generate WebP versions of your images, and enables you to serve even smaller images to supported browsers. Several methods are available for serving WebP images, including Apache-compatible rewrite rules and our Alternative WebP Rewriting option compatible with caches and CDNs. Also works with the WebP option in the Cache Enabler plugin from KeyCDN.

= WP-CLI =

Allows you to run all Bulk Optimization processes from your command line, instead of the web interface. It is much faster, and allows you to do things like run it in 'screen' or via regular cron (instead of wp-cron, which can be unpredictable on low-traffic sites). Install WP-CLI from wp-cli.org, and run 'wp-cli.phar help ewwwio optimize' for more information. 

= FooGallery =

All images uploaded and cached by FooGallery are automatically optimized. Previous uploads can be optimized by running the Media Library Bulk Optimize. Previously cached images can be optimized by entering the wp-content/uploads/cache/ folder under Folders to Optimize and running a Scan & Optimize from the Bulk Optimize page.

= NextGEN Gallery =

Features optimization on upload capability, re-optimization, and bulk optimizing. The NextGEN Bulk Optimize function is located near the bottom of the NextGEN menu, and will optimize all images in all galleries. It is also possible to optimize groups of images in a gallery, or multiple galleries at once.

= NextCellent Gallery =

Features all the same capability as NextGEN, and is the continuation of legacy (1.9.x) NextGEN support.

= GRAND Flash Album Gallery =

Features optimization on upload capability, re-optimization, and bulk optimizing. The Bulk Optimize function is located near the bottom of the FlAGallery menu, and will optimize all images in all galleries. It is also possible to optimize groups of images in a gallery, or multiple galleries at once.

= Image Store =

Uploads are automatically optimized. Look for Optimize under the Image Store (Galleries) menu to see status of optimization and for re-optimization and bulk-optimization options. Using the Bulk Optimization tool under Media Library automatically includes all Image Store uploads.

= CDN Support =

Uploads to Amazon S3, Azure Storage, Cloudinary, and Dreamspeed CDN are optimized. All pull mode CDNs like Cloudflare, KeyCDN, MaxCDN, and Sucuri CloudProxy are also supported.

= Translations =

Huge thanks to all our translators! If you would like to help translate this plugin (new or existing translations), you can do so here: https://translate.wordpress.org/projects/wp-plugins/ewww-image-optimizer-cloud
To receive updates when new strings are available for translation, you can signup here: https://ewww.io/register/

== Installation ==

1. Upload the 'ewww-image-optimizer-cloud' plugin to your '/wp-content/plugins/' directory.
1. Activate the plugin through the 'Plugins' menu in WordPress.
1. Purchase an API key via https://ewww.io/plans/.
1. Enter your API key on the plugin settings page.
1. *Optional* Visit the settings page to adjust compression levels and turn on advanced optimization features.
1. Done!

Additional documentation can be found at http://docs.ewww.io. If you need further assistance using the plugin, please visit our [Support Page](https://ewww.io/contact-us/). The forums are community supported only.

== Frequently Asked Questions ==

= Google Pagespeed says my images need compressing or resizing, but I already optimized all my images. What do I do? =

http://docs.ewww.io/article/5-pagespeed-says-my-images-need-more-work

= Does the plugin replace existing images? =

Yes, but only if the optimized version is smaller. The plugin should NEVER create a larger image.

= Can I resize my images with this plugin? =

Yes you can, check the Advanced settings.

= Can I lower the compression setting for JPGs to save more space? =

The lossy JPG optimization using TinyJPG and JPEGmini will determine the ideal quality setting and give you the best results, but you can also adjust the default quality for conversion and resizing. More information: http://docs.ewww.io/article/12-jpq-quality-and-wordpress

= The bulk optimizer doesn't seem to be working, what can I do? =

If it doesn't seem to work at all, check for javascript problems using the developer console in Firefox or Chrome. If it is not working just on some images, you may need to increase the setting max_execution_time in your php.ini file. There are also other timeouts with Apache, and possibly other limitations of your webhost. If you've tried everything else, the last thing to look for is large PNG files. In my tests on a shared hosting setup, "large" is anything over 300 KB. You can first try decreasing the PNG optimization level in the settings. If that doesn't work, perhaps you ought to convert that PNG to JPG or set a max PNG optimization size. Screenshots are often done as PNG files, but that is a poor choice for anything with photographic elements.
[youtube https://www.youtube.com/watch?v=V4U2hQlmkvQ]

= I want to know more about image optimization. =

That's not really a question, but since I made it up, I'll answer it. See these resources:
http://developer.yahoo.com/performance/rules.html#opt_images  
https://developers.google.com/speed/docs/insights/OptimizeImages  

== Changelog ==

* Feature requests can be submitted via https://ewww.io/contact-us/ and commented on here: https://trello.com/b/Fp81dWof/ewww-image-optimizer
* If you would like to help translate this plugin in your language, get started here: https://translate.wordpress.org/projects/wp-plugins/ewww-image-optimizer-cloud/

= 3.2.6 =
* changed: time elapsed test now runs every 10 attachments
* fixed: time elapsed test during bulk scan was not running every X number of images
* fixed: scan was not returning results directly after detecting a broken attachment
* fixed: maximum number of rows for ewwwio_images was not high enough, bumped to 4 billion
* fixed: db migration function was not linking records to attachments properly

= 3.2.5 =
* fixed: converting PNG to JPG with GD did not properly convert resizes
* fixed: broken attachment metadata could halt the bulk scanner
* fixed: background optimization running when sleep is disabled

= 3.2.4 =
* changed: when license has been exceeded, visiting the settings page flushes the license cache
* fixed: warnings for illegal string offsets
* fixed: regression with the dreaded duplicate key name
* fixed: scheduled optimization could run during bulk optimization, causing unexpected results

= 3.2.3 =
* added: image linker for media images optimized using scheduled optimizer or the old Scan and Optimize
* added: low memory mode for bulk scanner with notice to user
* added: ability to manually configure how much memory is available using EWWW_MEMORY_LIMIT constant
* added: variable query counts depending on available memory
* added: ability to view and remove debug.log from settings page
* added: ability to manually disable background optimization using EWWW_DISABLE_ASYNC constant
* changed: check every 100 images during scan to avoid timeouts and memory errors
* changed: additional folder scanner can stop & resume mid-folder
* fixed: bulk scanner updates timestamps when it should not
* fixed: special characters are mangled during database insert on some systems
* fixed: pending images that were already optimized were not cleared from queue
* fixed: images with invalid updated dates in database corrected
* fixed: images that should be excluded from optimization were still queued even though they would not be optimized
* fixed: results column was too short, causing bulk optimization to get stuck on an image that was previously optimized
* fixed: if two different attachments reference the same image, duplicate records could be inserted into database during media scan

= 3.2.2 =
* added: estimated time remaining on bulk optimize
* added: 'ewww_image_optimizer_image_resized' hook added right after resizing, before original is overwritten
* changed: image resizing is performed before any thumbnails are generated for reduced resource usage
* fixed: compatibility with Azure storage plugin
* fixed: bulk optimization not playing nice with WP Offload S3
* fixed: optimization results for resized original not displayed when using Imsanity
* fixed: bulk optimization not working for utf-8 filenames - credit to devsporadic on github
* fixed: retina paths not tested correctly in some odd cases
* removed: generating full-size retina image automatically when resizing images and WP Retina 2x Pro detected

= 3.2.1 =
* fixed: really old versions of PHP (less than 5.5) cannot cope with using empty() on a function return value
* fixed: queue of images not reset when reloading bulk page

= 3.2.0 =
* added: option to ignore folders when optimizing
* added: ability to disable optimization or creation for any or all previews of PDF files in WordPress 4.7
* added: optimization results detail for all resizes of an image in media library list view
* added: automatic metadata rebuilding for broken image attachments in media library during bulk scan
* changed: bulk optimizers for media library and everything else have been merged
* changed: bulk optimization processes images in batches for fewer AJAX requests to your server
* changed: optimization results no longer stored in attachment metadata
* changed: populating list of optimized images during scan uses less memory
* changed: obsolete options removed from database
* changed: if scan is interrupted, it will automatically retry
* changed: excessive re-optimization warning ignores theme and plugin images
* changed: if full-size image is converted, all resizes, custom sizes, and retina images will be converted
* changed: conversion will not inject extra numbers if possible
* changed: image results message generated on demand to avoid stale results
* removed: unoptimized images page, bulk scanner is now able to accomplish the job more accurately
* fixed: parallel mode prevents successful conversion
* fixed: image paths with special characters stored incorrectly in database
* fixed: parallel optimization for retina and custom sizes was missing parameters
* fixed: bulk optimizing a single image was broken, but who does that anyway?
* fixed: notice when LIBXML_VERSION is undefined and alt webp is enabled
* fixed: invalid default value for timestamp in db records
* fixed: one-click optimization returns no error when running out of API credits
* fixed: background mode was not checked properly in nextgen and flagallery functions
* fixed: incorrect mimetype set after image conversion for PNG2JPG
* fixed: using getimagesize on pdf files

== Upgrade Notice ==

= 3.2.3 =
* The bulk scanner will now attempt to auto-detect how much memory is available to avoid exceeding memory limits within PHP. Some webhosts do not allow the ini_get() function, so the plugin will fall back to the current memory usage plug 16MB. If you need to set the memory limit for EWWW IO manually, you can do so with the EWWW_MEMORY_LIMIT constant in wp-config.php.

= 2.8.1 =
* KeyCDN added support for WebP images generated by EWWW I.O. into the Cache Enabler plugin. If you are using Cache Enabler, you may wish to use their WebP option instead of Alt WebP Rewriting. Works very nicely with CDNs and is a nice simple caching plugin.

= 2.8.0 =
* added: resizing for uploaded images, set max width and height and optionally resize all existing images
* changed: settings have been revamped, please check to make sure your settings were migrated properly
* added: PDF optimization introduced (from 2.7 actually)

== Contact and Credits ==

Written by [Shane Bishop](https://ewww.io). Based upon CW Image Optimizer, which was written by [Jacob Allred](http://www.jacoballred.com/) at [Corban Works, LLC](http://www.corbanworks.com/). CW Image Optimizer was based on WP Smush.it.  
[Hammer](http://thenounproject.com/noun/hammer/#icon-No1306) designed by [John Caserta](http://thenounproject.com/johncaserta) from The Noun Project.  
[Images](http://thenounproject.com/noun/images/#icon-No22772) designed by [Simon Henrotte](http://thenounproject.com/Gizmodesbois) from The Noun Project.
