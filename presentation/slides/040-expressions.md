##Expressions and Filters

We can do more than just read data from the model 

```markup
<paper-progress value="{{ selected + 1 }}">
<template if="{{ file.extension | matchExtension('markdown') }}">
```

```javascript
// filter example
matchExtension: function ( value, type ) {
    return this[type + 'List'].some( function ( valid ) {
        return valid === value;
    } );
}
```
<a class="docs" target="_blank" href="http://www.polymer-project.org/docs/polymer/expressions.html"></a>
