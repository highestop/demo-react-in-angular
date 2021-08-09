# React In Angular

Progressive Migration From Angular(v12) to React(v17)

## Getting Started

My origin remote codebase is in GitLab, so `git remote add github git@github.com:highestop/react-in-angular.git` first to add the github remote.

Next `git checkout github:main && git switch -c main` to create a local branch `main` which upstream is set to `github:main`.

If there is another code source only need to fetch and rebase, `git remote add source **` and then `git fetch source && git rebase origin/master` to update codes from source to local, then push to `origin:master` or checkout `main` and rebase and do `git push --set-upstream github main` push to `github:main`.
