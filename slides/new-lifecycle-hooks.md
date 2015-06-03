##  New Lifecycle Hooks

`didUpdateElement`

```javascript
/* Ember 1.12 */
Component.extend({
  didInsertElement() {
    this.$().button({
      text: this.get('value'),
      disabled: this.get('disabled')
    });
  },
  valueDidChange: observer('value', function() {
    this.$().option('text', this.get('value'))
  })
});
/* Ember 1.13 */
Component.extend({
  didInsertElement() {
    this.$().button({
      text: this.attrs.value,
      disabled: this.attrs.disabled
    });
  },
  didUpdateElement() {
    this.$().options({
      text: this.attrs.value,
      disabled: this.attrs.disabled
    });
  }
});
```