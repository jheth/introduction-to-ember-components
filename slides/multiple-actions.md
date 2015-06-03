##  Multiple Actions

```html
<!-- index.hbs -->
{{blog-post save="savePost" delete="deletePost"}}
```

```html
<!-- components/blog-post.hbs -->
<h1>{{title}}</h1>
<div class='body'>{{body}}</div>
<button {{action 'save'}}>Save</button>
<button {{action 'delete'}}>Delete</button>
```

```javascript
App.BlogPostComponent = Ember.Component.extend({
  actions: {
    save: function() {
      this.sendAction( 'save', this.get('post') );
    },
    delete: function() {
      this.sendAction( 'delete', this.get('post') );
    }
  }
});

App.IndexRoute = Ember.Route.extend({
  actions: {
    savePost: function(post) {
      post.save();
    },
    deletePost: function(post) {
      post.destroyRecord();
    }
  }
});
```