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

## Git

You'll need to install [Git](https://git-scm.com/) to interact with the Learn platform. We'll cover Git in greater depth later on, but for now you should know that it's _source control management_ software. That's a fancy way of saying that it helps keep track of revisions and changes to your code.

To install Git (and a bunch of other useful software), open your terminal and try to enter `git` — it will most likely fail and prompt you to install the OS X Command Line Tools. Go ahead and install them.

## Configuring Git and GitHub

Next, you'll need to set up your SSH keys so that [GitHub](https://github.com) can recognize your local machine.

Log in on GitHub, and then go to your settings.

![GitHub settings](https://curriculum-content.s3.amazonaws.com/javacs/github_settings.png)

On the lefthand side of the screen, click "SSH keys".

At the bottom of the "SSH keys" box that shows up on the next screen, click the link for "generating SSH keys" and follow the instructions there.

Now when you go to clone a repository, be sure to clone it with SSH!

## A Ruby Setup that You'll Like

OS X comes with Ruby (2.0 by default) – don't use it. A bunch of system libraries and utilities depend on it, and if you end up changing something, your system could break in weird and unexpected ways.

Instead, install a Ruby version manager – this gives you greater flexibility and keeps your system Ruby untouched.

(Note: Some of you might be complaining about installing Ruby for a series of Java lessons. Learn's software depends on Ruby, and while we won't be covering it much here, Ruby is an interesting language and one that's used all over the place in software engineering (especially web development). You don't have to like it, but you'd do well to learn it.)

We're going to use [`rvm`](https://rvm.io/) as our version manager. Install it with the following commands:

```bash
gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
\curl -sSL https://get.rvm.io | bash -s stable --ruby=2.3.0
```

This will take a while.

Verify the installation with `ruby -v`. It should print something like `ruby 2.3.0p0 (2015-12-25 revision 53290) [x86_64-darwin15]`.

If any of the above steps don't work exactly as expected, be sure to restart your terminal session and try again before assuming something is broken.


## The Learn Gem

Ruby packages are called "gems." Learn provides a command line interface as a gem; you can install it with

``` bash
gem install learn-co
gem install learn-test
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

You now have access to the `learn` command in any of the upcoming lessons. `learn-test` will run your tests, and `learn submit` will submit your work.

Happy learning!


## Resources

- [Guide to installing Ruby (on Rails) on OS X](https://gorails.com/setup/osx/10.11-el-capitan); **ignore the Rails-specific bits**
- [Homebrew](http://brew.sh/)
- [rvm](https://rvm.io/)
