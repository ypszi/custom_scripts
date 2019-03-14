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

Refreshes APIs.

### Arguments
 1. Directory to be used (optional)
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
### Arguments
### Dependencies

## dfps
### Arguments
### Dependencies

## docker-compose-deploy
### Arguments
### Dependencies

## docker-compose-restart
### Arguments
### Dependencies

## docker-sync-restart
### Arguments
### Dependencies

## gallpull
### Arguments
### Dependencies

## gbdel
### Arguments
### Dependencies

## gd
### Arguments
### Dependencies

## gds
### Arguments
### Dependencies

## gf
### Arguments
### Dependencies

## gitall
### Arguments
### Dependencies

## glog
### Arguments
### Dependencies

## gsgo
### Arguments
### Dependencies

## gspull
### Arguments
### Dependencies

## lsapps
### Arguments
### Dependencies

## osu
### Arguments
### Dependencies

## package-release
### Arguments
### Dependencies
