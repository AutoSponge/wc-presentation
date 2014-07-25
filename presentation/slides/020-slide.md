##Event Binding

Then we handled the response with this: 

```javascript
handleFilesList: function ( e, data/*, sender*/ ) {
    var elms = data.response.querySelectorAll( 'li' );
    [].slice.call( elms, 0 ).reduce( function ( files, li, i ) {
        var name = li.innerText.trim();
        files.push( {
            name: name,
            index: i,
            extension: name.split( '.' ).pop()
        } );
        return files;
    }, this.files );
}
```
    