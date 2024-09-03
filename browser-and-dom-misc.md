# The DOM

While most developers have some understanding of how HTML and the DOM work,
there are a good amount of tags available that are most likely being misused. I
don't care about non-evergreen browsers, so that's the only guarantee about
compatibility I'm able to make.

## Tags

    <nav>       the main navigation controls
    <header>    the introductory block at the start of the page
    <main>      the main content, should cover most of the page
    <section>   the different parts of main
    <footer>    page end, credits and stuff
    <aside>     the sidebar, if any exists

## Events

A big gotcha of DOM events is that they propagate to their parent nodes if left
unhandled. By setting `this.stopPropagation()` the events are no longer
propagated to their parents.

Another gotcha with the DOM is that when you're building dynamic systems
with JavaScript, existing DOM nodes will have default behavior that is
executed. For example: when submitting a form, the default behavior is to
refresh the page after submission. To prevent this from happening you have to
use the `this.preventDefault()` method within the form element.

## Reflows & Repaints

> A repaint occurs when changes are made to an elements skin that changes
> visibility, but do not affect its layout. Examples of this include outline,
> visibility, or background color. According to Opera, repaint is expensive
> because the browser must verify the visibility of all other nodes in the DOM
> tree.

> A reflow is even more critical to performance because it involves changes
> that affect the layout of a portion of the page (or the whole page).

[source](http://stackoverflow.com/questions/2549296/whats-the-difference-between-reflow-and-repaint)

## Buttons

Creating a button can be done in multiple ways (all dependending on style).
Function comes down to semantics. Best practices for this are:

* __a__: use anchor tags for external links
* __button__: use buttons for all non-form related actions
* __input__: use input tags for all form related actions

## Push notifications on the web

Create a manifest in `index.html`:
```html
<link rel="manifest" href="/manifest.json">
```

* [installable Web Apps with the WebApp Manifest in Chrome for Android](http://updates.html5rocks.com/2014/11/Support-for-installable-web-apps-with-webapp-manifest-in-chrome-38-for-Android)
* [push notifications on the Open Web](http://updates.html5rocks.com/2015/03/push-notificatons-on-the-open-web)
* [introduction to service workers](http://www.html5rocks.com/en/tutorials/service-worker/introduction/)
* [notifications api](https://notifications.spec.whatwg.org/)
* [push api](http://w3c.github.io/push-api/)

## Open links in new tab

```javascript
window.open(url, '_blank')
```

```html
<a href="" target="_blank"></a>
```

## window.fetch

Uses promises, first `.then` call defines in what form the data will be
displayed. The value can be one of `arrayBuffer()`, `blob()`, `formData()`,
`json()` and `text()`.

```javascript
fetch('http://zacanger.com')
  .then((res) => res.text())
  .then((a) => console.log(a))
```

Setting cookie headers is not possible with `fetch`. Instead cookies can be set
through the `credentials` api. The value can be one of `omit`, `same-origin`,
`include` where `omit` is the default.

```javascript
fetch('/something', { credentials: 'same-origin' })
```

## Append class in JS

```javascript
const node = document.querySelector('.foo')
node.classList.remove('ugly')
node.classList.add('pretty')
node.classList.toggle('hide')
```

## Create popup banner
__iOS__
```html
<meta name="apple-itunes-app" content="app-id=myAppStoreID, affiliate-data=myAffiliateData, app-argument=myURL">
```

__android__
```json
"prefer_related_applications": true,
"related_applications": [
  {
  "platform": "play",
  "id": "com.google.samples.apps.iosched"
  }
]
```

- [developers.google.com/app-install-banners](https://developers.google.com/web/updates/2015/03/increasing-engagement-with-app-install-banners-in-chrome-for-android#native)
- [developer.apple.com/smart-banners](https://developer.apple.com/library/mac/documentation/AppleApplications/Reference/SafariWebContent/PromotingAppswithAppBanners/PromotingAppswithAppBanners.html)
