# GH - Git project menagment tool - v0.9

## Usage

### gh exec
  Shows this help message

### gh status
  Shows the statuses of all local git projects

### gh clone
  Clone a project from github into your projects directory
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

## About

Written and maintained by Igor Sarcevic
Distrubuted under MIT Licence
