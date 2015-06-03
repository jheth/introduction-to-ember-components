##  Actions

```html
{{#if isExpanded}}
  <div class='body'>{{body}}</div>
  <button {{action 'hide'}}>Hide</button>
{{else}}
  <button {{action 'show'}}>Show More...</button>
{{/if}}
```

```javascript
App.BlogPostComponent = Ember.Component.extend({
  isExpanded: false,

  actions: {
    show: function() {
      this.set('isExpanded', true);
    },

    hide: function() {
      this.set('isExpanded', false);
    }
  }
});
```