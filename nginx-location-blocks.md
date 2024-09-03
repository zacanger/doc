* `location = /` - will only match the root path
* `location ^~ /community` - will match every path starting with /community
* `location ~ \.pl` - will match all files that contain .pl
* `location ^~ /news` - will match every path starting with /news
* `location ^~ /app` - will match every path starting with /app
* `location /` - will match all paths not matched above
* `location ~* ^/news/(.*\.php)$` - will match all files ending in .php, with paths starting with /news/
* `location ~* ^/app/(.*\.php)$` - will match all files ending in .php, with paths starting with /app/
