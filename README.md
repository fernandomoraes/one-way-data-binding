simple test:
===========

```html
<body ow-app="app">
  <div ow-controller="PersonCtrl">
		{{name}}, {{age}} - {{city}}
	</div>
	<div ow-controller="CarCtrl">
		{{name}} ({{year}})
	</div>
</body>
```

```javascript
(function(){

		new OneWay('app')
			.registerController('PersonCtrl', function(scope){
				scope.name = 'Fernando Moraes';
				scope.age = 24;
				scope.city = "Siderópolis";
			})
			.registerController('CarCtrl', function(scope){
				scope.name = 'Fusca';
				scope.year = 1970;
			});

	})();
```
