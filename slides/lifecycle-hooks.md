##  Lifecycle Hooks

* willInsertElement <br><small>Called when a view is going to insert an element into the DOM.</small>
* didInsertElement <small>Called when the element of the view has been inserted into the DOM or after the view was re-rendered. Override this function to do any set up that requires an element in the document body.</small>
* willDestroyElement <small>Called when the element of the view is going to be destroyed. Override this function to do any teardown that requires an element, like removing event listeners.</small>
* willClearRender <small>Called when the view is about to rerender, but before anything has been torn down. This is a good opportunity to tear down any manual observers you have installed based on the DOM state</small>
* parentViewDidChange <br><small>Called when the parentView property has changed.</small>