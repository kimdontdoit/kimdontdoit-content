```js
// app/code/Vendor/Flex/view/web/js/example-component.js

define([], function (Component) {
	return Component.extend({ defaults: {
		template: SwiftOtter_Flex/example-component',
		
		sampleText: "Here is some sample text." }
	});
});
```

```html
<!-- app/code/SwiftOtter/Flex/view/web/template/example-component.html -->

<div class="sample-component">
	<p data-bind="text: sampleText"></p>
</div>
```

```js
this.price = ko.observable(12.42)

this.price()

this.price(12.99)

// arrays

this.prices = ko.observableArray([])

// with callback

this.computedVal = ko.computed(callback)
this.pureComputedVal = ko.pureComputed(callback)

```

```html
<div data-bind="text: price"></div>
```

```html
<ul>  
<li>Please choose</li>  
<!-- ko foreach: payments -->  
<li data-bind="text: $data.name"></li>
<!-- /ko -->

</ul>
```

```js
define([ 'uiComponent'

], function(Component) { return Component.extend({

defaults: {
price: 11,
tracks: { price: true
}, imports: {

price: '${$.provider}:price'

// we are linking the price variable on this with the price observable in $.provider.

} }

})});
```