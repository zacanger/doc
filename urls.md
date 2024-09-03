[URLs](http://www.ietf.org/rfc/rfc2396.txt) are made up of (usually just some) of these parts: `<scheme>://<username>:<password>@<host>:<port>/<path>;<parameters>?<query>#<fragment>`.
* The scheme is the _protocol_ (http, https, ftp, git, etc.). It ends with `:` (not `//`).
* The username and password are fairly self-explanitory, and we don't see that a whole whole lot these days, except
  maybe in FTP.
* The host is the part we all know well, like 'github' or 'google.' It can be a domain name or an IP address.
* The port (80 for HTTP, 443 for HTTPS, etc.) is self-explanitory; defaults to 80.
* The path would be segments (like `/doc/search` or whatever), and can contain semicolons to separate parameters (like `thing=foo;stuff=bar`).
* Queries can be before or after parameters, and that'd be something like `/?q=foo+bar`.
* Fragments are for specific parts of a resource, like `somepage.html#somesection`.
* `; / ? : @ & = + $ ,` are reserved characters (meaning they have special uses in URLs).
* `- _ . ! ~ * ' ( )` are unreserved (you can use them almost wherever you'd like).
* `{ } | \\ ^ [ ] \` ` are unwise to use in URLs (note that this includes the backslash and backtick/grave, which may not render in Markdown code blocks, depending on parser).
* `< > # % "` don't use these, at all (except the `%` and `#` _if_ you have a valid reason for it, because they do special things in URLs).

