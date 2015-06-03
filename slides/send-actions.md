##  Sending Actions

`sendAction`

```html
<!-- index.hbs -->
{{blog-post action="savePost"}}
```

```html
<!-- components/blog-post.hbs -->
<h1>{{title}}</h1>
<div class='body'>{{body}}</div>
<button {{action 'save'}}>Save</button>
```

```javascript
App.BlogPostComponent = Ember.Component.extend({
  actions: {
    save: function() {
      /* Notify templates controller or route */
      this.sendAction();
      /* Send with post parameter */
      this.sendAction( 'action', this.get('post') );
    }
  }
});
```