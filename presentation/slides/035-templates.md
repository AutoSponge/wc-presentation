##Templates

Augments native template tag

- single
- iterative
- conditional
- recursive

```markup
<template bind="{{ files }}">
<template repeat="{{ file in files }}">
<template if="{{ file.extension }}">
<template repeat="{{ files }}" id="t">
    <li>{{name}}
    <ul>
      <template ref="t" repeat="{{ children }}">
```

<a class="docs" target="_blank" href="http://www.polymer-project.org/docs/polymer/binding-types.html"></a>