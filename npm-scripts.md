# NPM Scripts

`npm` is a great tool for build automation. Much of the time, you can just use npm scripts rather than Gulp or Grunt.

## Why NPM Scripts
* JavaScript all the things.
* Cut down on dependencies.
* Use any NPM script (Remember to `—save-dev`).
* Always up to date.
* Remove dependence on plugin authors.
* Less code to debug.
* No need to learn plugins
* Avoid frustrating debugging

## Common misconceptions
*  NPM scripts require strong command line skills.
*  NPM scripts aren’t powerful enough.
*  Gulp’s streams are necessary for fast builds.
*  NPM scripts don’t run cross platform.

## package.json
You define all your scripts in the `package.json` file.
If you don’t already have it, read below.

### Get Started
```bash
$ npm init
```

### Example
The following is an example of a package.json file. You define scripts as
children in the `scripts` object.

```json
{
  "name": "foo",
  "version": "0.0.1",
  "description": "foo",
  "main": "index.js",
  "scripts": {
    "test": "echo testing",
    "start": "echo starting",
    "stop": "echo stopping",
    "restart": "echo restarting",
    "start:dev": "echo 'something else i guess'"
  }
}
```

## Invoke commands
NPM provides a couple of shorthands for invoking commands.
To list all commands in package.json run `npm run`.

```bash
# Start shorthand
$ npm start

# Test shorthands
$ npm test
$ npm tst
$ npm t

# Start and restart
$ npm stop
$ npm restart

# Everything else
$ npm run myscript
```

If you haven't defined `npm restart`, NPM  will run stop and then start.

## Pre- and Post- hooks
You can run pre and post hooks before and after a script.
A hook is just another script, prefixed with *pre* or *post*.
Hooks are just like any other scripts, and you can run them directly with `npm run premyscript`.
The order in which you define hooks doesn't matter.

```json
  "scripts": {
    "premyscript": "echo premyscript",
    "myscript": "echo myscript",
    "postmyscript": "echo postmyscript"
  },
```

## Chaining
With NPM scripts it’s possible to chain commands, just as you do with Gulp and
Grunt. NPM scripts are basically just shell commands you invoke through `NPM
run`, which means you can use all your favourite shell operators.

### Ampersand Operator: Parallel commands
You can also use the `&` operator to run two commands at the same time on Unix.

```bash
npm run script1.js & npm run script2.js
```

You can also use [Parallelshell](https://github.com/keithamus/parallelshell) to
run commands in parallel - cross platform. Another great option for this is
[npm-run-all](https://www.npmjs.com/package/npm-run-all).

### AND Operator: Chain commands
Chaining commands (*Waits for each command to finish successfully before
starting the next*) is possible with the `&&` operator. This is very similar to
`pre-` or `post-` hooks.

The AND Operator would execute the second command only if the execution of first
command succeeds.

### OR Operator

### Pipe Operator
This `|` operator is very useful where the output of first command acts as an
input to the second command.

### Output Operator
`>` Output to file
```bash
grep 'John Doe' bigFileWithNames.txt > linesWithJohnDoe.txt
```

## Complex Scripts
Decompose big problems by calling one script from another.
Use `&&` to call multiple scripts serially on a single line.
```json
{
  "scripts": {
    "clean": "rimraf ./dist && mkdir dist",
    "prebuild": "npm run clean",
    "build": "cross-env NODE_ENV=production webpack"
  }
}
```

If a command gets too complicated, you can always call a separate file
```json
{
	"scripts": {
    "build": "node build.js"
  }
}
```

## Streams
You don’t need Gulp for streams. Streaming has always been built into both Unix
and Windows command lines. The pipe `|` operator streams the output of one
command to the input of another command. And the redirection `>` operator
redirects output to a file.

## Cross-platform

```bash
&&  # chain tasks (Run one task after another)
<   # input file contents to a command
>   # redirect command output to a file
|   # redirect command output to another command
```

You can also use node packages instead of shell commands.  For example use the
package `rimraf` instead of `rm -rf` or use `cross-env` to set environment
variables in a cross-platform way. Find modules by searching Google, NPM or take
a look at libraries.io.

Last but not least, you can use [shelljs](https://www.npmjs.com/package/shelljs)
for portable Unix shell commands.


## Version Bumping
npm version - shows current version
```json
{
  "scripts": {
    "version:major": "npm version major",
    "version:minor": "npm version minor",
    "version:patch": "npm version patch"
  }
}
```

#### Notes
Use the `npm -s` flag to silence npm's output from the subtasks, which makes the
log output a little tidier (it is a shortcut for --loglevel=silent:

## Further Reading
* http://substack.net/task_automation_with_npm_run
* https://medium.com/@dabit3/introduction-to-using-npm-as-a-build-tool-b41076f488b0
* https://css-tricks.com/why-npm-scripts
* https://medium.freecodecamp.com/why-i-left-gulp-and-grunt-for-npm-scripts-3d6853dd22b8
