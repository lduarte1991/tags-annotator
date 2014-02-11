tags-annotator
==============

Plugin for Annotator that allows a tokenized system of tagging annotations and a way for them to be distinguished based on different colors for different tags

#Installation

To use the tool you need to install the [Annotator plugin](https://github.com/okfn/annotator/) to annotate text.

In addition, add tags-annotator.min.js and tags-annotator.min.css CDN distributed file to your head tag, like this:

```html
	<head>
		<!-- Annotator -->
		<script src="http://ajax.googleapis.com/ajax/libs/jquery/1.7/jquery.min.js"></script>
		<script src="http://assets.annotateit.org/annotator/v1.2.7/annotator-full.min.js"></script>
		<link rel="stylesheet" href="http://assets.annotateit.org/annotator/v1.2.7/annotator.min.css">

		<!-- tags Pluging -->
		<script src="src/tags-annotator.js"></script>
		<link href="src/tags-annotator.css" rel="stylesheet">
	
	</head>
```

Furthermore, you will need to create an instance of Annotator with the plugin, as follow:

```js
	<script>
		var 
    	var optionstags = {
    		tag:{tagnumber1:color1,tagnumber2:color2}
		};
    	$('#div_id').annotator().annotator('addPlugin','HighlightTags',optionstags);
    </script>
```

Change #div_id for the real id where the Annotator is and "optionstags" should include the tags and the colors they correspond to. 