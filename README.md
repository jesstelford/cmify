cmify (aka node-css-modules)
====

A node-first approach to [CSS Modules](https://github.com/css-modules/css-modules), so you can use CSS Modules on the server without any extra tools.

Example
----

```js
var cmify = require('cmify')
var styles = cmify.load('./styles.css')

console.log('Generated classnames:', styles)
console.log('Generated CSS:', cmify.getAllCss())
```

For a complete example take a look at [cmify-example](https://github.com/joshwnj/cmify-example)

Building for the browser
----

With browserify:

```
npm install -D browserify

browserify -p cmify/plugin src/index.js
```

With hot module reloading:

```
npm install -D watchify browserify-hmr

watchify -p browserify-hmr -p cmify/plugin src/index.js -o dist/index.js
```

Thanks
----

to the [CSS Modules team](https://github.com/orgs/css-modules/people)

License
----

MIT
