# React Errors

You will get one of these:
```
Uncaught (in promise) TypeError: Cannot read property 'toUpperCase' of undefined(…)
ReactCompositeComponent.js:870 Uncaught TypeError: Cannot read property 'displayName' of undefined
```
if you try to do `import { ComponentName } from 'ComponentName.jsx'`
instead of `import ComponentName from 'ComponentName.jsx'`.

This error: `Uncaught TypeError: Cannot read property 'toUpperCase' of undefined`
might be caused by importing: `import { Link } from 'redux-router'`
instead of `import { Link } from 'react-router'`

Performance problems might be caused by 'redux-logger' and 'redux-devtools' packages.
Remove them from production build!

This error: `Uncaught TypeError: Cannot read property 'displayName' of undefined at Array.forEach (native)`
When you try to render an array of items with map callback: `{items.map(renderItem)}`
You have to wrap the rendered result into `<div></div>` tag.

```
index_bundle.js:9077 Warning: Failed propType: Invalid prop `component` supplied to `IndexRoute`.
```
Standardize import
module.exports = Component should become export default Component.
