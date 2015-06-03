##  mut Helper

```html
<my-counter count={{mut activatedCount}} />
```

```javascript
// my-counter.js
export default Component.extend({
  click: function() {
    this.attrs.count.update(this.attrs.count.value + 1);
  }
});
```

The mut helper will produce an object that contains both a value property and an update method.