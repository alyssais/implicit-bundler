Implicit Bundler
================

Sometimes I have to switch between multiple Ruby versions. This could be because a project uses an old version, or because I've just upgraded to a new one.

When I do this, usually the first command I'll run is `bundle`, which I usually won't have installed. Then I'll have to install Bundler. Then I'll realise that the version of Bundler I just installed is different to the version required in the project's Gemfile.lock, so then I'll have to install that version. _ugh_.

Implicit Bundler solves this problem. When you run `bundle`, if it isn't installed it'll download it for you. It also wraps [postit](https://github.com/segiddins/postit), so whenver you run `bundle` in a project directory, the correct version will automatically be installed if it isn't already.

**Note**: Implicit Bundler currently only works if your Ruby install is managed by [rbenv](https://github.com/sstephenson/rbenv).

Installation
------------

```sh
brew install alyssais/utils/implicit-bundler
```

You also need to make sure that the `bundle` command points to Implicit Bundler. To do this, add the following to your .bashrc/.zshrc:

```sh
alias bundle=implicit-bundler
```

Contributing
------------

Bug reports and pull requests are welcome on GitHub at https://github.com/alyssais/implicit-bundler. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](contributor-covenant.org) code of conduct.


License
-------

The utility is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

