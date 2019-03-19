These scripts are here to help development process. 

Some of the executables might depend on git aliases:
 - alias.go=checkout
 - alias.b=branch
 - alias.c=commit
 - alias.st=status
 - alias.cl=clone
 - alias.fs=fetch --all --prune

# Usage

 1. Update `app_location.cfg` to the location of your APIs. (It sets a variable called `ROOT_DIR`)
 2. Learn what each executable does. Some of the executables might be dependency of another.
 3. Enjoy the simplified development!

## api-refresh

Refreshes API(s). Uses Git Fetch, Git Pull, Composer install.

### Arguments

 1. Directory to be used (optional)
 	- must be an existing directory in `ROOT_DIR`
	- if not passed all directories will be used in `ROOT_DIR/*-api`
	- pass `.` to use current directory
 2. Branch to be used (optional)
	- if not passed current branch will be used.
	- if passed branch does not exist current branch will be used.
 
### Dependencies

 - gf
 - gitall
 - cpinstall

## cpinstall

Executes a `composer install` in each directory in `ROOT_DIR/*-api`.

## dcr

Executes a php command via docker.

### Arguments
 1. Name of the executable command
 2. Arguments of command

## deploy-api

Refreshes APIs, builds up its docker containers, executes necessary php commands (e.g. doctrine schema update).

### Arguments

 1. Branch to be used (optional)
	- if not passed current branch will be used.
	- if passed branch does not exist current branch will be used.

### Dependencies

 - api-refresh

## dfaps

List all docker containers formatted containing "api".

## dfps

List all docker containers formatted.

## docker-compose-deploy

Refreshes common-docker, builds up its docker containers.
Refreshes APIs, builds up its docker containers, executes necessary php commands (e.g. doctrine schema update).

### Dependencies

 - deploy-api

## docker-compose-restart

Restarts the docker containers based on docker-compose.yml in the current directory.

## docker-sync-restart

Restarts docker-sync in devenv_installer directory.

## gbdel

Deletes a branch. Both local and origin.

### Arguments

 1. Branch to be used

## gd

Creates a git diff export to the home directory and opens it in sublime text.

### Arguments

 1. Arguments of git diff

### Dependencies

 - [Sublime Text](https://www.sublimetext.com)

## gds

Creates a git diff of staged files export to the home directory and opens it in sublime text.

### Arguments

 1. Arguments of git diff

### Dependencies

 - [Sublime Text](https://www.sublimetext.com)

## gf

Alias to execute `git fetch --all --prune`.

## gitall

Executes git command in children directories of working directory.

### Arguments

 1. Git command

## glog

Creates a git log export to the home directory and opens it in sublime text.

### Arguments

 1. Arguments of git log

### Dependencies

 - [Sublime Text](https://www.sublimetext.com)

## gsgo

Smart Git Checkout. Uses stash, checkout, stash pop.

### Arguments

 1. Branch to be used

### Dependencies

## gspull

Smart Git Pull. Uses stash, pull, stash pop.

## lsapps

Lists apps from `ROOT_DIR`.

## osu

Executes doctrine schema update based on the phpfpm container of the current directory.

### Arguments

 1. Arguments of doctrine schema update.

### Dependencies

 - dcr

## package-release

Deprecated. Sends a notification to Slack about a dh-slim package.

### Arguments

 1. package name
 2. version

### Dependencies

 - php