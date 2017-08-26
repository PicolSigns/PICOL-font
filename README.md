# The PICOL icons pack as font!

## Installation
```
bower install picol-font
```

## About the content of this repository

* The directory `font` contains the font in different formats
* The directory `css` contains different css files, just for all your needs...<br>You can also avoid to use the `<i>` tag and assign icon classes directly to text elements.
* `demo.html` - The demo html file
* `config.json` - Just a settings file


## Why so many CSS files?
Because we like to fit all your needs! :)
* `picol.css` - is the basic file and is usually enougth. It contains @font-face and character codes definition
* `picol-ie7.css` - if you need IE7 support
* `picol-codes.css` and `picol-ie7-codes.css` - if you like to use your own @font-face rules. This can be very convenient for automated assets build systems.
* `picol-embedded.css` - if you are ok with dirty hack, this file is for you! This is a basic css file, but with embedded WOFF font. To avoid CORS issues in Firefox and IE9+, when fonts are hosted on the separate domain.<br />We strongly recommend to resolve this issue by `Access-Control-Allow-Origin` server headers.<br />Note that data url moved to separate @font-face to avoid problems with <IE9, when string is too long.
* `animation.css` - use it to get ideas about spinner rotation animation.


## Pay attention for Server setup
You MUST setup your Server to reply font files with proper `mime-type`, otherwise some browsers will fail showing fonts.
Apache usually already has necessary settings, but `nginx` and other webservers should be tuned.
Here is list of mime types for our file extentions:

* `eot`: `application/vnd.ms-fontobject`
* `woff`: `application/x-font-woff`
* `ttf`: `application/x-font-ttf`
* `svg`: `image/svg+xml`
