##Two-way Data Binding

We're updating/displaying the model in many ways:
 
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

<a class="docs" target="_blank" href="http://www.polymer-project.org/docs/polymer/databinding.html"></a>