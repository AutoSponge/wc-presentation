##Data Binding

We're updating the model in many ways:
 
```markup
<paper-input value="{{ selected }}">
<core-icon icon="av:skip-next" on-click="{{ next }}">
<polymer-element on-key-right="{{ next }}">
```

```javascript
next: function ( /*e, data, sender*/ ) {
    this.selected = +this.selected;
    if ( this.selected < this.files.length - 1 ) {
        this.selected += 1;
    }
}
```