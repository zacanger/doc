React Cheatsheet

* [official react jsfiddle](http://jsfiddle.net/reactjs/69z2wepo/)
* [unofficial react jsbin](http://jsbin.com/yafixat/edit?js,output)

```js
var Component = React.createClass({
  render: function () {
    return <div>Hello {this.props.name}</div>
  }
})
```

```js
ReactDOM.render(<Component name="John" />, document.body)
```

nesting
```js
var UserAvatar  = React.createClass({...})
var UserProfile = React.createClass({...})
```

```js
var Info = React.createClass({
  render() {
    return <div>
      <UserAvatar src={this.props.avatar} />
      <UserProfile username={this.props.username} />
    </div>
  }
})
```

* states (`this.state`) for dynamic data
* props (`this.props`) for parameters passed from parent

```html
<MyComponent fullscreen={true} />
```

```js
// props
  this.props.fullscreen //=> true

// state
  this.setState({ username: 'zacanger' })
  this.replaceState({ ... })
  this.state.username //=> 'zacanger'
```

```js
render: function () {
  return <div className={this.props.fullscreen ? 'full' : ''}>
    Welcome, {this.state.username}
  </div>
}
```

* defaults pre-populate `this.state.comments` and `this.props.name`

```js
React.createClass({
  getInitialState: function () {
    return { comments: [] }
  },

  getDefaultProps: function () {
    return { name: "Hello" }
  }
)
```

* the below are methods for instances of a `Component`

```js
ReactDOM.findDOMNode(c)  // 0.14+
React.findDOMNode(c)     // 0.13
c.getDOMNode()           // 0.12 below
```

```js
c.forceUpdate()
c.isMounted()

c.state
c.props

c.setState({ ... })
c.replaceState({ ... })

c.setProps({ ... })       // for deprecation
c.replaceProps({ ... })   // for deprecation

c.refs
```

* for lifecycle docs, please see additional notes and demo(s)

example: loading (ajax) data
```js
React.createClass({
  componentWillMount: function () {
    $.get(this.props.url, function (data) {
      this.setState(data)
    }.bind(this))
  },

  render: function () {
    return <CommentList data={this.state.data} />
  }
})
```

* references allow access to DOM nodes

```html
<input ref="myInput">
```

```js
this.refs.myInput
ReactDOM.findDOMNode(this.refs.myInput).focus()
ReactDOM.findDOMNode(this.refs.myInput).value
```
dom events
```html
<input type="text"
    value={this.state.value}
    onChange={this.handleChange} />
```

```js
handleChange: function(event) {
  this.setState({ value: event.target.value })
}
```

two-way binding (used the linkedstatemixin to make this easy)
```html
Email: <input type="text" valueLink={this.linkState('email')} />
```

```js
React.createClass({
  mixins: [React.addons.LinkedStateMixin]
})
```

```js
this.state.email
```

property validation
```js
React.createClass({
  propTypes: {
    email:      React.PropTypes.string
  , seats:      React.PropTypes.number
  , settings:   React.PropTypes.object
  , callback:   React.PropTypes.func
  , isClosed:   React.PropTypes.bool
  , any:        React.PropTypes.any
  }
})
```

required types
```js
propTypes: {
  requiredFunc:  React.PropTypes.func.isRequired,
  requiredAny:   React.PropTypes.any.isRequired,
```

Use `.element`, `.node`.
react elements (`.element` and `.node`)
```js
propTypes: { // react element; int, str, elem,
element:  React.PropTypes.element // or array
, node:     React.PropTypes.node // of the above
}
```

enumerables (`.oneOf` and `.oneOfType`)
```
propTypes: {
  enum:     React.PropTypes.oneOf(['M','F']),  // enum
  union:    React.PropTypes.oneOfType([        // any
              React.PropTypes.string,
              React.PropTypes.number ]),
```

arrays & objects (`.array[Of]`, `.object[Of]`, `.instanceOf`, `.shape`)
```js
propTypes: {
  array:    React.PropTypes.array
, arrayOf:  React.PropTypes.arrayOf(React.PropTypes.number)
, object:   React.PropTypes.object
, objectOf: React.PropTypes.objectOf(React.PropTypes.number)

, message:  React.PropTypes.instanceOf(Message)

, object2:  React.PropTypes.shape({
    color:  React.PropTypes.string
  , size:   React.PropTypes.number
  })
```

custom val
```js
propTypes: {
  customProp: function(props, propName, componentName) {
    if (!/matchme/.test(props[propName])) {
      return new Error('Validation failed!')
    }
  }
}
```

DOM manipulation thru classnames
```js
var cx = require('classnames')

render: function() {
  var classes = cx({
    'message': true
  , 'message-important': this.props.isImportant
  , 'message-read': this.props.isRead
  })
  return <div className={classes}>Great Scott!</div>
}
```

propagating properties (transferring props)
```html
<VideoPlayer src="video.mp4" />
```

```js
var VideoPlayer = React.createClass({
  render: function() {
    /* propagates src="..." down to this sub component */
    return <VideoEmbed {...this.props} controls='false' />
  }
})
```

mixins
```js
var SetIntervalMixin = {
  componentWillMount: function() { .. }
}
```

```js
var TickTock = React.createClass({
  mixins: [SetIntervalMixin]
}
```

top-level API
```js
React.createClass({ ... })

React.isValidElement(c)

ReactDOM.findDOMNode(c) // 0.14+
ReactDOM.render(<Component />, domnode, [callback]) // 0.14+
ReactDOM.unmountComponentAtNode(domnode) // 0.14+

ReactDOMServer.renderToString(<Component />) // 0.14+
ReactDOMServer.renderToStaticMarkup(<Component />) // 0.14+
```

'inline' styles
```js
var style = { backgroundImage: 'url(x.jpg)', height: 10 }
return <div style={style}></div>
```

innerhtml
```js
function markdownify() { return "<p>...</p>" }
<div dangerouslySetInnerHTML={{__html: markdownify()}} />
```

lists
```js
var TodoList = React.createClass({
  render: function() {
    function item(itemText) {
      return <li>{itemText}</li>
    }
    return <ul>{this.props.items.map(item)}</ul>
  }
})
```

