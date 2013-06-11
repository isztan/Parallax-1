Gumby Parallax Module
=====================

This UI module applies a simple background image parallaxing effect. Check out the demo at [gumbyframework.com/demo](http://gumbyframework.com/demo).

Installation
------------

Move gumby.parallax.js into your Gumby project and include the file in the same fashion as your other UI modules, after gumby.js and before gumby.init.js. In production you should minify JavaScript files into a single optimized gumby.min.js file, ensuring the order (gumby.js, UI modules, gumby.init.js) is retained. 

	<!--
	Include gumby.js followed by UI modules.
	Or concatenate and minify into a single file-->
	<script src="js/libs/gumby.js"></script>
	<script src="js/libs/ui/gumby.skiplink.js"></script>
	<script src="js/libs/ui/gumby.toggleswitch.js"></script>
	<script src="js/libs/ui/gumby.parallax.js"></script>
	<script src="js/libs/gumby.init.js"></script>
	
	<!-- In production minifiy and combine the above files into gumby.min.js -->
	<script src="js/libs/gumby.min.js"></script>
	<script src="js/plugins.js"></script>
	<script src="js/main.js"></script>
	
Move _parallax.scss into your Gumby project in sass/ui. Then import the file inside sass/ui/_all.scss in the same fashion as the other imports. Once you compile sass you are good to go.

	@import "video";
	@import "toggles";
	@import "parallax";


Usage
-----

Using the parallax module is simple. Add a class of `parallax` to the element ensuring it has a fixed height and a background image. Use the `gumby-parallax` attribute to specify the ratio at which the background image moves relative to the users scroll. The window scroll event will be used unless another element is specified in `gumby-holder`. The bg image will reach 0px Y position when the element itself reaches the top of the window, you can specify a px value in `gumby-offset` with which to offset this 'end point'.

	<!-- bg position will scroll at half the speed of windows natural scroll -->
	<!-- bg will be positioned at 0 0 when element is 100px from top of window -->
	<div class="parallax" gumby-parallax="0.5" gumby-offset="100"></div>


**MIT Open Source License**

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated
documentation files (the "Software"), to deal in the Software without restriction, including without limitation the
rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit
persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the
Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE
WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

	
	
