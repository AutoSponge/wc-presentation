##Other Models

Templates have their own models.

Template instances also have models.

```javascript
showModel: function ( e, detail, sender ) {
    var dialog = this.$.dialog;
    var model = sender.templateInstance.model.file;
    var code = dialog.querySelector( 'code' );
    code.innerHTML = JSON.stringify( model, null, '  ' );
    Prism.highlightElement( code );
    dialog.setAttribute( 'heading', model.name );
    this.dialog = 'model';
    dialog.toggle();
}
```

<a class="docs" target="_blank" href="http://www.polymer-project.org/docs/polymer/databinding.html#event-handling-and-data-binding"></a>