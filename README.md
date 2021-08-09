# React In Angular

React(v.17) in Angular(v.12), demo for progressive migration.

## How to use

The origin remote codebase is in GitLab, so `git remote add github git@github.com:highestop/react-in-angular.git` first to add the github remote.

Next `git checkout github:main && git switch -c main && git branch --set-upstream github main` to create a local branch `main` and set its upstream to `github:main`.

If there is another code source only to fetch and update, `git remote add source **` and then `git fetch source && git rebase source/master` to update codes from source to local, then push to `origin:master`. Or checkout `main` and rebase in the same way and do `git p` push to `github:main`.

Noted that, this README file is only available on Github, so DO NOT rebase `github:main` on other branches and push them to their sources. That may cause some problems for other people.
