##  action Helper

```html
{{!-- parent-component.hbs --}}
{{#each users as |user|}}
  <big-button on-active={{action 'selectedUser' user}} />

  {{!-- equivalent --}}
  <big-button on-active={{action actions.selectedUser user}} />
{{/each}}
```

```javascript
// parent-component.js
export default Component.extend({
  actions: {
    selectedUser(user) {
      // this is the component
      // user is the user from the current iteration of the loop
    }
  }
});
```
```javascript
// big-button.js
export default Component.extend({
  click: function() {
    this.attrs['on-active']();
  }
});
```