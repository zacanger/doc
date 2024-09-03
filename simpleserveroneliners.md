One-Liners for Simple Static Servers

* python 2: `python -m SimpleHTTPServer 8000`
* python 3: `python -m http.server 8000`
* twisted: `twistd -n web -p 8000 --path .`
* twisted: `python -c 'from twisted.web.server import Site; from twisted.web.static import File; from twisted.internet import reactor; reactor.listenTCP(8000, Site(File("."))); reactor.run()'`
* ruby: `ruby -rwebrick -e'WEBrick::HTTPServer.new(:Port => 8000, :DocumentRoot => Dir.pwd).start'`
* ruby 1.9.2+: `ruby -run -ehttpd . -p8000`
* adsf (ruby): `gem install adsf`, then `adsf -p 8000`
* sinatra (ruby): `gem install sinatra`, then `ruby -rsinatra -e'set :public_folder, "."; set :port, 8000'`
* perl: `cpan HTTP::Server::Brick`, then `perl -MHTTP::Server::Brick -e '$s=HTTP::Server::Brick->new(port=>8000); $s->mount("/"=>{path=>"."}); $s->start'`
* plack (perl): `cpan Plack`, `plackup -MPlack::App::Directory -e 'Plack::App::Directory->new(root=>".");' -p 8000`
* mojolicious (perl): `cpan Mojolicious::Lite`, `perl -MMojolicious::Lite -MCwd -e 'app->static->paths->[0]=getcwd; app->start' daemon -l http://*:8000`
* http-server (node): `npm i -g http-server`, `http-server -p 8000`
* live-server (node): `npm i -g live-server`, `live-server`
* luvi (node): `npm i -g luvi`, `luvi`
* glance (node): `npm i -g glance`, `glance`
* st (node): `npm i -g st`, `st`
* node-static (node): `npm i -g node-static`, `static`
* php: `php -S 127.0.0.1:8000`
* erlang: `erl -s inets -eval 'inets:start(httpd,[{server_name,"NAME"},{document_root, "."},{server_root, "."},{port, 8000},{mime_types,[{"html","text/html"},{"htm","text/html"},{"js","text/javascript"},{"css","text/css"},{"gif","image/gif"},{"jpg","image/jpeg"},{"jpeg","image/jpeg"},{"png","image/png"}]}]).'`
* busybox: `busybox httpd -f -p 8000`
* webfs: `webfsd -F -p 8000`
* iis express (eww...): `C:\> "C:\Program Files (x86)\IIS Express\iisexpress.exe" /path:C:\MyWeb /port:8000`
