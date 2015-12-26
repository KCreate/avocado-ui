### avocado-ui
Minimalist html templating engine. By minimalist i really mean minimalist.

### Usage
```javascript
var Avocado = require('avocado-ui');

var template = `
<div>
	<h1>{{title}}</h1>
	<p>
		{{message}}
	</p>
	<img src="{{url}}">
</div>
`;

var Avo = new Avocado();
Avo.setTemplate(template);
Avo.render({
	title: "Happy new year",
	message: "2016",
	url: "http://bit.ly/1ZuCicW"
}, function(result) {
	console.log(result);
});
```

The result variable in the callback will now contain the following:
```html
<div>
	<h1>Happy new year</h1>
	<p>
		2016
	</p>
	<img src="http://bit.ly/1ZuCicW">
</div>
```
