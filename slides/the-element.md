##  The Element

`tagName`

```html
<!-- Default div -->
<div id="ember180" class="ember-view">
  <h1>My Component</h1>
</div>
```

Customize
```javascript
App.BlogPostComponent = Ember.Component.extend({
  tagName: 'li'
});
```

New Output
```html
<li id="ember180" class="ember-view">
  <h1>My Component</h1>
</li>
```