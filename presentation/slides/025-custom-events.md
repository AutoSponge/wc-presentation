##Custom Events

We can also fire our own events:

```javascript
ready: function () {
  Mousetrap.bind( this.keys, this.keyHandler.bind( this ) );
}
keyHandler: function ( e, data ) {
  this.asyncFire( 'key-' + data, {event: e, key: data} );
}
```

```markup
<polymer-element
  name="wc-presentation"
  on-key-right="{{ next }}"
  on-key-left="{{ prev }}"
  attributes="url markdown raw">
```

<a class="docs" target="_blank" href="http://www.polymer-project.org/docs/polymer/polymer.html#fire"></a>