# basic commands

git init

`git add -A` or `git add .`

git remote add origin git@github.com:damianmalinowski/git-demo.git

git remote -v

git push --set-upstream origin main

git fetch

git pull === git fetch & git merge

git branch new-feature
git branch

git checkout new-feature

git checkout -b new-feature2

git checkout - // swith to previous branch

git branch -d new-feature

git commit -a

git commit -a -m 'another new lines'

git log

type `/searchquery` and use `n` => next result and `N` previous result

git log --oneline
git log --decorate
git log --graph c

git log -p // show changes

git log --stat // show statistic of changed files

clear // clear screen

git log -3 // show only last three commits

git log --after="3/15/16"
git log --before="yesterday"

git log --author="Trevou|Jane"

git log --grep="copyright"

git log -p -S"Math"
git log -p -GMath\|Random // use regular expression to go trough changed files

git log -i --author="Damian" // but ingore Case

git log --no-merges // ??????????

git log aaa.txt

git log -S"Math" --after="2 months ago" --oneline --stat

git diff

git diff --stat

git diff --cached

git diff HEAD

git diff origin/master

git diff prigin/master getRandomNumber.js

git blame readme.md

git log 8d0f -p

git tag v1.0.0
git tag

git tag -a v1.0.1 -m 'some message' // add adnotation

git log origin/master..

git rebase -i origin/master

git bisect start
git bisect bad
git log --oneline
git bisect good 105syu45m
git bisect reset

# adding git hook

modify file hooks/pre-commit

#!/bin/bash
npm run test

- hooks are added localy, so if you want to use it in remote place, you have to copy the hook

# global config file

git config --global user.name 'Jane Doe'
git config --global user.email 'damian.malinowski@axbit.com'
git config --global core.editor vim
cat ~/.gitconfig

git config --global alias.graph 'log --graph --oneline'

git config --list
git config --global --list

# .gitignore

git config --global core.excludesfile ~/.gitignore_global

git add src/app/app.comonent.\*

# Productive Git for Developers

## better looked log by adding alias

`lg = log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit --branches`

## move changes which were added to master to separate branch

- creating feature branch
- reset local master to `git reset --hard 9a7f06b`

## update my feature branch with the latest changes from master

- you can do it by `git merge master` if you share remote branch this is better way
- or do `git rebase master` you rewrite commit hashes, so you can notice desync with pushed remote branch. If you want to overwrite remote branch you can use `git push --force-with-lease'

## polish my git feature branch

final revert change

## Squash all of my commits into a singleone and merge into master

`git merge --squash app-refactoring`

## change the commit message of my last commit

`git commit --amend`

## add a file I've forgotten to add to my last commit

`git commit --amend`
