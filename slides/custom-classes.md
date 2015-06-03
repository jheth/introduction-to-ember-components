##  Custom Classes

`classNames classNameBindings`

```html
/* components/blog-post.hbs */
<h1>{{title}}</h1>
<div>{{body}}</div>
<p>{{author}}</p>
```

```javascript
App.BlogPostComponent = Ember.Component.extend({
 tagName: 'div',
 classNames: ['post'],
 classNameBindings: ['hidden', 'hidden:off:on', 'post.isPublished:published'],
 hidden: true
});
```

```html
<!-- Rendered DOM -->
<div id="ember180" class="ember-view post hidden off">
  <h1>{{title}}</h1>
  <div>{{body}}</div>
  <p>{{author}}</p>
</div>

<div id="ember180" class="ember-view post hidden off published">
...
</div>
```
