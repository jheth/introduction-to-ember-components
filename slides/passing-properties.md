##  Passing Properties

```html
{{! index.handlebars }}
<h1>Template: {{title}}</h1>
/* no properties */
{{blog-post}}

/* insideScope=outsideScope (Two-Way Data Binding) */
{{blog-post title=title}}
```

By default a component does not have access to properties in the template scope in which it is used.