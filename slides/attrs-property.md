##  attrs Property

```html
<my-component title={{model.name}} />
```

The component will see `this.attrs.title` as the current value of `model.name`.

Whenever `model.name` changes via observation, or when the parent component is re-rendered,
my-component's lifecycle hooks will be triggered, and it will see a new version of `model.name`.