##  Custom Attributes

`attributeBindings`

Bind attributes to the DOM element.

```javascript
App.LinkItemComponent = Ember.Component.extend({
  tagName: 'a',
  attributeBindings: ['href'],
  href: "http://emberjs.com"
});
```

Bind attributes to differently named properties:

```javascript
App.LinkItemComponent = Ember.Component.extend({
  tagName: 'a',
  attributeBindings: ['customHref:href'],
  customHref: "http://emberjs.com"
});
```