# locize-formatjs-example

Example how to use [FormatJS](http://formatjs.io/) and [locize.com](http://www.locize.com) using a node.js server.

Same rules apply to [react-intl](https://github.com/yahoo/react-intl),...

## starting the sample

```
npm i
npm start
```

open [localhost:8080](http://localhost:8080) in your browser

## What we do:

1. We use the [locize API](http://locize.com/api.html) Fetch Route to load the translations
2. We add the translation resources and language to js vars in the returned html
3. From there we use [yahoo/intl-messageformat](https://github.com/yahoo/intl-messageformat) like

```
function t(key, opts) {
  opts = opts || {};
  var m = new IntlMessageFormat(resources[key], lng);
  return m.format(opts);
}
```

Alternatively you could also load the resources via xhr and translate onLoaded
