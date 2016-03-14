# Getting Started with Learn on OS X

## Overview

At this point, you probably already have an environment setup that you like – we don't want to mess with that. We _do_, however, want to make sure that your environment can talk to Learn.

## Homebrew (no, not that kind of homebrew)

Some might argue that OS X loses to Linux when it comes to package management; those folks haven't used `brew`.

What's great about [Homebrew](http://brew.sh/) is that it helps to isolate your development environment(s) from your system environments. You won't have to worry about bricking your machine with a botched Python upgrade, for example.

To get started, simply open your terminal (by default, `Terminal.app`) and enter

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

That's it!

## A Ruby Setup that You'll Like

OS X comes with Ruby (2.0 by default) – don't use it. A bunch of system libraries and utilities depend on it, and if you end up changing something, your system could break in weird and unexpected ways.

Instead, use `brew` to install a Ruby version manager – this gives you greater flexibility and keeps your system Ruby untouched.

(Note: Some of you might be complaining about installing Ruby for a series of Java lessons. Learn's software depends on Ruby, and while we won't be covering it much here, Ruby is an interesting language and one that's used all over the place in software engineering (especially web development). You don't have to like it, but you'd do well to learn it.)

We're going to use [`rbenv`](https://github.com/rbenv/rbenv#homebrew-on-mac-os-x) as our version manager. Install it with `brew`:

```bash
brew install rbenv ruby-build
```

After installation finishes, run `rbenv init` and follow the instructions that print out. For the lazy, you can probably get by with

```bash
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bash_profile
```

Finally, install Ruby 2.3.0:

```bash
rbenv install 2.3.0
rbenv global 2.3.0
```

Verify the installation with `ruby -v`. It should print something like `ruby 2.3.0p0 (2015-12-25 revision 53290) [x86_64-darwin15]`.

If any of the above steps don't work exactly as expected, be sure to restart your terminal session and try again before assuming something is broken.


## The Learn Gem

Ruby packages are called "gems." Learn provides a command line interface as a gem; you can install it with

``` bash
gem install learn-co
```

If you run `learn hello`, you can walk through the setup of connecting this interface to your account on learn.co.

## Java and Ant

`brew` makes [Java](https://java.com/en/download/) and [Ant](http://ant.apache.org/) incredibly easy to install. Just run

```bash
brew cask install java
brew install ant
```

and you should be good to go.

## Wrap-up

You now have access to the `learn` command in any of the upcoming lessons. `learn` will run your tests, and `learn submit` will submit your work.

Happy learning!


## Resources

- [Guide to installing Ruby (on Rails) on OS X](https://gorails.com/setup/osx/10.11-el-capitan); **ignore the Rails-specific bits**
- [Homebrew](http://brew.sh/)
- [rbenv](https://github.com/rbenv/rbenv)
