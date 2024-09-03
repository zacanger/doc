# BUNDLER

* bundle # installs
* bundle install
* bundle install --path <path>
* bundle update
* bundle outdated
* bundle list
* bundle check
* bundle console
* bundle exec <command>
* bundle clean
* bundle clean --force

# RVM

* rvm list
* rvm list gemsets
* rvm gemset list
* rvm gemset create <name>
* rvm gemset use <name>
* rvm install <version>
* rvm <version> do gem install <gem>
* rvm <version> do bundle install

```
curl -sSL https://get.rvm.io | bash -s stable
source /home/username/.rvm/scripts/rvm
rvm use --default <version>
bundle install
```

# GEM

* gem env
* gem list
* gem outdated
* gem update <name>
* gem install <name>
* gem uninstall <name>

# RSPEC

* autotest
* rspec <path to spec>
* rspec <path to dir>
* bundle exec rspec <path to file>

# SHELL

* irb
* pry
* irb -r script
* require foo
* y <something> print as yaml

# MISC

* something.class
* something.to_s
* something.inspect

```
if (defined?(var)).nil?
  puts 'undef'
end
```

* hash1.merge(hash2)
* hash.keys.sort

```
hash.sort.map do |key, value|
  # do stuff
end
```

* File.open('filename.extension', 'w') { |file| file.write('stuff') }

