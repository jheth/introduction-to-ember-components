##  Wrapping Content

Introducing: {{yield}}

```html
< script type="text/x-handlebars" id="components/blog-post">
  <h1>{{title}}</h1>
  <div class="body">{{yield}}</div>
</ script>
```

```html
{{#blog-post title=title}}
  <p class="author">by {{author}}</p>
  {{body}}
{{/blog-post}}
```


Template scope inside the component block is the same as outside.