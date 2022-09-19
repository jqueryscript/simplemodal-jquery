Modal - A simple modal window
===========================================
A simple jQuery plugin for creating draggable alert & confirm dialog boxes and image/video/AJAX modal windows.

When designing a site, you often want to display different kinds of messages or ask the visitor for specific information. With this plugin you can do just that. 

You can create any kind of alert or confirmation dialog or even present your visitors with an image, a video, or an external page as a modal window without refreshing the page. This makes it easy to add things like newsletter, registration, or purchase forms.

Here is a [nice demo](https://www.jqueryscript.net/demo/alert-confirm-image-video-ajax-modal).

How to Use
----------

Minimal configuration


ALERT INTEGRATION 
-----------------
Snippet code Javascript:

```javascript	
	$("#myElement").click(function() {
	      $.fn.SimpleModal({
                btnOk:    "Alert button",
                title:    "Title",
	            contents: "Your message..."
	      }).showModal();
	});
```

Snippet code HTML:

```html	
	<a id="myElement" href="javascript;">Alert</a>
```

MODAL-AJAX INTEGRATION
----------------------
Snippet code Javascript:

```javascript
	$("#myElement").click(function() {
        $.fn.SimpleModal({
            model: "modal-ajax",
            title: "Title",
            param: {
                url: "file-content.php",
                onRequestComplete: function() { /* Action on request complete */ }
            }
        }.addButton("Action button", "btn primary", function() {
            this.hide();
        }).addButton("Cancel", "btn").showModal();
	});
```
Snippet code HTML:

```html
	<a id="myElement" href="javascript;">Open Modal</a>
```
