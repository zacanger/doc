# Lodash

This list is incomplete. Just some of the major functions.

## Collections

Works for both arrays and objects.

```javascript
_.filter(list, (n) => n % 2)    //=> Array
_.find(list, (n) => n % 2)      //=> item
_.findRight(list, ...)          //=> item
```

### Accessing

```javascript
_.at([ abcd ], 0)               //=> [ a ] - same as list[0]
_.at([ abcd ], [ 0, 1 ])        //=> [ ab ]
```

### Set/get

```javascript
_.set(object, 'users[0].name', value)
_.get(object, 'users[0].name')
_.get(object, ['users', 0, 'name'])
```

### Iteration

```javascript
_.forEach(list, (item, i) => ...)
_.forEachRight(list, ...)

_.map(list, ...)
```

```javascript
_.every(users, (u) => u.active)  //=> true|false (aka _.all)
_.any(users, ...)                //=> true|false (aka _.some)
```

## Array

```javascript
_.chunk([ abcd ], 2)           //=> [ [ab], [cd] ]
_.compact(list)

_.fill(Array(4), 'x')          //=> [ 'x', 'x', 'x', 'x' ]
_.flatten
_.flattenDeep
```

### Filtering

```javascript
_.drop([ abcdef ], 2)          //=> [   cdef ]
_.dropRight([ abcdef ], 2)     //=> [ abcd   ]
_.take([ abcdef ], 2)          //=> [ ab     ]
_.takeRight([ abcdef ], 2)     //=> [     de ]

_.initial([ abcdef ])          //=> [ abcde  ] - dropRight(list, 1)
_.rest([ abcdef ])             //=> [  bcdef ] - takeRight(list, 1)

_.slice([ abcdef ], 2, 4)      //=> [   cd   ]

_.dropWhile(list, 'active')            // works like filter
_.dropWhile(list, 'active', true)
_.dropWhile(list, { active: true })
_.dropWhile(list, (n) => ...)
_.dropRightWhile(list, ...)

_.without([ abcde ], b)        //=> [ acde ]

_.remove(list, (n) => n % 2)
```

### Accessing

```javascript
_.first([ abcdef ])            //=> a
_.last([ abcdef ])             //=> f
```

### Sets

```javascript
_.uniq()
_.difference([ abc ], [ bc ])       //=> [ a    ]
_.intersection([ abc ], [ bcd ])    //=> [  bc  ]
_.union([ abc ], [ bcd ])           //=> [ abcd ] (unique)

Array#concat()
```

### Indexes

```javascript
_.findIndex
_.findLastIndex

_.sortedIndex(list, val)
_.sortedLastIndex(list, val)

_.indexOf(list, val)
```

## Functions

### Currying

```javascript
greet = (greeting, name) => `${greeting}, ${name}!`
```

```javascript
fn = _.partial(fn, 'hi')
fn('joe')    //=> 'hi, joe!'

_.partial(fn, 'joe')
fn('yo')     //=> 'yo, joe!'
```

```javascript
_.curry(greet)('hi')         //=> function(name)
_.curryRight(greet)('joe')   //=> function(greet)
```

## Functions - decorating

### Throttling

```javascript
_.throttle(fn)
_.debounce(fn)
```

### Limiting

```javascript
_.before(5, fn)         // only works 5 times
_.after(5, fn)          // works only after 5 times
_.once(fn)              // like _.before(fn, 1)
```

### Etc

```javascript
_.wrap(_.escape, (name) => `hi ${name}`)
// same as doing `name = _.escape(name)`

_.delay(fn, 2000)

_.negate(fn)

_.memoize(fn)
_.memoize(fn, ...)
```

## Strings

### Capitalization

```javascript
_.capitalize('hello world')   //=> 'Hello world'
_.startCase('hello_world')    //=> 'Hello World'
_.snakeCase('hello world')    //=> 'hello_world'
_.kebabCase('hello world')    //=> 'hello-world'
_.camelCase('hello world')    //=> 'helloWorld'
```

### Padding

```javascript
_.pad('abc', 8)           //=> '   abc  '
_.padLeft('abc', 8)       //=> '     abc'
_.padLeft('abc', 8, '-')  //=> '00000abc'
_.padRight(...)
```

### Trim

```javascript
_.trim('  str  ')
_.trimLeft('  str  ')
_.trimRight('  str  ')
```

### Etc

```javascript
_.repeat('-', 2)              //=> '--'
_.deburr('déjà vu')           //=> 'deja vu'
_.trunc('hello world', 5)     //=> 'hello...'
```

```javascript
_.startsWith('abc', 'a')   //=> true
_.endsWith('abc', 'c')     //=> true
```

## Objects

```javascript
_.keys(obj)
_.values(obj)
```

## Chaining

```javascript
_([1, 2, 3])
  .reduce((total, n) => total + n)
  .map((n) => n * n)
  .tap(console.log)
  .thru((n) => n.reverse())
  .value()
```
