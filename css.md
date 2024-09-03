# CSS

## Naming

Naming things is hard, and with specificity in the mix it becomes even harder.
By using the naming scheme below, many, if not all naming issues will be
resolved. Short words and dashes between them are key.

```
.navbar              block
.navbar-item         block-element
.navbar-item-active  block-element_modifier
```

## Specificity

```css
.foo .foo-bar .foo-bar_baz {}
.foo-bar_baz {}
[foo="bar"] {}
```

By using the second or third form, specificity issues will never happen.

## Comments

Comments are useful to indicate new sections. Often times groups of selectors
belong together, and comments are a great way to indicate that.

## Variables

* have a main color
* light colors
* dark colors
* inverted colors
* err, warn, success, action
* have a complimentary color
* head, body, mono fonts
* z-indeces, colors, fonts are always a variable
* variables for everything
* all variables in one file

## Flexbox

Flex container (parent):

```txt
display           flex, inline-flex
flex-direction    row, row-reverse, column
flex-wrap         nowrap, wrap, wrap-reverse
flex-flow         <flex-direction> <flex-wrap>
justify-content   flex-start, flex-end, center, space-between, space-around
align-items       flex-start, flex-end, center, stretch, baseline
align-content     flex-start, flex-end, center, stretch, space-between, space-around
```

Flex items (children):

```txt
order             <integer>
flex-grow         <integer:0>
flex-schrink      <ufloat:1.0>
flex-basis        <length> | auto
flex              none | <flex-grow> <flex-shrink> || <flex-basis>
align-self        auto, flex-start, flex-end, center, stretch, baseline
```

## Files

Storing CSS in the right files is just as important as correctly naming
classes. There are a few base files every site wants to start out with:

```text
index.css       imports
vars.css        variable declarations
base.css        body classes & helpers, usually super tiny
typography.css  base text styles
buttons.css     base button styles
forms.css       base form styles
lists.css       base list styles
```

## Attribute selectors

```css
.show-grid [class*="span"] {} /* search children for class="span"*/
div[class^="something"] {}    /* search children for "begins with..." */
div[class$="something"] {}    /* search children for "ends with..." */
```

## Print stylesheets

There are 2 approaches: blacklisting and whitelisting. Whitelisting is unwieldy
to implement using CSS level 4, so blacklisting is the way to go.

### whitelisting

Pick the elements you want to hide (sidebar, footer, etc) and set them to
`display: none`.

## Style input placholders

Supported by autoprefixer.

```css
input::placeholder { }
```

## Shadow

```txt
box-shadow: [horizontal offset] [vertical offset]
            [blur radius] [optional spread radius] [color];
```

