wc-presentation
===============

a presentation about web components using web components

##Getting Started

`npm install`

`sh serve.sh`

[demo page](http://autosponge.github.io/wc-presentation/)

Note: 

- If you clone this repo, remember to delete the `index.html` file under `/slides`.
It's only there because Github doesn't allow directory listing.  If you want to serve it from
__gh-pages__, recreate the `index.html` file by saving the directory listing page.

- If you want to use the _remote control_, get [the other repo](https://github.com/AutoSponge/wc-presentation-remote)
and change the firebase url in both of them to your own firebase.  I used the following
for security rules after setting up a registered user under __Simple Login &gt; Email &amp; password__:

```javascript
{
    "rules": {
      ".read": false,
      "$userid": {
        ".read": true,
        ".write": "auth.id == $userid"
      }
    }
}
```

- Once you log into both the presentation and the remote-control, they will be synced.