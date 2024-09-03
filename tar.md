# tar

* `man tar`
* `tar -cf name.tar.gz file1 file2 file3`: make (non-compressed) tarball
* `tar -czf name.tar.gz file1 file2 file3`: make compressed (gzipped) tarball
* `tar -cZf name.tar.gz file1 file2 file3`: compress to compress
* `tar -tvf name.tar.gz | less`: view content of tarball
* `tar -rf name.tar.gz file-to-append... `: append file (only works with non-compressed)
* `tar -czf $(for f in /path/to/files/*; do process_file; echo "${f}"; done)`: compose with loop
* `find /path/to/pack -type f -exec tar -czf {}`: compose with find
* `find /path/to/pack -type f | xargs tar -czf`: compose with xargs
* `find /path/to/pack -type f | xargs tar -czf $(for .. in ...; do ... done;)`: all together now

