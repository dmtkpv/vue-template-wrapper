# vue-template-wrapper
Wraps source in `<template />`
```javascript
module.exports = function (source) {
    return `<template>${source}</template>`
}
```
## Using with webpack

_webpack.config.js_
```js
rules: [
    {
        test: /\.svg$/,
        use: ['vue-loader', 'vue-template-wrapper']
    }
]
```
You can now import SVG as a Vue component.
```js
import icon from './icon.svg'
export default {    
    components: { icon }
}
```
