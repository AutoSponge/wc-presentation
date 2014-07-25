##Custom Events

We can also trigger our own events:

```javascript
keyHandler: function ( e, data ) {
    this.asyncFire( 'key-' + data, {event: e, key: data} );
}
```