##  Example

```html
<!-- blog-post.hbs {{blog-post post=object}} -->
<h1>{{post.title}}</h1>
{{#if isEditing}}
  {{textarea value=post.body}}
  <button {{action 'save'}}>Save</button>
{{else}}
  {{post.body}}
  <button {{action 'edit'}}>Edit</button>
{{/if}}
```

```javascript
App.BlogPostComponent = Ember.Component.extend({
  tagName: 'div',
  classNames: ['post'],
  classNameBindings: ['post.isPublished:published'],
  isEditing: false,
  actions: {
    edit: function() {
      this.set('isEditing', true);
    },
    save: function() {
      this.set('isEditing', false);
      this.sendAction();
    }
  }
});
```