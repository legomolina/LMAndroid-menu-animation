# LMAndroid-menu-animation
Android L menu animation for open and close with CSS3

##### Introduction
This is a little CSS3 code to run the Android L menu animation on web.

##### Instalation
<b>This library needs <a href="https://jquery.com/" target="_blank">Jquery</a> to use it.</b><br />

```javascript
<script src="https://code.jquery.com/jquery-2.2.3.min.js" integrity="sha256-a23g1Nt4dtEYOj7bR+vTu7+T8VP13humZFBJNIYoEJo="   crossorigin="anonymous"></script>
```

In the example I provide all CSS is in the same page but, obviusly, you can change that creating a .css file and linking into the document. After that, you only need to create this HTML structure:

```html
<div id="outer-container">
		<div id="text">
			<!-- Put your content here... -->
		</div>
	<div id="inner-circle"></div>
</div>

<div id="outer-circle"></div>
```

And add this script into document.onload or $(document).ready:
```javascript
var circle = $("#inner-circle"); /* Fake button to make the content rounded and start from here */
$("#outer-circle").click(function() {
	if(circle.hasClass('expanded')) { /* If the content is expanded */
		$("#text").removeClass('expanded-text').one('webkitTransitionEnd otransitionend oTransitionEnd msTransitionEnd transitionend', function() {
			circle.removeClass('expanded');
		});
	}
	else {
		circle.addClass('expanded').one('webkitTransitionEnd otransitionend oTransitionEnd msTransitionEnd transitionend', function() {
			$("#text").addClass('expanded-text');
		});
	}
});
```

And you are done to use it!<br />
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/" target="_blank"><img alt="Licencia de Creative Commons" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">LMAndroid-menu-animation</span> by <span xmlns:cc="http://creativecommons.org/ns#" property="cc:attributionName">legomolina</span> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/" target="_blank">Creative Commons Reconocimiento-CompartirIgual 4.0 Internacional License</a>.
# LMSpoiler
