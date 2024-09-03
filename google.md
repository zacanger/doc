# Google

Learning how to search effectively is super important.
This is a collection of ASOs (Advanced Search Operators) and other tips.
There are more operators than what are listed here, but I find these to
be the most useful.

## Operators

* Exclusion: `-`
  * `foo -bar`
  * `theme -intitle:wordpress`
* Synonyms: `~`
  * `react ~tutorial` (include words like `guide` and `reference`)
* Wildcard: `*`
  * `bash * and replace` (include words like `find` and `search`)
* Or: `OR` or `|`
  * `bash OR ksh`
  * `bash | ksh`
* And: `AND`
  * Forces all conditions to be true
  * `bash AND ksh`
* Definition: `define:`
  * `define: foobar`
* Range: `..`
  * `laptop $200..$400`
* Math: you can use the search box/omnibar (if using Chromium) to do math,
  unit and currency conversions, etc.
* Exact match: `""`
  * `"google advanced search operators"`
* Filetype: `filetype:`, `ext:`
  * `haskell filetype:pdf`
  * `inurl:edu ext:pdf -intitle:theory haskell`
* Common words: `+`
  * Google removes common words (like `and`) from searches.
    `+and` would force inclusion of that word.
  * `biscuits +and tea`
* Search in site: `site:`
  * `vim site:blog.zacanger.com`
* Find links to a site: `link:`
  * `link:zacanger.com`
* Search for text in titles of pages:
  * `intitle:`
  * `allintitle:`
  * `inblogtitle:`
  * `inposttitle:`
  * `intitle:index.of inurl:pictures`
* Search only in text of pages:
  * `intext:`
  * `allintext:`
  * `(intext:"index of /.git") ("parent directory")`
* Search in anchors:
  * `inanchor:`
  * `allinanchor:`
* Search in url only:
  * `inurl:`
  * `allinurl:`
  * `inurl:wp-content intitle:index.of`
* Find related sites: `related:`
  * `related:`
* Find in social media: `@`
  * `@twitter vim`
* Show cached version: `cache:`
  * `cache:zacanger.com`
* Show info about a site: `info:`
  * `info:zacanger.com`
* Around: `AROUND()`
  * Proximity to other terms
  * `unicode AROUND(3) xterm`
