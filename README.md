# tipsy
Dirt-simple, accessible tooltips for the web.

Blends very good ideas from:

https://inclusive-components.design/tooltips-toggletips/

and

http://aninnovativeweb.tumblr.com/post/820491172/semantic-tooltips-with-pure-css3-and-html5/amp

Hovering, focusing, clicking, or tapping will bring up the tip.


## Dependencies

jQuery (at the moment)


## Usage - Concise Form

```html
	<p>Lorem ipsum <a data-tip="This is the tip.">dolor</a> sit amet</p>
```


## Expanded Form

tipsy.js will expand above example to:

```html
	<p>lorem ipsum <a href="#tip-0" class="tip"><div aria-describedby="tip-0">dolor</div><div role="tooltip" id="tip-0">This is the tip.</div></a> sit amet</p>
```

For more complicated tooltips (i.e., those that have markup), you can use the expanded form directly.


## Full Example

```html
<!doctype html>
	<html>
		<head>
			<link rel="stylesheet" type="text/css" href="tipsy.css">
			<script type="text/javascript" src="your-jquery/jquery.min.js"></script>
			<script type="text/javascript" src="tipsy.js"></script>	
		</head>
	<body>
		<!-- Concise form -->
		<p>Concise: Lorem ipsum <a data-tip="This is the tip.">dolor</a> sit amet</p>
		
		<!-- Expanded form -->
		<p>Expanded: Ut enim ad <a href="#tip-1" class="tip"><div aria-describedby="tip-1">minim</div><div role="tooltip" id="tip-1">This is the tip.</div></a> veniamolor</p>
	</body>
</html>
```


## Fallback

If you use the concise form without js, the fallback is to use css to display the data-tip attribute on hover.
