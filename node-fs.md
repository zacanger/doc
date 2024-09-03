# Node's FS


```javascript
// Reading
fs.readFile('./file', (err, data) => {})
fs.readFile('./file', { encoding: 'utf-8' }, (err, data) => {})
fs.readFileSync('./file')

// Writing
fs.writeFile('./file', (err, data) => {})
fs.writeFileSync('./file', data)
fs.appendFile('./file', (err, data) => {})
fs.appendFileSync('./file', data)

// Watch
fs.watch('./file (or directory)', { persistent: true }, (e, file) => {})

// Info
fs.stat('./file', a => {
  a.isFile()
  a.isDirectory()
  a.isSymbolicLink()
})

// Misc operations
fs.rename('old', 'new', () => {})
fs.chown('file', uid, gid, () => {})
fs.symlink('src', 'dest', () => {})
fs.unlink('link', () => {})
fs.rmdir('dir', () => {})
fs.readdir('dir', (err, files) => {})
fs.realpath('path', (err, path) => {})
```
