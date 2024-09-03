* URIs
  * consistent naming (plural nouns)
  * self-descriptive
  * natural sub resources
* UX
  * provide filtering, sorting, paging, field selection
  * good documentation
  * self-documentation / discoverability
  * don't make the client do anything the server could do
  * versioning
  * handle errors with appropriate HTTP status codes and a message
  * return updated resources in response
* Server
  * cache intelligently
  * gzip all the things
  * rate limit info in headers
  * logging/monitoring
* Security
  * keep sensitive info out of URLs
  * restrict scope and methods
  * input validation, strong typing, secure parsing
  * CSRF tokens
  * SSL/https
  * OAuth 2.0
  * HMAC (hash-based message authentication code)
