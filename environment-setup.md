# How to Setup Your Ruby Environment

This guide will walk you through the steps for setting up a full functioning Ruby environment setup on your local machine. The process varies depending on your operating system. If you have access to an Apple computer running a recent version of OS X or a desktop Linux version, I'd highly recommend using it. Although the tools for Windows have greatly improved over the last few years, development is still smoothest on a *-nix based operating system. 

## Mac OS X

OS X comes preinstalled with (typically outdated) version of Ruby. For various reasons, it's better to install a Ruby version manager to allow you to install multiple versions on your machine and easily switch between them. There are a number of different open source options available, but we will use [rbenv](https://github.com/sstephenson/rbenv).

The easiest way to install rbenv is though [Homebrew](http://brew.sh/), a nifty little package manager for OS X.

### Install or Update Homebrew

To install, open up Terminal (in your Applications > Utilities directory) and run the following command:

    ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"

If you already have Homebrew installed on your machine, you may need to update it first:

    brew update

### Install git

Run the following command to install the latest version of git:

    brew install git

### Install rbenv

Once Homebrew is installed, run the following:

    brew install rbenv ruby-build

This will install rbenv and ruby-build, a little utility that will download and compile ruby versions for you. After installation, you'll need to add a line to your bash profile using `pico` (or your favorite text editor):

    pico ~/.bash_profile

Paste the following at the end of the file:

    eval "$(rbenv init -)"

Then, Save and Exit (`Control-X`, `Y` to save). Close and re-open a new terminal window to apply the changes.

### Install your first ruby version

We'll use one of the latest versions of Ruby in the 2.x branch:

    rbenv install 2.0.0-p247

This may take a while. Plug your laptop into a wall outlet and go brew a cup of coffee.

When complete, run the following to set this as your global Ruby version:

    rbenv global 2.0.0-p247

Run `ruby -v` and you should see something to the effect of `ruby 2.0.0p247 (...)`.

And that's it!

## Windows

Download [RailsInstaller](http://railsinstaller.org/en) for Windows and check out the installation help video.