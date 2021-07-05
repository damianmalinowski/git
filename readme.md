git init

git add -A

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
