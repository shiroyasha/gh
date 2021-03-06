# GH - Git project managment tool - v0.9

![Logo](http://fc06.deviantart.net/fs46/f/2009/245/3/9/WALLPAPER___RainbowSlide_by_lastscionz.jpg)

Developers usually work on multiple Git repositories at once, cloning, pushing,
and keeping their local repositories up to date. This can be achieved manually,
but after a certain threshold of local repositories (around 10 repositories)
this process can become tedious and time consuming.

GH is here help. If you keep your local repositories in a project directory it
can help you list their current statuses, pull the latest changes, or even
remove some of them.

Here is an example workflow with GH:

For example let's clone the following repositories into your local cache:
 - [Faraday](https://github.com/lostisland/faraday)
 - [Base App](https://github.com/renderedtext/base-app)
 - [Rails](https://github.com/rails/rails)

You can achieve this very easily using GH:

``` bash
$ gh clone lostisland/faraday
$ gh clone renderedtext/base-app
$ gh clone rails/rails
```

The above commands will by default put these repositories into the `$HOME/code`
directory. You can list them with `gh list`.

``` bash
$ gh list
base-app -> git@github.com:/renderedtext/base-app.git
faraday -> git@github.com:/lostisland/faraday.git
rails -> git@github.com:/rails/rails.git
```

Or even inspect their statuses with `gh status`:

``` txt
$ gh status
base-app
## master...origin/master

rails
## master...origin/master
 D Rakefile

faraday
## master...origin/master
```
## Installation

You can use the following automatic installer command that will install GH
inside the `bin` directory in your home path.

``` sh
curl -L 'https://raw.githubusercontent.com/shiroyasha/gh/master/install' | bash
```

### Adding GH to your path

After installation, please append GH's path into your PATH environment variable.
You can achieve this by adding the following line into your `.bashrc` or `.zshrc`
file:

``` sh
export PATH=$PATH:$HOME/bin
```

## Projects path

GH uses the `PROJECTS_PATH` environment variable to determine
the location where you store your git projects. By default
this directory is `$HOME/code` but you can change it simply
by exporting another value:

```
export PROJECTS_PATH=$HOME/projects
```

GH will create the projects directory if it doesn't exists

## Usage

### gh status
  Shows the statuses of all local git projects

### gh clone
  Clone a project from GitHub into your projects directory
  For example to clone Faraday(https://github.com/lostisland/faraday)
  type the following:

    gh clone lostisland/faraday

### gh rm
  Removes a local git project from your projects directory
  For example to remove Faraday type the following:

    gh rm faraday

### gh list
  Lists all your local git projects

### gh exec
  Executes a bash command in every projects directory
  For example to count the number of files in each directory
  type the following

    gh exec 'ls | wc -l'

### gh help
  Shows this help message

## About

Written and maintained by Igor Sarcevic
Distrubuted under MIT Licence
