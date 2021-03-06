The Lab: The Great Grunt Shootout
=============

This repository contains the source code for the above [Lab episode](http://www.letscodejavascript.com/v3/episodes/lab/1) of James Shore's [Let's Code: Test-Driven JavaScript](http://www.letscodejavascript.com) screencast. Let's Code: Test-Driven JavaScript is a screencast series focused on rigorous, professional JavaScript development.

This episode was focused on comparing [Grunt](http://gruntjs.com/) and [Jake](https://github.com/mde/jake), two automated build tools for JavaScript. Grunt was evaluated in comparison to Jake by reimplementing the [Automatopia project](https://github.com/jamesshore/automatopia)'s primary build script in Grunt.

To evaluate the results yourself, compare `Gruntfile.js` to `Jakefile.js`. For more information, [watch the screencast](http://www.letscodejavascript.com/v3/episodes/lab/1).

*Update, 11 January 2014:* Added a [Gulp](http://gulpjs.com/) implementation of the build. See `Gulpfile.js` and compare it to `Gruntfile.js` and `Jakefile.js`.

Building and Testing
--------------------

Before building for the first time:

1. Install [Node.js](http://nodejs.org/download/).
2. Download and unzip [the source code](https://github.com/jamesshore/automatopia/archive/master.zip) into a convenient directory.
3. All commands must run from the root of the source tree: `cd <directory>`.
4. To cause the build to fail unless certain browsers are tested, edit `REQUIRED_BROWSERS` at the top of `Jakefile.js` and in `requiredBrowsers` config section of `Gruntfile.js`. Otherwise, comment those lines out.

To build (and test):

1. Run `./jake.sh karma` (Unix/Mac) or `jake karma` (Windows) to start the Karma server.
2. Start the browsers you want to test and point each one at `http://localhost:8080`.
3. Run `./jake.sh` (Unix/Mac) or `jake` (Windows) every time you want to build and test.

Use `./grunt.sh` (or `grunt` on Windows) instead of `./jake.sh` (or `jake`) to use Grunt instead of Jake. Use `./gulp.sh` (or `gulp`) to use Gulp.


License
-------

MIT License. See `LICENSE.TXT`.