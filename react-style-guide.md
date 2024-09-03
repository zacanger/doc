# React Styleguide


## Directory Structure

* You should have a single entry point in your source.
* Components each belong in their own subdirectory.
* Each component should have its assets in that subdirectory.
  * Except for assets that never change.
  * And except for global styles.
  * Keep component tests with their components.
* Don't nest component directories.
* Keep your source and built code in separate subdirectories.
* Keep your config, manifest, etc. files all in the top level.

```
/projectroot/package.json
/projectroot/.eslintrc
/projectroot/webpack.config.dev.js
/projectroot/webpack.config.prod.js
/projectroot/dist/index.html
/projectroot/dist/assets-that-never-change/stuff
/projectroot/src/index.js
/projectroot/src/config.js
/projectroot/src/stores/stuff.js
/projectroot/src/actions/something.js
/projectroot/src/components/ComponentOne/One.jsx
/projectroot/src/components/ComponentOne/One.styl
/projectroot/src/components/ComponentOne/one.test.js
/projectroot/src/components/ComponentTwo/two.styl
/projectroot/src/components/ComponentTwo/Two.jsx
/projectroot/src/components/ComponentTwo/two.test.js
/projectroot/src/shared/global.styl
/projectroot/server/index.js
/projectroot/server/routes/endpoint.js
```

(You get the idea, I think.)


## Styling

* Use atomic classnames as much as possible.
* `.xs .warn .red` is better than `.component-small-view .warning-button-red`.


## Code

* Use ESNext. There's no reason not to do this.
* Use Babel.
* Avoid classes where possible.
  * This can be difficult with React, but try to use functions instead of classes.
* For components with more than two attributes, make them multi-line. Put the close on a newline.
* Use imports. Line up `from`. Spaces in `{}`.
* Comma-first.
* Semicolons only when actually necessary.
* Avoid using extensions in your `import`s. That makes things difficult if you ever want to change.

```
import React             from 'react'
import { stuff, things } from 'SomeOtherThing'
inmport One              from './One'

render(){
  return (
    <One
      something={this.props.whatever}
      other={stuff}
      attribute={yep}
    />
  )
}

export default RenderedComponentOneYay
```


## Builds

* Have separate configuration for development and production.
* Automate everything as much as possible.
* Don't just blindly pick a build system.
  * Browserify is almost always fastest and simplest for builds.
  * Webpack almost always offers the most for React development.
  * Gulp is almost always the most flexible and covers the most ground.
  * Grunt almost always is... still a thing that people use sometimes.

