# Lab 1 : Setup and Install Dependencies

>(accepting community contributions)

OpenUI5 development is suited for any JavaScript editor. Here are some options if you don't have a favorite:
* [Visual Studio](https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx)
	* Visual Studio Community is free for individual developers, open source projects, academic research, education, and small professional teams. [Learn more](https://www.visualstudio.com/support/legal/mt171547)
* [Sublime Text](http://www.sublimetext.com/3)
	* Sublime Text may be downloaded and evaluated for free, however a license must be purchased for continued use.
* [Visual Studio Code](https://code.visualstudio.com/)
	* Free

Ensure you have a web server available to serve our HTML and JavaScript files:
* Web server built into editor
* `npm install http-server`
* `python -m SimpleHTTPServer 8000`

Create our index page to test our web server:

```html
<!doctype html>
<html>
	<head>
		<title>OpenUI5 Workshop</title>
		<script id="sap-ui-bootstrap"
				src="https://openui5.hana.ondemand.com/resources/sap-ui-core.js"
				data-sap-ui-libs="sap.m"
				data-sap-ui-theme="sap_bluecrystal"
				data-sap-ui-resourceRoots='{"workshop": "./"}'>
		</script>
		<script>
			sap.ui.getCore().attachInit(function() {
				sap.ui.require([
					"sap/m/Shell",
					"sap/ui/core/ComponentContainer"
				], function (Shell, ComponentContainer) {
					// TODO: we'll add a Shell here later
				});
			});
		</script>
	</head>
	<body class="sapUiBody" role="application">
		<div id="content"></div>
	</body>
</html>
```

Run your web server, you should see a blue page. This is perfect (we are just testing the web server and your editor)!