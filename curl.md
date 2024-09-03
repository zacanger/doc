# curl

```
-X <HTTP_VERB> ........ use a certain http verb
--data-binary <data> .. keep data as-is, don't attach newlines
--cookie <token> ...... pass in a cookie
-H <header> ........... add a header
-d <data> ............. pass in data
-L .................... follow redirects
```

* Cookies: Retrieve from browser tools network tab
* Headers: `curl -H "Content-Type: application/json" http://localhost:3000`
* Data: `curl -H "Content-Type: application/json" -d \
  '{"username":"xyz","password":"xyz"}' http://localhost:3000/api/login`
* Data-Binary: `curl --data-binary @myFile.json http://localhost:3000/api`
