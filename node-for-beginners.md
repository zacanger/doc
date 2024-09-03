# Node For Beginners

Some things you should do right away:
* Install node. Go to <https://nodejs.org> and get the installer appropriate for
  your OS.
* Make sure it stays up to date. If you're on Mac or Linux, use NPM to install
  N: `npm i -g n`; using N is simple, just do `n latest` to get the latest Node
  and NPM.
  * If you're on windows, check out <https://github.com/marcelklehr/nodist>.
* Install some helpful global modules: `npm i -g live-server luvi bower`. I'm
  suggesting both live-server and luvi because the code live-server injects to
  refresh the page can sometimes conflict with client-side JS (like Angular).
* If you're getting permissions errors, you'll need to own the directory where
  Node installs modules. Rather than running `sudo` before every NPM command,
  just take ownership of `/usr/local` with the command `chown -R yourusername
  /usr/local`.

## What?
Node is a JavaScript runtime. It's a program (usually run from the command line)
which executes JavaScript, and comes with a built-in library for writing network
and filesystem code.  Node is built on [V8](https://code.google.com/p/v8/), the
same JavaScript VM used in the Chrome browser.  Instead of being wrapped with a
GUI and web browser features like the DOM, node wraps V8 to expose lower-level
operating system APIs.  Some modules that come with node include: `http`, `fs`
(filesystem), `crypto` (cryptography), and lots more.

### What's a module?
Modules are chunks of code you can 'require' and then use.  Today we'll use the
`http` module, like so:

```javascript
const http = require('http')
```

`require` is a function built into node.  It takes a string module name and
returns that module.

### You can make your own modules!

```javascript
// my-module.js
module.exports = 'hey!'

// app.js
const myModule = require('./my-module')
console.log(myModule)
```

Notice the require string is now a relative path, and that we've emitted the
`.js`.  It's optional for the `js` extension.

Modules are great for breaking your code down into smaller pieces that are
easier to think about.

## `http` module
This is what we'll be using today, but first...

### The network stack
- HTTP
- TLS (optional)
- TCP
- IP
- Ethernet
- Physical card

Try this: `ping www.google.com`

You should see an IP address in parenthesis that will be used for subsequent
pings.  Where'd that address come from?  This is the IP layer, specifically a
DNS (Domain Name Service) lookup.

Try pinging again using that IP address instead.  The results should be the
same.

Now try this: `telnet www.google.com 80`

This is the next layer up: TCP.  Telnet is a tool for working with TCP
connections.  The command above says to open a TCP connection with
`www.google.com` on port `80`, which is the default for non-secure web traffic.

HTTP is the next layer after TCP (in a non-secure connection), so let's try
some!

```
(still inside the telnet prompt)
GET / HTTP/1.1
```

Did you get all the HTML back?  We can do everything above in one step with `curl`:
`curl www.google.com`

`curl` is an HTTP tool.

### Ok, back to node!
Make a new directory to work in, then create a `server.js` file in that
directory.  Edit that file so it looks like this:

```javascript
const http = require('http')
```

### What is Non-blocking IO?
When PHP hits a line that requires an IO operation, like a database read/write,
PHP basically pauses execution at that line and hands over control to the
database software to execute the command. Once the operation on the database
completes, the control is given back to PHP and executes the commands after that
line. This is blocking, because the database operation "blocks" PHP execution
until it completes. With the same situation, NodeJS does this by asynchronously
calling the IO operation. This means that while the operation is ongoing on the
database, NodeJS proceeds in doing other stuff like cater the next request. When
the IO operation completes, NodeJS runs the handler that was set to handle the
data when the operation completes.  Great for RESTful APIs

```javascript
// server.js
const
  http      = require('http')
, server    = http.createServer()
, port      = process.env.PORT || 4444
, onRequest = (req, res) => {
	res.statusCode = 200
  res.setHeader('X-XSS-Protection', '1; mode=block')
  res.setHeader('Content-Type', 'text/html')
	res.end('<h1>Hello world</h1>')
}
server.on('request', onRequest)
server.listen(port)
console.log(`server listening on ${port}`)
```

Run using `node server`.

Now make a really simple html page that tries to access the endpoint they just
created. Make sure they understand that we're using jQuery/$.get as just a
really simple way to make a web request. We've done this with Angular services
up to this point.

```html
<!doctype html>
<html lang="en">
<head>
  <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/jquery/2.2.6/jquery.min.js"></script>
  <script type="text/javascript">
    // $http in Angular. $.get in jQuery.
    $(function(){$.get('http://localhost:4444')})
  </script>
</head>
</html>
```

Open the file using live-server or luvi. Open the network tab and examine the
request and response.

### Quick Tips
- `$ node -v` see what version of node you are using
- `$ chmod u+x myscript.js` make your javascript file executable
- `#!/usr/bin/env node` use this shebang at the top of all node files you want to be executable
- Using ES6 Modules and ES7 in Node: `npm i -g babel-cli`, then run programs
  with `babel-node` instead of `node`.

### Links

#### Projects
- [Making a Game API Server in Node (Revisited)](http://blog.couchbase.com/making-a-game-api-server-using-nodejs-revisited)
- [Write your shell scripts in JavaScript, via Node.js](http://www.2ality.com/2011/12/nodejs-shell-scripting.html)
- [Managing Node.js Dependencies with Shrinkwrap (manage Dependency Collisions)](http://blog.nodejs.org/2012/02/27/managing-node-js-dependencies-with-shrinkwrap/)
- [How To Self Detect A Memory Leak in Node](http://www.nearform.com/nodecrunch/self-detect-memory-leak-node/)
- [Get Open Graph Data with Node.js](http://davidwalsh.name/open-graph-data-nodejs)

#### Continuous Integration
- [Travis CI](https://travis-ci.org/)
- [AppVeyor](http://www.appveyor.com/)

#### Awesome Node.js Lists
- [sindresorhus/awesome-nodejs](https://raw.githubusercontent.com/sindresorhus/awesome-nodejs/master/readme.md)

#### Learning node.js
- [You Don’t Know Node: Quick Intro to Core Features](https://medium.com/software-engineering/you-don-t-know-node-quick-intro-to-core-features-8e5146655bef)
- [NodeSchool](http://nodeschool.io/)
- [node.js Interview Questions](https://blog.risingstack.com/node-js-interview-questions/)

#### Books
- [Node.js in Action, Second Edition](https://www.manning.com/books/node-js-in-action-second-edition)
- [Node.js The Right Way](https://pragprog.com/book/jwnode/node-js-the-right-way)

#### Testing & Debugging Node
- [TEN TIPS FOR CODING WITH NODE.JS #1: DEVELOP DEBUGGING TECHNIQUES](http://www.nearform.com/nodecrunch/node-js-develop-debugging-techniques/)
- [Node.js Testing Strategies](http://www.pluralsight.com/courses/nodejs-testing-strategies)
- [Debugging Node.js Applications Using Core Dumps](https://reaktor.com/blog/debugging-node-js-applications-using-core-dumps/)

#### Node CLI
- [minimist](https://github.com/substack/minimist)

#### Node Security
- [Secure Node Apps Against OWASP Top 10](http://scottksmith.com/blog/2015/06/08/secure-node-apps-against-owasp-top-10-injection/)
- [Top Overlooked Security threats to Node.js Web Applications](https://speakerdeck.com/player/c5d895008c77013162b85e7a2e8ee0d7)

#### Design Patterns
- [Fundamental Node.js Design Patterns](https://blog.risingstack.com/fundamental-node-js-design-patterns/)

# Giant Bunch of Resources

|Title|URL|Description|Level of Difficulty*|
| ------ | ------ | ------ | ------ | ------ |
|NodeSchool Learn You Node|http://nodeschool.io|A command line workshopper course for learning Node.js at your own pace|1||
|Express.js Fundamentals|http://flippinawesome.org/2013/11/11/express-js-fundamentals/|Covers the basics of getting started and core concepts|1||
|The Art of Node|http://github.com/maxogden/art-of-node|An introduction to Node.js that includes the command line workshopper Learn You Node and Stream Adventure courses from nodeschool.io|1||
|Learn to Code|http://ifoundthemeaningoflife.com/learntocode|Not so much a tutorial as a guide through available tutorials. Path from beginner > JS & Node > intermediate|1||
|Node.js Fundamentals|http://strongloop.com/developers/videos/#a-video-intro-to-nodejs-fundamentals|Video explaining Node.js fundamentals|1||
|Intro to Express.js Parameters, Error Handling and Other Middleware |http://flippinawesome.org/2013/05/28/intro-to-express-js-parameters-error-handling-and-other-middleware/|Discusses some of the core Express features in the form of middleware|2||
|Emailing in Node.js with Nodemailer |http://blog.ijasoneverett.com/2013/07/emailing-in-node-js-with-nodemailer/|Walks through the process of using nodemailer to send email|2||
|The Dead-Simple Step-by-Step Guide for Front-End Developers to Getting Up and Running with Node.JS, Express, Jade, and MongoDB |http://cwbuecheler.com/web/tutorials/2013/node-express-mongo/|Set up the full stack and have a webpage running in 30 minutes. Make it talk to your DB in another 30. |2||
|Understanding JavaScript Callbacks |http://cwbuecheler.com/web/tutorials/2013/javascript-callbacks/|Unlocking the Asynchronous Powers of JavaScript|2||
|Understanding Express.js|http://evanhahn.com/understanding-express/|Overview of Connect and Express concepts like middlewares, request handling, routing, etc.|2||
|Creating a Simple RESTful Web App with Node.js, Express, and MongoDB |http://cwbuecheler.com/web/tutorials/2014/restful-web-app-node-express-mongodb/|Learn the basics of REST and use them to build an easy, fast, single-page web app. - 3|3||
|Writing a Command Line Utility using Node|http://flippinawesome.org/2013/07/29/writing-a-command-line-utility-using-node/|Steps through building a simple command-line calculator program that accepts two parameters and adds them together|4||
|Node Sass Boilerplate|https://github.com/anotheruiguy/node-sass-boilerplate|A bare bones Node project using the C version of Sass called libsass using the Node.js bindings to libsass. There is a full readme of instructions to build your own project from scratch using npm and Grunt. Use the full example project as a measure with the instructions. |4||
|A Sample App with Node.js, Express and MongoDB – Part 1|http://blog.ijasoneverett.com/2013/03/a-sample-app-with-node-js-express-and-mongodb-part-1/|Walks through the process of creating a CRUD app|4||
|A Sample App with Node.js, Express and MongoDB – Part 2 |http://blog.ijasoneverett.com/2013/04/a-sample-app-with-node-js-express-and-mongodb-part-2/|Continuation of part 1.  Covers editing and deleting from MongoDB|4||
|Building Multiplayer Games with Node.js and Socket.IO|http://flippinawesome.org/2013/09/30/building-multiplayer-games-with-node-js-and-socket-io/|Walks through the basics of building a simple multi-screen, multiplayer word game using the Socket.IO library within Node|5||
|Teach Yourself Node.js in 10 Steps|http://blog.ponyfoo.com/2013/07/12/teach-yourself-nodejs-in-10-steps|An introductory overivew of Node.js, npm, callback conventions, events, and HTTP server basics|2||
|Bevry's introduction to Node.js|http://bevry.me/node/preface|This class was originally run for General Assembly in Sydney, and has been recorded and made available online.|3||
|Node Angular Mongo & Express
Mean stack articles + many good things|http://flip.it/OxXyB|Magazine about the MEAN stack (MongoDB, ExpressJS, AngularJS and Node.js)|*||
|Learn All The Nodes|https://www.youtube.com/playlist?list=PLQmX5gaHg2SXyKuT9BQ_nbFIdZ39yeRxH|Weekly screencasts on Node.js.  The current episodes are all beginners.|2||
|Node: Up and Running|http://chimera.labs.oreilly.com/books/1234000001808/index.html|Book by Tom Hughes-Croucher, a bit older, but explains the fundamentals|2||
|Hackathon Starter|https://github.com/sahat/hackathon-starter|Boilerplate app to get Noding in no time!|4||
|Full Streams Ahead|http://dry.ly/full-streams-ahead|Introduction to streams in Node|4||
|Node.js Picture VOting App Tutorial|http://tutorialzine.com/2014/01/nodejs-picture-voting-game-part-1/|Step by step on how to create a voting app in node.js|3||
|Real-time collaborative drawing with Node.JS|http://12devsofxmas.co.uk/2012/12/day-3-realtime-collaborative-drawing-with-node-js/|Step by step on how to create a real-time collaborative drawing tool with the Express framework for node.js, socket.io & paper.js|2||
|Javascript Weekly|http://javascriptweekly.com/|Javascript weekly mailing list|*||
|Introduction to Node.js|http://hectorcorrea.com/#/blog/introduction-to-node-js/51|How to get started with Node.js for web development for people coming from other platforms. From console "hello world" to web page with basic HTTP GET/POST.|2||
|Node.js Stream Handbook|https://github.com/substack/stream-handbook|A handbook covering the basics of how to write node.js programs with streams.|3||
|Node Tuts|http://nodetuts.com/|Video tutorials for Node.js|2||
|Node.js Tutorial for Beginners|http://www.tutorialindustry.com/node-js-tutorial-for-beginners|If you are a beginner looking for a quick way to learn node.js then BINGO! you have come to the right place.|2||
|Node.js Express: Definition, Installation, Project structure, Example|http://www.tutorialindustry.com/node-js-express-tutorial|Learn how to use node.js express framework to build web applications. express framework provides all the low level services for you so that you can focus on more important things.|2||
|Node.js Mongodb: Express, Mongoose Installation, Examples|http://www.tutorialindustry.com/node-js-mongodb-tutorial-for-beginners|Learn node.js interaction with mongodb, perform CRUD operations, serve static and dynamic contents using example.|2||
|Node.js Mysql: Express, Mysql Module Installation, Examples|http://www.tutorialindustry.com/node-js-mysql-tutorial-for-beginners|Learn node.js interaction with MySql database, perform CRUD operations, serve static and dynamic content using example.|2||
|Node.js Mail Tutorial: Send Emails Using Nodemailer Module|http://www.tutorialindustry.com/nodejs-mail-tutorial-using-nodemailer-module|Node.js Mail Tutorial: If you are a beginner and looking for an easy way to send mails in node.js, try nodemailer module.|2||
|How to Upload Files to Node.js Server Using Express Framework|http://www.tutorialindustry.com/how-to-upload-files-to-nodejs-server|Learn how to upload files to node.js server, learn what modules are required and the uploading process along with the source code.|2||
|How to Read/Write Files in Node.js using File System (fs) Module|http://www.tutorialindustry.com/how-to-read-write-files-in-node-js-using-file-system-fs-module|Learn how to write a file, read files in node.js. I have explained through an example how to read/write files using the inbuilt node.js file system (fs) module.|2||
|Node.js CouchDB Tutorial: Using Nano, Express Modules, Examples, CRUD Operations|http://www.tutorialindustry.com/node-js-couchdb-tutorial-for-beginners|Learn how to install nano, express modules, node.js couchdb examples. How to interact with couchdb and perform CRUD Operations.|3||
|Node.js Redis Tutorial: Express, Redis Modules, Examples with Explanation|http://www.tutorialindustry.com/nodejs-redis-tutorial-for-beginners|Learn how to integrate redis into your node.js application in a step by step procedure along with examples, Interaction with Redis Sever.|3||
|5 Best Node.js Books for Beginners- Javascript Basic, Nodejs Starter Books|http://www.tutorialindustry.com/5-best-nodejs-books-for-beginners|There are many great books available for node.js, here are few books from the best publishers on javascript, nodejs beginners, advanced.|1||
|Node.js Developer Roadmap: How to Be a Node.js Developer?|http://www.tutorialindustry.com/how-to-be-a-nodejs-developer|Why should I learn Node.js? What are the prerequisites? What are the steps involved in becoming a good nodejs programmer?|1||
|Node.js Infographic|http://www.tutorialindustry.com/nodejs-infographic|This Node.js Infographic explains why you should learn node.js (in a different approach.) Also checkout the google trends showing node.js, indeed.com showing node.js job trends.|1||
|10 Habits of the Happy Node Hacker|https://blog.heroku.com/archives/2014/3/11/node-habits|A blog post from Heroku with tips and techniques to keep you and your node apps happy.|||
|Server Side Node|https://github.com/hegdeashwin/Server-Side-Node.js|This training kit has been developed for those who already have the basic knowledge of JavaScript; This training kit will teach you the basics of NodeJS and NPM (Node Package Manager).|1||


_\*1 is "What is JavaScript?" and 5 is "Go forth, young padawon, rely on your training and you will succeed!"_

