##Other Models

Templates have their own models.

Template instances also have models.

```javascript
showModel: function ( e, detail, sender ) {
    var dialog = this.$.dialog;
    var model = sender.templateInstance.model.file;
    dialog.setAttribute( 'heading', model.name );
    dialog.innerHTML = [
        '<pre>',
        '<code class="language-javascript">',
        JSON.stringify( model, null, '  ' ),
        '</code>',
        '</pre>'
    ].join( '' );
    Prism.highlightElement( dialog.querySelector( 'code' ) );
    dialog.toggle();
}
```

<a class="docs" target="_blank" href="http://www.polymer-project.org/docs/polymer/databinding.html#event-handling-and-data-binding"></a>