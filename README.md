# Getting Started with Learn on OS X

## Overview

At this point, you probably already have an environment setup that you like – we don't want to mess with that. We _do_, however, want to make sure that your environment can talk to Learn.

# Setup

## Setting Up Your Environment for Learn.co

You need a proper development environment to learn to code. Whether you're learning Web Development, with a focus on Ruby, Python, or Javascript; or Mobile Development, with a focus on Objective-C & iOS or Java & Android; this guide is going to go through the manual steps you can take to set up your environment to work with Learn.co .

## Automating the Setup with Environmentalizer

Normally we setup your computer using the [Learn OSX Companion application](https://flatironschool-static.s3.amazonaws.com/learn.zip). That is definitely the easiest way to set up your computer.

If you use that app, a Github account is all you need (and you presumably already have one, since you're reading this document!).

### **If you use the Learn Companion App, you don't need to continue reading this guide; you are done!**

*If you're curious, or want more control over your environment, feel free to continue on for manual instructions.*

## About the Learn App

That application actually just uses a BASH script called [Environmentalizer](https://github.com/learn-co-curriculum/setup-with-environmentalizer).

You can either choose to run that script manually or proceed with this guide to install the requirements as you see fit.

## Manual Requirements

In general the list of requirements for using Learn are:

1. A [GitHub](https://github.com/join) account. You can use the free account on GitHub—you won't need private repositories at this point.

2. You should have your GitHub account tied to your shell preferably via [SSH](https://help.github.com/articles/generating-ssh-keys/) but you can use [OSX Keychains](https://help.github.com/articles/updating-credentials-from-the-osx-keychain/).

3. You'll need a way to compile software. If you're on OSX, the best thing you can do is use [XCode](https://developer.apple.com/xcode/downloads/) and [XCode Command Line Tools](https://developer.apple.com/library/ios/technotes/tn2339/_index.html) [download for 10.10 XCode 6.3.1](http://adcdownload.apple.com/Developer_Tools/Command_Line_Tools_OS_X_10.10_for_Xcode_6.3.1/commandlinetoolsosx10.10forxcode6.3.1.dmg) to get GCC.

4. You'll probably need a package manager of some sort. We love [Homebrew](http://brew.sh/) on OSX.

5. You're going to need [git](http://git-scm.com/downloads). It generally comes with most modern operating systems, can be installed via Homebrew, apt-get, and most package managers easily. 

6. A Ruby Interpreter. Having a working interpreter is a great idea because so much tooling is built in Ruby. This is true for Web Development with Python or Javascript, and even for Mobile Development with iOS & XCode. If you can type `ruby -v` and not get an error, you probably have enough of a Ruby environment. If you are studying Web Development with Ruby (such as the Rails framework) you definitely need a great Ruby environment. We love [RVM](https://rvm.io/) for managing Ruby versions and environments.

7. The `learn` gem. Simply type: `gem install learn-co` or if you get a permissions error, `sudo gem install learn-co`. Then type in `learn` to configure it with your github account and you'll be all set.

8. A Text Editor. For iOS, XCode is a great IDE. But you'll find the free editors [Sublime Text](http://www.sublimetext.com/) and [Atom](https://atom.io/) useful anyway so go ahead an install them.

Those are the absolute requirements.


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
